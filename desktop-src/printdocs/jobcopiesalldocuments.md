---
description: 瞭解 JobCopiesAllDocuments 元素，它會指定作業的複本數目。
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409031"
---
# <a name="jobcopiesalldocuments"></a>JobCopiesAllDocuments

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

指定作業的複本數目。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|-------------------------|
| 項目類型 <br/>   | ParameterDef<br/> |
| 範圍前置詞 <br/> | 工作 (Job)<br/>          |
| 注意 <br/>          | None<br/>         |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>結構屬性

下表概述 XML 結構中所定義之變數的特性。



| 屬性                | xsi:type           | 值                        |
|-------------------------|--------------------|------------------------------|
| DataType<br/>     | 字串<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | 整數<br/> | 1<br/>                 |
| MaxValue<br/>     | 整數<br/> | 未定義<br/>         |
| MinValue<br/>     | 整數<br/> | 1<br/>                 |
| 強制性<br/>    | string<br/>  | psk：無條件<br/> |
| 多個<br/>     | 整數<br/> | 1<br/>                 |
| Unittype.pixel 表示<br/>     | string<br/>  | 副本<br/>            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




