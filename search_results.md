# Common Search Results Issues

## ISSUE: Archived (Old or Unwanted) Documents in Search Results
You can remove unwanted documents from appearing in search results by 
1. Limiting SearchUnify (SU) crawls to the directories (or folders) where the updated docs, discussions, and/or content is.
2. Recrawling your content source (CS) after changing indexing settings.

### 1. Change What Can Be Indexed
#### **FOR WEBSITE CS**
Create a directory ``` /archive``` (you can select another name) and place all the documents in that directory.
If your CS is a website, go to Content Sources > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > Rules > By Filter, and enter the absolute path of the place where the archived documents are placed in the **Should Not Crawl** box. If your archived documents are placed at ```mycompany.com/archives```, then enter ```https://mycompany.com/archives``` and ```http://mycompany.com/archives```. ![Should Not Crawl](https://i.ibb.co/mhqmKQp/archives.png)   
#### **FOR ALL OTHER CSes**
If your CS is not a website, go to Search Clients > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > Content Sources > Create Formula, and exclude the directory from appearing in search results. The instructions for using Create Formula are in [Use Create Formula for Access Control](https://docs.searchunify.com/Content/Search-Clients/Create-Formula.htm) 

### 2. Recrawl Your CS
Go to **Content Sources** and click ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/recrwal.png). 

## ISSUE: Some Content Fields Are Not Indexed
A content type, such as a Zendesk ticket, can have multiple content fields. SearchUnify indexes them all by default. But an admin can change settings, leading to some fields being removed from search. You can fix that in the **Rules** tab of your CS. To find it, go to **Content Sources** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png) > **Rules** > ![EDIT](https://docs.searchunify.com/Content/Resources-Mamba20/Images/Icons/edit-tuning.png). In the dialog that opens, select the content fields for indexing and searching.

