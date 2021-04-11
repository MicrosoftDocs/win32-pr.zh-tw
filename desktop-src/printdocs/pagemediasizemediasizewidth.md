---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321691"
---
# <a name="pagemediasizemediasizewidth"></a>PageMediaSizeMediaSizeWidth

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

指定自訂 MediaSize 選項的維度 MediaSizeWidth 方向。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| Name                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| 項目類型 <br/>   | ParameterDef<br/>                                   |
| 範圍前置詞 <br/> | 頁面<br/>                                           |
| 備註 <br/>          | 連結至 PageMediaSize 元素，自訂選項<br/> |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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



| 屬性                | xsi:type           | 值                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | 字串<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | 整數<br/> | 未定義<br/>       |
| MaxValue<br/>     | 整數<br/> | 未定義<br/>       |
| MinValue<br/>     | 整數<br/> | 未定義<br/>       |
| 強制性<br/>    | 字串<br/>  | psk：條件式<br/> |
| 多個<br/>     | 整數<br/> | 1<br/>               |
| Unittype.pixel 表示<br/>     | 字串<br/>  | 微米<br/>         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




