---
description: 指定裝置名稱的當地語系化版本。
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: modelNameLS 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995495"
---
# <a name="modelnamels-element"></a>modelNameLS 元素

指定裝置名稱的當地語系化版本。

## <a name="usage"></a>使用方式

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a>屬性



| 屬性               | 類型                                   | 必要       | 描述                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| **資料**<br/>     | 當地語系化的模型名稱字串<br/> | Yes<br/> | 當地語系化的模型名稱。<br/> <br/>                 |
| **Language**<br/> | 語言識別項字串<br/>  | Yes<br/> | 當地語系化模型名稱的語言。<br/> <br/> |



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



 

 




