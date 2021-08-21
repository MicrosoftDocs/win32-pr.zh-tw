---
title: 方向 (參數) 屬性
description: 方向屬性描述資料是從用戶端傳送到伺服器、伺服器到用戶端，還是從兩者傳送。
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- 遠端程序呼叫 RPC、描述的方向屬性
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e9ff23e7e12acbd5cf301afe6786599268d2e149878a326a62f79cd91f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930637"
---
# <a name="directional-parameter-attributes"></a>方向 (參數) 屬性

方向屬性描述資料是從用戶端傳送到伺服器、伺服器到用戶端，還是從兩者傳送。 函數原型中的所有參數都必須與方向屬性相關聯。 有三種可能的方向屬性組合： 1) \[ [**in**](/windows/desktop/Midl/in)、 \] 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] 和 3) \[ **in**、 **out** \] 。 這些描述在呼叫和呼叫程式之間傳遞參數的方式。 當您在預設的 (Microsoft 擴充模式) 中進行編譯時，會省略參數的方向屬性，MIDL 編譯器會假設的預設值為 \[  \] 。

\[ [**Out**](/windows/desktop/Midl/out-idl) \] 參數必須是指標。 事實上， \[  \] 因為 C 函式參數是以傳值方式傳遞，所以 out 屬性在套用至不做為指標的參數時沒有意義。 在 C 中，被呼叫的函式會收到參數值的私用複本。它無法變更該參數的呼叫函數值。 但是，如果參數做為指標，則可以用來存取和修改記憶體。 \[ **Out** \] 屬性工作表示伺服器函式應該將值傳回給用戶端的呼叫函式，而且應該根據指派給指標的屬性，傳回與指標相關聯的記憶體。

下列介面示範三種可能適用于參數的方向屬性組合。 函數 **InOutProc** 定義于 IDL 檔案中，如下所示：

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

第一個參數 *s1* 是唯一的 \[ [](/windows/desktop/Midl/in) \] 。 它的值會傳送到遠端電腦，但不會傳回給呼叫程式。 雖然伺服器應用程式可以變更 *s1* 的值，但用戶端上的 *s1* 值在呼叫前後都相同。

第二個參數（ *ps2*）在函式原型中定義為具有 \[ [**in**](/windows/desktop/Midl/in) \] 和 \[ [**out**](/windows/desktop/Midl/out-idl) \] 屬性的指標。 \[ **In** \] 屬性工作表示參數的值會從用戶端傳遞至伺服器。 \[ **Out** \] 屬性工作表示 *ps2* 所指向的值會傳回給用戶端。

第三個參數 \[ 只是 [**out**](/windows/desktop/Midl/out-idl) \] 。 在伺服器上配置參數的空間，但輸入時未定義此值。 如先前所述，所有 \[ **out** \] 參數都必須是指標。

遠端程式會變更這三個參數的值，但只有 \[ [**out**](/windows/desktop/Midl/out-idl) \] 和 in 參數的新值 \[ [](/windows/desktop/Midl/in) \] 可供用戶端使用。


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



從呼叫 **InOutProc** 時，會修改第二個和第三個參數。 第一個參數（唯一的參數） \[ [](/windows/desktop/Midl/in) \] 不會變更。

![in 參數](images/prog-a22.png)

![out 參數](images/prog-a23.png)

![out 參數](images/prog-a21.png)

 

 