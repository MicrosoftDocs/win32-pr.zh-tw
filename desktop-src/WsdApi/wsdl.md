---
description: 指定要針對合約資訊處理的 WSDL 檔案。
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: wsdl 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158141fb8afdc216c47639f6bbb50c1d399e25f202ebbdd2f0a2c045859bffb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049516"
---
# <a name="wsdl-element"></a>wsdl 元素

指定要針對合約資訊處理的 WSDL 檔案。

## <a name="usage"></a>使用方式

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                           | 描述                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | 防止在 WSDL 檔案中的元素中，針對指定的目標產生 import 語句 \<wsdl:import> 。 <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | 指定 \<wsdl:import> 未明確指定位置之指示詞的下載位置。<br/> <br/>           |
| [**路徑**](path.md)<br/>                   | WSDL 輸入檔的檔案和路徑。<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>子項目順序

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>父元素



| 元素                                     | 描述                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | WSDAPI 程式碼產生器 XML 腳本檔的根項目。<br/> <br/> |



## <a name="remarks"></a>備註

在 XML 設定檔案中的 [**path**](path.md)元素後面出現的任何 [**importHint**](importhint.md)或 [**excludeImport**](excludeimport.md)元素都會被忽略。

## <a name="element-information"></a>項目資訊



| 標籤 | 值 |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




