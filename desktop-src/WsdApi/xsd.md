---
description: 指定要針對合約資訊處理的 XSD 檔案。
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: xsd 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994545"
---
# <a name="xsd-element"></a>xsd 元素

指定要針對合約資訊處理的 XSD 檔案。

## <a name="usage"></a>使用方式

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a>屬性



| 屬性           | 類型                       | 必要       | 描述                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| **path**<br/> | pathname 字串<br/> | Yes<br/> | XSD 輸入檔的檔案和路徑。<br/> <br/> |



## <a name="child-elements"></a>子元素



| 元素                               | 描述                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [**typeUri**](typeuri.md)<br/> | 指定要包含在 XSD 檔案中的類型。<br/> <br/> |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
typeUri*
```

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

檔案名字串也應該包含完整的路徑資訊。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




