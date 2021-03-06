# Common Search Results Issues

## ISSUE: Archived (Old or Unwanted) Documents in Search Results
> *Applicable only to Website content sources. For other content sources, check out **[No Way to Exclude Documents from Search](https://github.com/chetangrazitti/testingapidoc/blob/master/search_results.md#issue-no-way-to-exclude-documents-from-search)*** 

You can remove unwanted documents from appearing in search results. The process involves two steps:

### 1. Select What Can Be Indexed
1. Create a directory ``` /archive``` (you can select another name).
2. Place all the documents in ```/archive```.
3. Go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** > **By Filter**.
4. Enter the absolute path of the place where the archived documents are placed in the **Should Not Crawl** box. If your archived documents are placed at ```mycompany.com/archive```, then enter ```https://mycompany.com/archive```. ![Should Not Crawl](https://i.ibb.co/mhqmKQp/archives.png)   

### 2. Recrawl Your CS
1. Go to **Content Sources** and click ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/recrwal.png). 

## ISSUE: No Way to Exclude Documents from Search 
You can exclude one or two documents from search, or make an entire category of documents invisible to searchers.

### METHOD 1. Exclude One or Two Docs from Search
The simplest way to exclude a few documents from search is to delete them from a search engine's index. The process is simple.
1. Go to **Content Sources** > **Total Documents**.
2. Select your search client from the dropdown.
3. Use the search box to find a document. 
4. Delete it. 

### METHOD 2. Make Entire Doc Category (or Categories) Unsearchable
This process involves excluding documents that have either a specified content field value (authorName) or fall within a specified content field range (date).  
1. Go to **Search Clients** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Content Sources** > **Create Formula**. 
2. Find a content field. It can be ```date```, ```url```, ```authorName```, or anything. Mention a value for the content field and toggle **Parity** to the right. All documents with that content field value will disappear from search. For example, if you set ```firstName``` to ```/chetan/i```, then all the documents written by authors whose first name is "Chetan" will become unsearchable.

You can find the instructions for using Create Formula are in [Use Create Formula for Access Control](https://docs.searchunify.com/Content/Search-Clients/Create-Formula.htm) 

## ISSUE: Lithium Results Are Broken
Renaming is a primary reason for broken Lithium results. When you change the name of a board, recrawl your entire content source. Until the recrawl, all Lithium links will remain broken.

## ISSUE: Results Break and Get Fixed Automatically
Documents are usually inaccessible when indexing is in progress. If you have set indexing to take place at 4 p.m. everyday and the process takes about 5 minutes, then some links might not work during those 5 minutes.

## ISSUE: Cannot Turn Off Search Suggestions 
> **IMPORTANT**. Search suggestions cannot be turned off entirely for a search client.

Search suggestions help users find information quicker. Although they cannot be turned off entirely, you can prevent them from displaying for specific keywords. The process is straightforward.

1. Go to **NLP Manager** > **Suggestions Removal**.
2. Select a search client.
3. Click **Add Text**.
4. Enter the keyword(s) and click **Save.**

Search suggestions will not be displayed for the keyword(s) on the selected search engine.
## ISSUE: Cannot Turn Off Search Suggestions 
> **IMPORTANT**. Search suggestions cannot be turned off entirely for a search client.

Search suggestions help users find information quicker. Although they cannot be turned off entirely, you can prevent them from displaying for specific keywords. The process is straightforward.

1. Go to **NLP Manager** > **Suggestions Removal**.
2. Select a search client.
3. Click **Add Text**.
4. Enter the keyword(s) and click **Save.**

Search suggestions will not be displayed for the keyword(s) on the selected search engine.
## ISSUE: Cannot Turn Off Search Suggestions 
> **IMPORTANT**. Search suggestions cannot be turned off entirely for a search client.

Search suggestions help users find information quicker. Although they cannot be turned off entirely, you can prevent them from displaying for specific keywords. The process is straightforward.

1. Go to **NLP Manager** > **Suggestions Removal**.
2. Select a search client.
3. Click **Add Text**.
4. Enter the keyword(s) and click **Save.**

Search suggestions will not be displayed for the keyword(s) on the selected search engine.
