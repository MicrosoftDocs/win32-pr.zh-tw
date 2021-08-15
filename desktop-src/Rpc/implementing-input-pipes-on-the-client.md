---
title: 在用戶端上執行輸入管道
description: 使用輸入管道將資料從用戶端傳送到伺服器時，您必須執行提取程式。
ms.assetid: e941a6be-ca91-42b1-9323-ffc63d521f6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0301fc7324a982db81b6c728131762361cfce185f3d432f238ca2cf8d715546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929117"
---
# <a name="implementing-input-pipes-on-the-client"></a>在用戶端上執行輸入管道

使用輸入管道將資料從用戶端傳送到伺服器時，您必須執行提取程式。 提取程式必須尋找要傳送的資料、將資料讀入緩衝區，以及設定要傳送的元素數目。 當伺服器開始將資料提取到本身時，並非所有資料都必須在緩衝區中。 提取程式可以累加方式填滿緩衝區。

如果沒有其他要傳送的資料，程式會將其最後一個引數設定為零。 傳送所有資料時，提取程式應該在傳回之前，先進行任何必要的清除作業。 針對屬於 \[ in、out 管道的參數 \] ，提取程式必須在傳輸所有資料之後重設用戶端的狀態變數，讓推送程式可以使用它來接收資料。

下列範例是從平臺軟體發展工具組 (SDK) 所隨附的 Pipedemo 程式中解壓縮。


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void SendLongs()
{
    LONG_PIPE inPipe;
    int i;
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
 
    for (i=0; i<PIPE_SIZE; i++)
        globalPipeData[i] = IN_VALUE;
 
    pipeDataIndex = 0;
    inPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    inPipe.pull  = PipePull;
    inPipe.alloc = PipeAlloc;
 
    InPipe( inPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );

}//end SendLongs
 
void PipeAlloc( rpc_ss_pipe_state_t stateInfo,
                ulong requestedSize,
                long **allocatedBuffer,
                ulong *allocatedSize )
{ 
    ulong *state = (ulong *)stateInfo;
    if ( requestedSize > (BUF_SIZE*sizeof(long)) )
    {
       *allocatedSize = BUF_SIZE * sizeof(long);
    }
    else
    {
       *allocatedSize = requestedSize;
    }
    *allocatedBuffer = globalBuffer; 
} //end PipeAlloc
 
void PipePull( rpc_ss_pipe_state_t stateInfo,
               long *inputBuffer,
               ulong maxBufSize,
               ulong *sizeToSend )
{
    ulong currentIndex;
    ulong i;
    ulong elementsToRead;
    ulong *state = (ulong *)stateInfo;

    currentIndex = *state;
    if (*state >=  PIPE_SIZE )
    {
        *sizeToSend = 0; /* end of pipe data */
        *state = 0; /* Reset the state = global index */
    }
    else 
    {
        if ( currentIndex + maxBufSize > PIPE_SIZE )
            elementsToRead = PIPE_SIZE - currentIndex;
        else
            elementsToRead = maxBufSize;
 
        for (i=0; i < elementsToRead; i++)
        {
            /*client sends data */
            inputBuffer[i] = globalPipeData[i + currentIndex];
        }
 
        *state +=   elementsToRead;
        *sizeToSend = elementsToRead;
    } 
}//end PipePull
```



此範例包含 MIDL 編譯器所產生的標頭檔。 如需詳細資訊，請參閱 [在 IDL 檔案中定義管道](defining-pipes-in-idl-files.md)。 它也會宣告它用來做為資料來源的變數（稱為 globalPipeData）。 變數 globalBuffer 是提取程式用來傳送從 globalPipeData 取得之資料區塊的緩衝區。

SendLongs 函式會宣告輸入管道，並為數據源變數 globalPipeData 配置記憶體。 在您的用戶端/伺服器程式中，資料來源可以是用戶端所建立的檔案或結構。 您也可以讓您的用戶端程式從伺服器取得資料、加以處理，然後使用輸入管道將它返回伺服器。 在這個簡單的範例中，資料來源是一種動態配置的長整數緩衝區。

在開始傳輸之前，用戶端必須設定狀態變數、提取程式和配置程式的指標。 這些指標會保留在用戶端宣告的管道變數中。 在此情況下，SendLongs 會宣告 inPipe。 您可以針對狀態變數使用任何適當的資料類型。

用戶端會藉由叫用伺服器上的遠端程式，在管道之間起始資料傳輸。 呼叫遠端程式會告訴伺服器程式用戶端已準備好要傳送。 然後伺服器就可以將資料提取到本身。 這個範例會叫用名為 InPipe 的遠端過程。 將資料傳輸至伺服器之後，SendLongs 函式會釋出動態配置的緩衝區。

每次需要緩衝區時，不需配置記憶體。 此範例中的配置程式只會將指標設定為變數 globalBuffer。 提取程式會在每次傳送資料時重複使用此緩衝區。 每次伺服器從用戶端提取資料時，更複雜的用戶端程式可能需要配置新的緩衝區。

用戶端 stub 會呼叫提取程式。 此範例中的提取程式會使用狀態變數來追蹤全域資料來源緩衝區中要讀取的下一個位置。 它會將來源緩衝區的資料讀入管道緩衝區。 用戶端存根會將資料傳輸至伺服器。 傳送所有資料之後，提取程式會將緩衝區大小設定為零。 這會告訴伺服器停止提取資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管道](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 