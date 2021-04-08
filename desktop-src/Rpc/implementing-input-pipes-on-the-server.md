---
title: 在伺服器上執行輸入管道
description: 若要開始將資料傳送到伺服器，用戶端會呼叫其中一個伺服器的遠端程式。
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d60c2436129b59619f5a9954c70823631d72ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840215"
---
# <a name="implementing-input-pipes-on-the-server"></a><span data-ttu-id="6c4d1-103">在伺服器上執行輸入管道</span><span class="sxs-lookup"><span data-stu-id="6c4d1-103">Implementing Input Pipes on the Server</span></span>

<span data-ttu-id="6c4d1-104">若要開始將資料傳送到伺服器，用戶端會呼叫其中一個伺服器的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-104">To begin sending data to a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="6c4d1-105">此程式必須在伺服器的存根中重複呼叫提取程式。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-105">This procedure must repeatedly call the pull procedure in the server's stub.</span></span> <span data-ttu-id="6c4d1-106">MIDL 編譯器會使用應用程式的 IDL 檔案來自動產生伺服器的提取程式。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-106">The MIDL compiler uses the application's IDL file to automatically generate the server's pull procedure.</span></span>

<span data-ttu-id="6c4d1-107">每次伺服器程式在其存根中叫用提取程式時，提取程式都會接收來自用戶端的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-107">Each time the server program invokes the pull procedure in its stub, the pull procedure receives blocks of data from the client.</span></span> <span data-ttu-id="6c4d1-108">它會將資料拆收到伺服器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-108">It unmarshals the data into the server's buffer.</span></span> <span data-ttu-id="6c4d1-109">然後，伺服器的遠端程式就可以用任何需要的方式處理此資料。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-109">The server's remote procedure can then process this data in any way required.</span></span> <span data-ttu-id="6c4d1-110">迴圈會繼續執行，直到伺服器收到長度為零的緩衝區為止。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-110">The loop continues until the server receives a buffer of zero length.</span></span>

<span data-ttu-id="6c4d1-111">下列範例是來自平臺軟體發展工具組 (SDK) 隨附的範例中所包含的 Pipedemo 程式。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-111">The following example is from the Pipedemo program contained in the samples that come with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="6c4d1-112">它說明使用管道從用戶端將資料提取到伺服器的遠端伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="6c4d1-112">It illustrates a remote server procedure that uses a pipe to pull data from the client to the server.</span></span>

``` syntax
//file: server.c (fragment)
#include uc_server.c
#define PIPE_TRANSFER_SIZE 100 /* Transfer 100 pipe elements at one time */
 
void InPipe(LONG_PIPE     long_pipe )
{
    long local_pipe_buf[PIPE_TRANSFER_SIZE];
    ulong actual_transfer_count = PIPE_TRANSFER_SIZE;
 
    while(actual_transfer_count > 0) /* Loop to get all 
                                        the pipe data elements */
    {
        long_pipe.pull( long_pipe.state,
                        local_pipe_buf,
                        PIPE_TRANSFER_SIZE,
                        &actual_transfer_count);
        /* process the elements */
    } // end while
} //end InPipe
```

 

 




