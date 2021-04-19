---
description: 針對埠類型作業產生存根函式的實作為。
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: stubDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980307"
---
# <a name="stubdefinitions-element"></a>stubDefinitions 元素

針對埠類型作業產生存根函式的實作為。

## <a name="usage"></a>使用方式

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                         | 描述                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**釋放器**](deallocator.md)<br/>                   | 指定存根函式所要使用的釋放器類型。<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | 指定產生的函數中是否包含相關的事件引數。<br/> <br/>               |
| [**事件**](events.md)<br/>                             | 指定產生的函數中是否包含相關事件。<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | 指定產生的函式中是否包含用來傳遞錯誤資訊的參數。<br/> <br/> |
| [**操作**](operation.md)<br/>                       | 指定要產生程式碼的作業。<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | 指定作業的存根函數所要使用的釋放器類型。<br/> <br/>                    |
| [**portType**](porttype.md)<br/>                         | 指定要產生程式碼的埠類型。<br/> <br/>                                       |
| [**serverClass**](serverclass.md)<br/>                   | 指定主機端伺服器類別的名稱。<br/> <br/>                                                |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




