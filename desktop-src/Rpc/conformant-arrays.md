---
title: 符合標準的陣列
description: 一致性陣列的大小在每次用戶端傳遞至伺服器上的遠端程式時，可能會有所不同或符合。
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19766b7b9552bcab08a4d194629892e51d5185ed39b0bedddbaef32f08cececf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073428"
---
# <a name="conformant-arrays"></a>符合標準的陣列

一致性陣列的大小在每次用戶端傳遞至伺服器上的遠端程式時，可能會有所不同或符合。 應用程式的 MIDL 檔案中的介面定義，可讓用戶端在每次叫用遠端程式時，指定陣列的大小。 在 \[ \] 陣列定義中使用空的方括弧 () 或星號 (\[ \* \]) 以表示符合標準的陣列。

下列範例會在 MIDL 檔案的介面中包含遠端程式的定義。 用戶端會指定由參數 *arraySize* 傳遞給伺服器的陣列大小。

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

介面定義會使用 MIDL 屬性 \[ [**大小 \_ ，**](/windows/desktop/Midl/size-is) \] 來指定用戶端傳遞至伺服器的陣列大小。 如果您想要指出陣列索引編號的最大值，請改用 \[ [**max \_ 為**](/windows/desktop/Midl/max-is) \] 屬性。 如需有關這些 MIDL 屬性的詳細資訊，請參閱 [陣列屬性](array-attributes.md)。

下列程式碼片段說明用戶端可能如何叫用先前 MIDL 檔案中定義的遠端程式。


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



此片段會呼叫遠端過程 MyRemoteProc 兩次。 在第一次叫用時，它會傳遞20個元素的陣列。 第二次呼叫時，用戶端會傳遞200個元素的陣列。

 

 