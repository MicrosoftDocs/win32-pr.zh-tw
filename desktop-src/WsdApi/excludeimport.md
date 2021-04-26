---
description: 防止針對 WSDL 檔中 wsdl： import 專案所命名的指定目標產生 import 語句。
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995875"
---
# <a name="excludeimport-element"></a>excludeImport 元素

防止在 WSDL 檔案中的元素中，針對指定的目標產生 import 語句 \<wsdl:import> 。 這可以用來防止 WsdCodeGen 匯入已知的目標，例如 WS-Addressing 和 WS-Eventing 的規格，即使 WSDL 中參考了這些目標也是一樣。

這個元素的值必須設定為要排除的元素中所指定的命名空間 \<wsdl:import> 。

## <a name="usage"></a>使用方式

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                         | 描述                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | 指定要針對合約資訊處理的 WSDL 檔案。<br/> <br/> |



## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




