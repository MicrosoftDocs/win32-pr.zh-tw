---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996885"
---
# <a name="pagewatermarktextcolor"></a>PageWatermarkTextColor

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

定義浮水印文字的 sRGB 色彩。 格式為 ARGB： \# AARRGGBB。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|--------------------------------------------|
| 項目類型 <br/>   | ParameterDef<br/>                    |
| 範圍前置詞 <br/> | 頁面<br/>                            |
| 備註 <br/>          | 連結至 PageWatermark 元素<br/> |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構如下所示：

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>結構屬性

下表概述 XML 結構中所定義之變數的特性。



| 屬性                | xsi:type           | 值                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | 字串<br/>  | xs:string<br/>       |
| DefaultValue<br/> | 整數<br/> | 未定義<br/>       |
| MaxValue<br/>     | 整數<br/> | 未定義<br/>       |
| MinValue<br/>     | 整數<br/> | 未定義<br/>       |
| 強制性<br/>    | 字串<br/>  | psk：條件式<br/> |
| Unittype.pixel 表示<br/>     | 字串<br/>  | sRGB<br/>            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




