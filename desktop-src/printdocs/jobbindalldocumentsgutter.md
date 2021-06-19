---
description: 瞭解 JobBindAllDocumentsGutter 元素，它會指定系結裝訂邊的寬度。
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42180ff9a00d1502d844b270fe5da7324825ca3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409071"
---
# <a name="jobbindalldocumentsgutter"></a>JobBindAllDocumentsGutter

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

指定裝訂裝訂邊的寬度。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|-----------------------------------------|
| 項目類型 <br/>   | ParameterDef<br/>                 |
| 範圍前置詞 <br/> | 工作 (Job) <br/>                         |
| 備註 <br/>          | 連結至 JobBinding 元素<br/> |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
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
| 強制性<br/>    | String<br/>  | psk：條件式<br/> |
| 多個<br/>     | 整數<br/> | 1<br/>               |
| Unittype.pixel 表示<br/>     | string<br/>  | 微米<br/>         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




