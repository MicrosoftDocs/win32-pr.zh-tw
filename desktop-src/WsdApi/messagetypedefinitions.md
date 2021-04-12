---
description: 針對訊息類型產生 XML 架構資料表的 C 常數。
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: messageTypeDefinitions 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f86043cc28b527778c91772ad731d3a271921f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192171"
---
# <a name="messagetypedefinitions-element"></a>messageTypeDefinitions 元素

針對訊息類型產生 XML 架構資料表的 C 常數。

## <a name="usage"></a>使用方式

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                   | 描述                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**操作**](operation.md)<br/> | 指定要產生程式碼的作業。<br/> <br/>  |
| [**portType**](porttype.md)<br/>   | 指定要產生程式碼的埠類型。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**檔**](file.md)<br/> | 從程式碼產生器輸出檔案。<br/> <br/> |



## <a name="remarks"></a>備註

此元素通常用於 C 來源檔案，以提供 [**messageTypeDeclarations**](messagetypedeclarations.md)所宣告的架構資料表。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




