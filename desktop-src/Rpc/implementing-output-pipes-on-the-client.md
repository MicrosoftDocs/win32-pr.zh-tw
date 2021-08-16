---
title: 在用戶端上執行輸出管道
description: 使用輸出管道將資料從伺服器傳送至用戶端時，您必須在用戶端中執行推播程式。
ms.assetid: ab544daf-fbf7-4b00-95a8-55c149a86c27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e959db9e505bb7dfe570552fe0385251485591fecb1f818ab4d5de402c2297b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929127"
---
# <a name="implementing-output-pipes-on-the-client"></a>在用戶端上執行輸出管道

使用輸出管道將資料從伺服器傳送至用戶端時，您必須在用戶端中執行推播程式。 推送程式會從用戶端 stub 取得緩衝區和元素計數的指標，而如果專案計數大於0，則會處理資料。 例如，它可以將資料從存根的緩衝區複製到它自己的記憶體。 或者，它可以處理存根緩衝區中的資料，並將它儲存到檔案中。 當元素計數等於零時，推送程式會先完成任何所需的清除工作，然後再傳回。

在下列範例中，用戶端函數 ReceiveLongs 會配置管道結構和全域記憶體緩衝區。 它會初始化結構、進行遠端程序呼叫，然後釋出記憶體。

## <a name="example"></a>範例


```C++
//file: client.c (fragment)
#include <windows.h>
#include "pipedemo.h"
long *  globalPipeData;
long    globalBuffer[BUF_SIZE];
 
ulong   pipeDataIndex; /* state variable */
 
void ReceiveLongs()
{
    LONG_PIPE *outputPipe;
    idl_long_int i;
 
    globalPipeData =
        (long *)malloc( sizeof(long) * PIPE_SIZE );
    
    pipeDataIndex = 0;
    outputPipe.state =  (rpc_ss_pipe_state_t )&pipeDataIndex;
    outputPipe.push  = PipePush;
    outputPipe.alloc = PipeAlloc;
 
    OutPipe( &outputPipe ); /* Make the rpc */
 
    free( (void *)globalPipeData );
 
}//end ReceiveLongs()

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
 
void PipePush( rpc_ss_pipe_state_t stateInfo,
               long *buffer,
               ulong numberOfElements )
{
    ulong elementsToCopy, i;
    ulong *state = (ulong *)stateInfo;

    if (numberOfElements == 0)/* end of data */
    {
        *state = 0; /* Reset the state = global index */
    }
    else
    {
        if (*state + numberOfElements > PIPE_SIZE)
            elementsToCopy = PIPE_SIZE - *state;
        else
            elementsToCopy = numberOfElements;
 
        for (i=0; i <elementsToCopy; i++)
        { 
            /*client receives data */
            globalPipeData[*state] = buffer[i];
            (*state)++;
        }
    }
}//end PipePush
```



此範例包含 MIDL 編譯器所產生的標頭檔。 如需詳細資訊，請參閱 [在 IDL 檔案中定義管道](defining-pipes-in-idl-files.md)。 它也會宣告變數 globalPipeData，它會用來做為資料接收。 變數 globalBuffer 是推播程式用來接收其儲存在 globalPipeData 中之資料區塊的緩衝區。

ReceiveLongs 函式會宣告管道並配置全域資料接收變數的記憶體空間。 在您的用戶端/伺服器程式中，資料接收器可以是用戶端所建立的檔案或資料結構。 在這個簡單的範例中，資料來源是一種動態配置的長整數緩衝區。

在開始進行資料傳輸之前，您的用戶端程式必須初始化輸出管道結構。 它必須設定狀態變數、推送程式和配置程式的指標。 在此範例中，輸出管道變數稱為 outputPipe。

用戶端會透過叫用伺服器上的遠端程式，來通知伺服器他們已準備好接收資料。 在此範例中，遠端程式稱為 OutPipe。 當用戶端呼叫遠端程式時，伺服器就會開始進行資料傳輸。 每次資料抵達時，用戶端 stub 都會視需要呼叫用戶端的配置和推送程式。

此範例中的配置程式只會將指標設定為變數 globalBuffer，而不是在每次需要緩衝區時配置記憶體。 提取程式接著會在每次傳送資料時重複使用此緩衝區。 每次伺服器從用戶端提取資料時，更複雜的用戶端程式可能需要配置新的緩衝區。

此範例中的推送程式會使用狀態變數來追蹤將資料儲存在全域資料接收緩衝區中的下一個位置。 它會將管線緩衝區的資料寫入接收緩衝區。 然後，用戶端 stub 會從伺服器接收下一個資料區塊，並將它儲存在管道緩衝區中。 傳送所有資料之後，伺服器會傳輸大小為零的緩衝區。 這會提示推送程式以停止接收資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管道](/windows/desktop/Midl/pipe)
</dt> <dt>

[**/Oi**](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 