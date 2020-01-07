## ISSUE: Content Source Not Indexed 
There can be multiple reasons for content source indexing to fail. The most common ones include:  

- The person whose ID was used to authorize crawling is doesn't have the ```rwx``` permissions on the content they are trying to crawl.
- Somehow the content source was saved without selected any field for indexing. Go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** and ensure that at least one content field is selected.
- Google Drive does not permit SearchUnify to find and index files until you explicitly provide access. To enable access, go to Search Clients > Edit > Content Sources, and toggle Permissions Override to the left.
- Ensure that all boards, or the ones that you desire to index, are not set to hidden. (Lithium and other communities)
- Be an admin user with access to the files that you are trying to index. If you cannot view a file on your org, then the chances of SearchUnify indexing it are nil. (Salesforce)
- Ensure that you are a Knowledge user if youare trying to index Salesforce Communities. (Salesforce)
- Assign each article in Knowledge a category. Category-less articles might not get indexed. (Salesforce)
- Subscribe to at least one channel and/or upload at least one video on your channel. Nary a subscription or upload, SearchUnify will have no data to crawl. (YouTube and Vimeo)
- Use dynamic sitemaps. If a sitemap is static, then SearchUnify might not know that new documents have been created and therefore not index them. (Website)
