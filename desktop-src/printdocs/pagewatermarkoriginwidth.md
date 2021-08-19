---
description: 取得 PageWatermarkOriginWidth 參數的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57533d7d7322eedf586c86bfbfd28a82b9cc143aedd7c6318c6c1f6ecb36451f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731908"
---
# <a name="pagewatermarkoriginwidth"></a>PageWatermarkOriginWidth

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

指定相對於 PageImageableSize 原點的浮水印原點。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| 名稱 | 值 |
|----------------------------|--------------------------------------------|
| 項目類型 <br/>   | ParameterDef<br/>                    |
| 範圍前置詞 <br/> | 頁面<br/>                            |
| 備註 <br/>          | 連結至 PageWatermark 元素<br/> |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>結構屬性

下表概述 XML 結構中所定義之變數的特性。



| 屬性                | xsi:type           | 值                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| DataType<br/>     | 字串<br/>  | xs:integer<br/>                                                  |
| DefaultValue<br/> | 整數<br/> | 未定義<br/>                                                   |
| MaxValue<br/>     | 整數<br/> | 小於或等於 PageImageableSize-System.windows.controls.primitives.iscrollinfo.extentwidth 值<br/> |
| MinValue<br/>     | 整數<br/> | 0<br/>                                                           |
| 多個<br/>     | 整數<br/> | 1<br/>                                                           |
| 強制性<br/>    | 字串<br/>  | psk：條件式<br/>                                             |
| Unittype.pixel 表示<br/>     | 字串<br/>  | 微米<br/>                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




