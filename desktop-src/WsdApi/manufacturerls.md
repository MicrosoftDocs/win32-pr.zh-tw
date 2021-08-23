---
description: 指定制造商名稱的當地語系化版本。
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: manufacturerLS 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5b6922e0d914048003b976ecf1f9a7b82febc2a9802334f1a125e357985e319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794028"
---
# <a name="manufacturerls-element"></a>manufacturerLS 元素

指定制造商名稱的當地語系化版本。

## <a name="usage"></a>使用方式

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a>屬性



| 屬性               | 類型                                          | 必要       | 描述                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| **資料**<br/>     | 當地語系化的製造商名稱字串<br/> | Yes<br/> | 當地語系化的製造商名稱。<br/> <br/>                 |
| **Language**<br/> | 語言識別項字串<br/>         | Yes<br/> | 當地語系化製造商名稱的語言。<br/> <br/> |



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                   | 描述                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | 定義要執行之裝置的製造商和型號中繼資料。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




