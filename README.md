## **INTRODUCTION :**

LFCM (Lotus File Cabinet Management) is a distributed attachment storage architecture with a dynamic allocation mechanism for Lotus Domino/Notes.  <br><br><br>

## **Version :** 1.0.1 <br><br>

## **Installation Overview :** <br>
**Step 1:**
Place the physical database template file (CSLE0001.ntf) in
the data root directory of the Lotus Domino/Notes server.

**Step 2:** Deploy the File Cabinet Management system (FileCabinetMgr.ntf). After initialization, configure the following param-
eters:
- Maximum capacity of a single physical database: 𝑓Max
- Maximum number of documents per database: 𝑑Max
- Physical file cabinet storage path
- Application database path that will utilize the file cabinet

**Step 3:** Copy the required components from the LFCM Template Application (FC_App.ntf) into the target application database
(NewDb), and embed the file cabinet subform into the target forms to replace the original RichText field.

> **Step 3.1** (Script Libraries)
Copy the following script libraries into NewDb:
 
- CSIC_Custom_Lib
- CSIC_Encrypt_Lib
- CSIC_FC_ExtendedLib
- CSIC_FC_Lib

> **Step 3.2** (Subforms)
Copy subforms subFileCabinet_0 to subFileCabinet_9 into the subform design of NewDb.

> **Step 3.3** (Embedding)
Embed the required number of file cabinet subforms into the target form according to the number of attachment fields.
For example, embedding subFileCabinet_0 creates a single file cabinet interface.
This refactoring approach significantly reduces development effort and effectively overcomes the file size limitations
of the Lotus Domino/Notes platform.<br><br>


## **Authors** <br>
Cheng-Hsiung Tsai <br><br>
Email : derricktsai@hotmail.com<br><br>

## **Maintainer** <br>
Cheng-Hsiung Tsai <br>
Email : derricktsai@hotmail.com<br><br>

## **License** <br>
This project uses the <a href="https://github.com/derricktsai-nkust/FileCabinet/blob/main/LICENSE">MIT License</a>, with a full version of the license included in the repository.

