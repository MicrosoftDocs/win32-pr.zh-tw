---
title: 不同陣列
description: 在 MIDL 中，不同陣列的大小是固定的。 它們可讓用戶端將不同的陣列部分從用戶端傳遞至伺服器。 陣列部分的大小可能會因調用而異。 但是，整體陣列的大小是固定的。
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463525"
---
# <a name="varying-arrays"></a>不同陣列

在 MIDL 中，不同陣列的大小是固定的。 它們可讓用戶端將不同的陣列部分從用戶端傳遞至伺服器。 陣列部分的大小可能會因調用而異。 但是，整體陣列的大小是固定的。

例如，下列範例顯示 MIDL 檔案介面中的遠端程式定義。 用戶端傳遞至伺服器的陣列大小是由常數陣列大小來修正 \_ 。 介面會指定用戶端在參數 firstElement 和 chunkSize 中傳遞給伺服器之陣列的部分。

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

介面定義 \[ [**\_ 會先**](/windows/desktop/Midl/first-is)使用 MIDL 屬性， \] 來指定用戶端傳遞至伺服器之陣列部分中第一個元素的索引編號。 [ \[ [**長度] \_ 是**](/windows/desktop/Midl/length-is) \] [屬性] 指定用戶端傳遞的陣列元素總數。 如需有關這些 MIDL 屬性的詳細資訊，請參閱 [陣列屬性](array-attributes.md)。

下列程式碼片段說明用戶端可能如何叫用先前 MIDL 檔案中定義的遠端程式。


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



此片段會呼叫遠端過程 MyRemoteProc 兩次。 在第一次叫用時，它會傳遞編號為20到119的陣列元素，如變數 firstArrayElementNumber 和 totalElementsPassed 中的值所示。 第二次呼叫時，用戶端會傳遞編號為120到319的陣列元素。

 

 