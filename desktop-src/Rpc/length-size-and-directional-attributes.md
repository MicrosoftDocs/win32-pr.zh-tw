---
title: 長度、大小和方向屬性
description: 在用戶端和伺服器之間傳遞陣列時，與大小相關的屬性 \ max \_ 是 \，而 \ 大小 \_ 是 \ 判斷伺服器 stub 配置多少陣列元素。
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91424a93a53fe710c945011d19f8f97dc0f65e4899bc3305be5725d5a08e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020129"
---
# <a name="length-size-and-directional-attributes"></a>長度、大小和方向屬性

在用戶端和伺服器之間傳遞陣列時，大小相關屬性 \[ [**最大值 \_ 為**](/windows/desktop/Midl/max-is) \] ，而 \[ [**大小 \_ 則是**](/windows/desktop/Midl/size-is) \] 決定伺服器 stub 配置多少陣列元素。 長度相關的屬性 \[ [**長度 \_ 為**](/windows/desktop/Midl/length-is) \] ， \[ [**第一個 \_ 是**](/windows/desktop/Midl/first-is) \] ，而 \[ [**最後一個則 \_ 是**](/windows/desktop/Midl/last-is) \] 決定要將多少專案傳送至伺服器和用戶端。

不同的方向屬性可以套用至參數。 不過，某些方向屬性組合可能會造成錯誤。 例如，假設您要撰寫的介面指定具有兩個參數的程式、陣列，以及陣列的傳輸長度。 *Dir \_ attr* 一詞是指套用至參數的方向屬性，如下所示：

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

下表說明每個方向屬性組合的 MIDL 編譯器行為。



| Array                                          | Length 參數                               | 從用戶端到伺服器的呼叫期間的存根動作                                                                                                                                                                                                                          | 從伺服器回到用戶端時的存根動作                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**在**](/windows/desktop/Midl/in)\]                          | \[[**在**](/windows/desktop/Midl/in)\]                          | 傳輸參數所指示的長度和元素數目。                                                                                                                                                                                              | 未傳送任何資料。                                                                                                                                                                                                 |
| \[[**在**](/windows/desktop/Midl/in)\]                          | \[[**擴展**](/windows/desktop/Midl/out-idl)\]                    | 不合法;MIDL 編譯器錯誤。                                                                                                                                                                                                                                         | 不合法;MIDL 編譯器錯誤。                                                                                                                                                                                      |
| \[[**在**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in)、 [ **out**](/windows/desktop/Midl/out-idl)\] | 傳送 length 參數所指示的長度和元素數。                                                                                                                                                                                       | 只傳輸長度。                                                                                                                                                                                            |
| \[[**擴展**](/windows/desktop/Midl/out-idl)\]                    | \[[**在**](/windows/desktop/Midl/in)\]                          | 傳輸長度。<br/> 如果陣列大小是固定的，請在伺服器上配置陣列大小，但不傳輸任何元素。<br/> 如果陣列大小未系結，則不是合法： MIDL 編譯器錯誤。<br/>                                                              | 傳輸長度所指出的元素數目。<br/> 請注意，您可以變更長度，而且在用戶端上的值可以有不同的值。 請勿傳輸長度。<br/>          |
| \[[**擴展**](/windows/desktop/Midl/out-idl)\]                    | \[[**擴展**](/windows/desktop/Midl/out-idl)\]                    | 在伺服器上配置長度參數的空間，但不傳輸參數。 如果陣列大小是固定的，請在伺服器上配置陣列大小，但不傳輸任何專案。<br/> 如果陣列大小不是固定的，則不是合法： MIDL 編譯器錯誤。<br/> | 傳輸由伺服器應用程式所設定的長度所指定的專案長度和元素數目。                                                                                                             |
| \[[**擴展**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in)、 [ **out**](/windows/desktop/Midl/out-idl)\] | 傳輸長度參數。 如果陣列大小已系結，請在伺服器上配置陣列大小，但不傳輸任何元素。<br/> 如果陣列大小未系結，則不是合法： MIDL 編譯器錯誤。<br/>                                                           | 傳輸長度。 傳輸長度所指出的陣列元素數目。<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in)、 [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**在**](/windows/desktop/Midl/in)\]                          | 傳輸參數所指示的長度和元素數目。                                                                                                                                                                                              | 請勿傳輸長度。 傳輸長度所指出的元素數目。<br/> 請注意，長度可以變更，而且在用戶端上的原始值可以有不同的值。<br/> |
| \[[**in**](/windows/desktop/Midl/in)、 [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**擴展**](/windows/desktop/Midl/out-idl)\]                    | 不合法;MIDL 編譯器錯誤。                                                                                                                                                                                                                                         | 不合法;MIDL 編譯器錯誤。                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in)、 [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in)、 [ **out**](/windows/desktop/Midl/out-idl)\] | 傳輸參數所指示的長度和元素數目。                                                                                                                                                                                              | 傳輸參數所指示的長度和元素數目。                                                                                                                                           |



 

一般而言，您不應該在伺服器端修改長度或大小參數。 如果您變更長度參數，則可以是孤立的記憶體。 如需詳細資訊，請參閱 [記憶體損壞](memory-orphaning.md)。

 

