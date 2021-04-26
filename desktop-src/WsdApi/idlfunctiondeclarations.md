---
description: 針對埠類型作業產生 proxy 函式的 IDL 宣告。
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: idlFunctionDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994735"
---
# <a name="idlfunctiondeclarations-element"></a>idlFunctionDeclarations 元素

針對埠類型作業產生 proxy 函式的 IDL 宣告。

## <a name="usage"></a>使用方式

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>         | 指定產生的 proxy 函數中是否包含非同步作業。<br/> <br/>         |
| [**eventArg**](eventarg.md)<br/>   | 指定產生的函數中是否包含相關的事件引數。<br/> <br/>               |
| [**事件**](events.md)<br/>       | 指定產生的函數中是否包含相關事件。<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/> | 指定產生的函式中是否包含用來傳遞錯誤資訊的參數。<br/> <br/> |
| [**操作**](operation.md)<br/> | 指定要產生程式碼的作業。<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>   | 指定要產生程式碼的埠類型。<br/> <br/>                                       |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
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

這個元素會產生對應至合約所呼叫之作業的成員函式宣告。 這些宣告的格式適合 MIDL 編譯器取用，而且通常會在 .idl 檔中使用。

範例：

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




