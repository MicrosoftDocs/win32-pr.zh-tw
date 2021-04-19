---
description: 指定要針對合約資訊處理的 WSDL 檔案。
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: wsdl 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcb96e063a289e16d5e459b59cb8808a763618a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380732"
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



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 否            |



 

 




