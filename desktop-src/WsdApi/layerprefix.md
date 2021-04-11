---
description: 定義要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: layerPrefix 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b712edee4b33c7158280b9d310624371fd58688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115024"
---
# <a name="layerprefix-element"></a>layerPrefix 元素

定義要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。

## <a name="usage"></a>使用方式

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

每個程式碼產生器腳本都應該為所建立的模組定義唯一的前置詞字串。 例如，圖片框架腳本會使用 "PFDEMO" 的前置詞。

WSDAPI 使用 "WSD" 前置詞。

## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




