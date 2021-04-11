---
title: 使用內容控制碼進行伺服器開發
description: 從伺服器程式開發的觀點來看，內容控制碼是不具類型的指標。 伺服器程式會將內容控制碼指向記憶體中的資料，或儲存在其他形式的儲存體 (（例如磁片上的檔案) ），藉以初始化內容控制碼。
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021892"
---
# <a name="server-development-using-context-handles"></a><span data-ttu-id="17588-104">使用內容控制碼進行伺服器開發</span><span class="sxs-lookup"><span data-stu-id="17588-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="17588-105">從伺服器程式開發的觀點來看，內容控制碼是不具類型的指標。</span><span class="sxs-lookup"><span data-stu-id="17588-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="17588-106">伺服器程式會將內容控制碼指向記憶體中的資料，或儲存在其他形式的儲存體 (（例如磁片上的檔案) ），藉以初始化內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="17588-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="17588-107">比方說，假設用戶端使用內容控制碼來要求一系列資料庫中記錄的更新。</span><span class="sxs-lookup"><span data-stu-id="17588-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="17588-108">用戶端會呼叫伺服器上的遠端程式，並將搜尋金鑰傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="17588-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="17588-109">伺服器程式會搜尋資料庫中的搜尋索引鍵，並取得相符記錄的整數記錄號碼。</span><span class="sxs-lookup"><span data-stu-id="17588-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="17588-110">然後伺服器就可以在包含記錄號碼的記憶體位置上指向 void 的指標。</span><span class="sxs-lookup"><span data-stu-id="17588-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="17588-111">當它傳回時，遠端程式必須透過其傳回值或其參數清單，將指標傳回為內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="17588-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="17588-112">用戶端每次呼叫遠端程式來更新記錄時，都必須將指標傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="17588-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="17588-113">在每個更新作業期間，伺服器會將 void 指標轉換成整數的指標。</span><span class="sxs-lookup"><span data-stu-id="17588-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="17588-114">在伺服器程式指向內容資料的內容控制碼之後，會將控制碼視為開啟。</span><span class="sxs-lookup"><span data-stu-id="17588-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="17588-115">包含 **Null** 值的控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="17588-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="17588-116">伺服器會維護開啟的內容控制碼，直到用戶端呼叫關閉它的遠端程式為止。</span><span class="sxs-lookup"><span data-stu-id="17588-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="17588-117">如果在控制碼開啟時，用戶端會話終止，則 RPC 執行時間會呼叫伺服器執行時間常式來釋放控制碼。</span><span class="sxs-lookup"><span data-stu-id="17588-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="17588-118">下列程式碼片段會示範伺服器如何執行內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="17588-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="17588-119">在此範例中，伺服器會維護用戶端使用遠端程式寫入的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="17588-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="17588-120">內容資訊是一個檔案控制代碼，它會追蹤伺服器寫入資料之檔案中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="17588-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="17588-121">檔案控制代碼會封裝為參數清單中的內容控制碼，以進行遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="17588-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="17588-122">結構包含檔案名和檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="17588-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="17588-123">此範例的介面定義會在 [使用內容控制碼的介面開發](interface-development-using-context-handles.md)中顯示。</span><span class="sxs-lookup"><span data-stu-id="17588-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="17588-124">函數 RemoteOpen 會在伺服器上開啟檔案：</span><span class="sxs-lookup"><span data-stu-id="17588-124">The function RemoteOpen opens a file on the server:</span></span>


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



<span data-ttu-id="17588-125">函數 RemoteRead 會讀取伺服器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="17588-125">The function RemoteRead reads a file on the server.</span></span>


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



<span data-ttu-id="17588-126">函數 RemoteClose 會關閉伺服器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="17588-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="17588-127">請注意，伺服器應用程式必須將 **Null** 指派給內容控制碼，作為 close 函數的一部分。</span><span class="sxs-lookup"><span data-stu-id="17588-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="17588-128">這會與伺服器 stub 以及已刪除內容控制碼的 RPC 執行時間程式庫進行通訊。</span><span class="sxs-lookup"><span data-stu-id="17588-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="17588-129">否則，連接將保持開啟狀態，最後會發生內容執行。</span><span class="sxs-lookup"><span data-stu-id="17588-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


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
> <span data-ttu-id="17588-130">在預期的情況下，用戶端會將有效的內容控制碼傳遞給具有 \[ in、out \] 方向屬性的呼叫，但 RPC 不會拒絕此方向屬性組合的 **Null** 內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="17588-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="17588-131">**Null** 內容控制碼會以 **null** 指標的形式傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="17588-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="17588-132">\[應撰寫包含 in、out \] 內容控制碼之呼叫的伺服器程式碼，以避免在收到 **Null** 指標時發生存取違規。</span><span class="sxs-lookup"><span data-stu-id="17588-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




