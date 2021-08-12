---
description: 針對埠類型作業產生 proxy 函式的執行。
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: proxyFunctionImplementations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d64ae53d76100e5d38e1dd1a363f64a1004284b6f8a35ce5eb4e49d6d1e9a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552427"
---
# <a name="proxyfunctionimplementations-element"></a>proxyFunctionImplementations 元素

針對埠類型作業產生 proxy 函式的執行。

## <a name="usage"></a>使用量

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                     | 描述                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>           | 指定產生的 proxy 函數中是否包含非同步作業。<br/> <br/>         |
| [**事件**](events.md)<br/>         | 指定產生的函數中是否包含相關事件。<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | 指定產生的函式中是否包含用來傳遞錯誤資訊的參數。<br/> <br/> |
| [**操作**](operation.md)<br/>   | 指定要產生程式碼的作業。<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>     | 指定要產生程式碼的埠類型。<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | 指定用戶端 proxy 類別的名稱。<br/> <br/>                                               |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




