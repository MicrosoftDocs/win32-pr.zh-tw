---
title: 使用內容控制碼進行伺服器開發
description: 從伺服器程式開發的觀點來看，內容控制碼是不具類型的指標。 伺服器程式會將內容控制碼指向記憶體中的資料，或儲存在其他形式的儲存體 (（例如磁片上的檔案) ），藉以初始化內容控制碼。
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db05441f7314fba628d1ec07db5f99266c595c84e672ada976b38f7576ab5d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925334"
---
# <a name="server-development-using-context-handles"></a>使用內容控制碼進行伺服器開發

從伺服器程式開發的觀點來看，內容控制碼是不具類型的指標。 伺服器程式會將內容控制碼指向記憶體中的資料，或儲存在其他形式的儲存體 (（例如磁片上的檔案) ），藉以初始化內容控制碼。

比方說，假設用戶端使用內容控制碼來要求一系列資料庫中記錄的更新。 用戶端會呼叫伺服器上的遠端程式，並將搜尋金鑰傳遞給它。 伺服器程式會搜尋資料庫中的搜尋索引鍵，並取得相符記錄的整數記錄號碼。 然後伺服器就可以在包含記錄號碼的記憶體位置上指向 void 的指標。 當它傳回時，遠端程式必須透過其傳回值或其參數清單，將指標傳回為內容控制碼。 用戶端每次呼叫遠端程式來更新記錄時，都必須將指標傳遞至伺服器。 在每個更新作業期間，伺服器會將 void 指標轉換成整數的指標。

在伺服器程式指向內容資料的內容控制碼之後，會將控制碼視為開啟。 包含 **Null** 值的控制碼已關閉。 伺服器會維護開啟的內容控制碼，直到用戶端呼叫關閉它的遠端程式為止。 如果在控制碼開啟時，用戶端會話終止，則 RPC 執行時間會呼叫伺服器執行時間常式來釋放控制碼。

下列程式碼片段會示範伺服器如何執行內容控制碼。 在此範例中，伺服器會維護用戶端使用遠端程式寫入的資料檔案。 內容資訊是一個檔案控制代碼，它會追蹤伺服器寫入資料之檔案中的目前位置。 檔案控制代碼會封裝為參數清單中的內容控制碼，以進行遠端程序呼叫。 結構包含檔案名和檔案控制代碼。 此範例的介面定義會在 [使用內容控制碼的介面開發](interface-development-using-context-handles.md)中顯示。


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



函數 RemoteOpen 會在伺服器上開啟檔案：


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



函數 RemoteRead 會讀取伺服器上的檔案。


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



函數 RemoteClose 會關閉伺服器上的檔案。 請注意，伺服器應用程式必須將 **Null** 指派給內容控制碼，作為 close 函數的一部分。 這會與伺服器 stub 以及已刪除內容控制碼的 RPC 執行時間程式庫進行通訊。 否則，連接將保持開啟狀態，最後會發生內容執行。


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> 在預期的情況下，用戶端會將有效的內容控制碼傳遞給具有 \[ in、out \] 方向屬性的呼叫，但 RPC 不會拒絕此方向屬性組合的 **Null** 內容控制碼。 **Null** 內容控制碼會以 **null** 指標的形式傳遞至伺服器。 \[應撰寫包含 in、out \] 內容控制碼之呼叫的伺服器程式碼，以避免在收到 **Null** 指標時發生存取違規。

 

 

 




