---
description: 針對埠類型作業產生 proxy 函式的實作為宣告。
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: functionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192912"
---
# <a name="functiondeclarations-element"></a>functionDeclarations 元素

針對埠類型作業產生 proxy 函式的實作為宣告。

## <a name="usage"></a>使用方式

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | 指定產生的 proxy 函數中是否包含非同步作業。<br/> <br/>         |
| [**事件**](events.md)<br/>       | 指定產生的函數中是否包含相關事件。<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | 指定產生的函式中是否包含用來傳遞錯誤資訊的參數。<br/> <br/> |
| [**操作**](operation.md)<br/> | 指定要產生程式碼的作業。<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | 指定要產生程式碼的埠類型。<br/> <br/>                                       |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="remarks"></a>備註

這個元素會產生對應至合約所呼叫之作業的成員函式宣告。 這些宣告的格式適合 c + + 編譯器取用，通常用於 .cpp 檔案中。

範例：

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




