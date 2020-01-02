# ISSUE: Content Source Not Indexed 
There can be multiple reasons for content source indexing to fail. The ones that apply to all content sources include:

## Applicable to All Content Sources
- Insufficient permissions: The person whose ID was used to authorize crawling is doesn't have the ``rwx``` permissions on the content they are trying to crawl.
- No content fields selected: Go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** and ensure that at least one content field is selected.

## "Content Source"-Specific Reasons

### Google Drive
Google Drive does not permit SearchUnify to find and index files until you explicitly provide access. To enable access, go to Search Clients > Edit > Content Sources, and toggle Permissions Override to the left.

### Lithium and Other Communities 
Ensure that all boards, or the ones that you desire to index, are not set to hidden.

### Salesforce
- Be an admin user with access to the files that you are trying to index. If you cannot view a file on your org, then the chances of SearchUnify indexing it are nil.
- Ensure that you are a Knowledge user if youare trying to index Salesforce Communities.

## YouTube and Vimeo
Subscribe to at least one channel and/or upload at least one video on your channel. Nary a subscription or upload, SearchUnify will have no data to crawl.

## ISSUE: Content Fields Not Indexed
A content type, such as a Zendesk ticket, can have multiple content fields. SearchUnify indexes them all by default. But an admin can change settings, leading to some fields being removed from search. You can fix that.
1. Go to the **Rules** tab of your content source. To find it, go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png). 
2. In the dialog that opens, select the content fields for indexing and searching.
