---
description: 指定要包含在 XSD 檔案中的類型。
ms.assetid: dd3894a8-1848-4ae0-ba6c-42ac4fe36ff3
title: typeUri 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b746a8e301d6d76e0b6dc977c1595778663c8e20860f321fd0f6c8e61980b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611548"
---
# <a name="typeuri-element"></a>typeUri 元素

指定要包含在 XSD 檔案中的類型。

## <a name="usage"></a>使用方式

``` syntax
<typeUri
  type = "character_string"
  uri = "character_string"/>
```

## <a name="attributes"></a>屬性



| 屬性           | 類型                         | 必要       | 描述                                                            |
|---------------------|------------------------------|----------------|------------------------------------------------------------------------|
| **type**<br/> | 字元 \_ 字串<br/> | Yes<br/> | 型別的名稱。<br/> <br/>                           |
| **uri**<br/>  | 字元 \_ 字串<br/> | Yes<br/> | 型別的命名空間。 必須是有效的 URI。<br/> <br/> |



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                       | 描述                                                                       |
|-------------------------------|-----------------------------------------------------------------------------------|
| [**Xsd**](xsd.md)<br/> | 指定要針對合約資訊處理的 XSD 檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




