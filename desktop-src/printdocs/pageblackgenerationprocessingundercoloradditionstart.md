---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: 檢查 PageBlackGenerationProcessingUnderColorAdditionStart 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549346"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a>PageBlackGenerationProcessingUnderColorAdditionStart

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述將套用 UCA 的陰影層級。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|------------------------------------------------------------|
| 項目類型 <br/>   | ParameterDef<br/>                                    |
| 範圍前置詞 <br/> | 頁面<br/>                                            |
| 備註 <br/>          | 連結至 PageBlackGenerationProcessing 元素<br/> |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>結構屬性

下表概述 XML 結構中所定義之變數的特性。



| 屬性                | xsi:type           | 值                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | 字串<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | 字串<br/>  | 未定義<br/>       |
| MaxValue<br/>     | 整數<br/> | 100<br/>             |
| MinValue<br/>     | 整數<br/> | 0<br/>               |
| 多個<br/>     | 整數<br/> | 1<br/>               |
| 強制性<br/>    | string<br/>  | psk：條件式<br/> |
| Unittype.pixel 表示<br/>     | string<br/>  | percent<br/>         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




