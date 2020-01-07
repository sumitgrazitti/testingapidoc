## ISSUE: Archived (Old or Unwanted) Documents in Search Results {Incomplete problem statement}
> *Applicable only to Website content sources. For other content sources, check out **[No Way to Exclude Documents from Search](https://github.com/chetangrazitti/testingapidoc/blob/master/search_results.md#issue-no-way-to-exclude-documents-from-search)*** 

You can remove unwanted documents from appearing in search results. The process involves two steps:

### 1. Select What Can Be Indexed
1. Create a directory ``` /archive``` (you can select another name).
2. Place all the documents in ```/archive```.
3. Go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** > **By Filter**.
4. Enter the absolute path of the place where the archived documents are placed in the **Should Not Crawl** box. If your archived documents are placed at ```mycompany.com/archive```, then enter ```https://mycompany.com/archive```. ![Should Not Crawl](https://i.ibb.co/mhqmKQp/archives.png)   

### 2. Recrawl Your CS
1. Go to **Content Sources** and click ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/recrwal.png). 


{we can mention about date-boosting as well for old and archived docs. That's a good use case.}
