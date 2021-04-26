---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995545"
---
# <a name="pagewatermarktextangle"></a>PageWatermarkTextAngle

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

指定浮水印文字相對於 PageImageableSizeWidth 方向的角度。 角度是以逆時針方向來測量。

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
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>結構屬性

下表概述 XML 結構中所定義之變數的特性。



| 屬性                | xsi:type           | 值                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | 字串<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | 整數<br/> | 0<br/>               |
| MaxValue<br/>     | 整數<br/> | 359<br/>             |
| MinValue<br/>     | 整數<br/> | 0<br/>               |
| 多個<br/>     | 整數<br/> | 1<br/>               |
| 強制性<br/>    | 字串<br/>  | psk：條件式<br/> |
| Unittype.pixel 表示<br/>     | 字串<br/>  | 度<br/>         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




