---
title: 多個管道的規則
description: 在遠端程序呼叫的單一呼叫中，多個管道的規則 (RPC) 。
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd2de7a44f63d5c943f1d6526ee328bbae3e63c99bac118ec843ad266d1f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925975"
---
# <a name="rules-for-multiple-pipes"></a>多個管道的規則

您可以在 \[ 單一呼叫中將 [**in**](/windows/desktop/Midl/in) \] 、 \[ [**out**](/windows/desktop/Midl/out-idl) \] 和 \[ **in、out** \] 輸送參數結合在一起，但您必須以特定順序處理管道，如下列虛擬程式碼範例所示：

> [!Note]  
> Windows Vista 和更新版本的平臺不再支援此功能。

 

-   從參數中的第一個 (最左邊的) 開始，取得每個輸入管道的資料 \[  \] ，並依序繼續執行，然後在開始處理下一個管道之前清空每個管道。
-   在每個輸入管道都經過完整處理之後，請傳送輸出管道的資料，再一次從第一個 \[ **輸出** \] 參數開始，然後依序繼續執行，然後在開始處理下一個管道之前先填入每個管道。

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 