---
description: 指定制造商名稱的當地語系化版本。
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: manufacturerLS 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea756e9c2a55c9bc062b6ddd8566ea5443c6ed80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974387"
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



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




