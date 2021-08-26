---
title: 在伺服器上執行輸入管道
description: 若要開始將資料傳送到伺服器，用戶端會呼叫其中一個伺服器的遠端程式。
ms.assetid: 6abaa851-41bf-4a03-8d12-cd595d74c8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf133fce019328b9fa7d6b2a03e47d516de5ca74310d611ecea1686c0b9a3a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020518"
---
# <a name="implementing-input-pipes-on-the-server"></a>在伺服器上執行輸入管道

若要開始將資料傳送到伺服器，用戶端會呼叫其中一個伺服器的遠端程式。 此程式必須在伺服器的存根中重複呼叫提取程式。 MIDL 編譯器會使用應用程式的 IDL 檔案來自動產生伺服器的提取程式。

每次伺服器程式在其存根中叫用提取程式時，提取程式都會接收來自用戶端的資料區塊。 它會將資料拆收到伺服器的緩衝區。 然後，伺服器的遠端程式就可以用任何需要的方式處理此資料。 迴圈會繼續執行，直到伺服器收到長度為零的緩衝區為止。

下列範例是來自平臺軟體發展工具組 (SDK) 隨附的範例中所包含的 Pipedemo 程式。 它說明使用管道從用戶端將資料提取到伺服器的遠端伺服器程式。

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

 

 




