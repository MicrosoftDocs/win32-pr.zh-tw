---
title: 在伺服器上執行輸出管道
description: 若要開始從伺服器接收資料，用戶端會呼叫其中一個伺服器的遠端程式。
ms.assetid: 5d791f4f-1d95-4bc0-b68f-db4fccc75ff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3eb1362736207f9cc79d82ab6c981431d0bfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023978"
---
# <a name="implementing-output-pipes-on-the-server"></a><span data-ttu-id="890b2-103">在伺服器上執行輸出管道</span><span class="sxs-lookup"><span data-stu-id="890b2-103">Implementing Output Pipes on the Server</span></span>

<span data-ttu-id="890b2-104">若要開始從伺服器接收資料，用戶端會呼叫其中一個伺服器的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="890b2-104">To begin receiving data from a server, a client calls one of the server's remote procedures.</span></span> <span data-ttu-id="890b2-105">此程式必須在伺服器的存根中重複呼叫推送程式。</span><span class="sxs-lookup"><span data-stu-id="890b2-105">This procedure must repeatedly call the push procedure in the server's stub.</span></span> <span data-ttu-id="890b2-106">MIDL 編譯器會使用應用程式的 IDL 檔案來自動產生伺服器的推送程式。</span><span class="sxs-lookup"><span data-stu-id="890b2-106">The MIDL compiler uses the application's IDL file to automatically generate the server's push procedure.</span></span>

<span data-ttu-id="890b2-107">在呼叫推送程式之前，遠端伺服器常式必須在輸出管道的緩衝區中填入資料。</span><span class="sxs-lookup"><span data-stu-id="890b2-107">The remote server routine must fill the output pipe's buffer with data before it calls the push procedure.</span></span> <span data-ttu-id="890b2-108">每次伺服器程式在其存根中叫用推送程式時，推送程式都會將資料封送處理，並將其傳輸至用戶端。</span><span class="sxs-lookup"><span data-stu-id="890b2-108">Each time the server program invokes the push procedure in its stub, the push procedure marshals the data and transmits it to the client.</span></span> <span data-ttu-id="890b2-109">迴圈會繼續執行，直到伺服器傳送長度為零的緩衝區為止。</span><span class="sxs-lookup"><span data-stu-id="890b2-109">The loop continues until the server sends a buffer of zero length.</span></span>

<span data-ttu-id="890b2-110">下列範例是來自 Windows SDK 隨附的範例中所包含的 Pipedemo 程式。</span><span class="sxs-lookup"><span data-stu-id="890b2-110">The following example is from the Pipedemo program contained in the samples that come with the Windows SDK.</span></span> <span data-ttu-id="890b2-111">它說明使用管道將資料從伺服器推送至用戶端的遠端伺服器程式。</span><span class="sxs-lookup"><span data-stu-id="890b2-111">It illustrates a remote server procedure that uses a pipe to push data from the server to the client.</span></span>


```C++
void OutPipe(LONG_PIPE *outputPipe )
{
    long *outputPipeData;
    ulong index = 0;
    ulong elementsToSend = PIPE_TRANSFER_SIZE;
 
    /* Allocate memory for the data to be passed back in the pipe */
    outputPipeData = (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    while(elementsToSend >0) /* Loop to send pipe data elements */
    {
        if (index >= PIPE_SIZE)
            elementsToSend = 0;
        else
        {
            if ( (index + PIPE_TRANSFER_SIZE) > PIPE_SIZE )
                elementsToSend = PIPE_SIZE - index;
            else
                elementsToSend = PIPE_TRANSFER_SIZE;
        }
                    
        outputPipe->push( outputPipe->state,
                          &(outputPipeData[index]),
                          elementsToSend ); 
        index += elementsToSend;
 
    } //end while
 
    free((void *)outputPipeData);
 
}
```



## <a name="related-topics"></a><span data-ttu-id="890b2-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="890b2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="890b2-113">管道</span><span class="sxs-lookup"><span data-stu-id="890b2-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="890b2-114">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="890b2-114">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 