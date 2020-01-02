# Common Search Results Issues

## ISSUE: Archived (Old or Unwanted) Documents in Search Results
You can remove unwanted documents from appearing in search results. The process involves two steps:
1. Index only the directories (or folders) where the updated docs, discussions, and/or content is
2. Recrawl your content source(s) after changing indexing settings

### 1. Index What Can Be Indexed
#### **FOR WEBSITE CS**
1. Create a directory ``` /archive``` (you can select another name).
2. Place all the documents in ```/archive```.
3. Go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** > **By Filter**.
4. Enter the absolute path of the place where the archived documents are placed in the **Should Not Crawl** box. If your archived documents are placed at ```mycompany.com/archives```, then enter ```https://mycompany.com/archives```. ![Should Not Crawl](https://i.ibb.co/mhqmKQp/archives.png)   
#### **FOR ALL OTHER CSes**
1. Go to **Search Clients** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Content Sources** > **Create Formula**.
2. Exclude the directory from appearing in search results. The instructions for using Create Formula are in [Use Create Formula for Access Control](https://docs.searchunify.com/Content/Search-Clients/Create-Formula.htm) 

### 2. Recrawl Your CS
1. Go to **Content Sources** and click ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/recrwal.png). 

## ISSUE: Content Fields Not Indexed
A content type, such as a Zendesk ticket, can have multiple content fields. SearchUnify indexes them all by default. But an admin can change settings, leading to some fields being removed from search. You can fix that.
1. Go to the **Rules** tab of your content source. To find it, go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png). 
2. In the dialog that opens, select the content fields for indexing and searching.


