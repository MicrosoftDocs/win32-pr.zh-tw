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
# <a name="implementing-output-pipes-on-the-server"></a>在伺服器上執行輸出管道

若要開始從伺服器接收資料，用戶端會呼叫其中一個伺服器的遠端程式。 此程式必須在伺服器的存根中重複呼叫推送程式。 MIDL 編譯器會使用應用程式的 IDL 檔案來自動產生伺服器的推送程式。

在呼叫推送程式之前，遠端伺服器常式必須在輸出管道的緩衝區中填入資料。 每次伺服器程式在其存根中叫用推送程式時，推送程式都會將資料封送處理，並將其傳輸至用戶端。 迴圈會繼續執行，直到伺服器傳送長度為零的緩衝區為止。

下列範例是來自 Windows SDK 隨附的範例中所包含的 Pipedemo 程式。 它說明使用管道將資料從伺服器推送至用戶端的遠端伺服器程式。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[管道](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 