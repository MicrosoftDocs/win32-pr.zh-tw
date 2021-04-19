---
description: 針對埠類型作業產生存根函式的宣告。
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: stubDeclarations 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985153"
---
# <a name="stubdeclarations-element"></a>stubDeclarations 元素

針對埠類型作業產生存根函式的宣告。

## <a name="usage"></a>使用方式

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**事件**](events.md)<br/>       | 指定產生的函數中是否包含相關事件。<br/> <br/> |
| [**操作**](operation.md)<br/> | 指定要產生程式碼的作業。<br/> <br/>                 |
| [**portType**](porttype.md)<br/>   | 指定要產生程式碼的埠類型。<br/> <br/>                |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*, 
  events?
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
| 可以是空的                        | 是           |



 

 




