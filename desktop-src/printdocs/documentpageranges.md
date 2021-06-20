---
description: 深入瞭解 DocumentPageRanges 元素，其描述頁面中檔的輸出範圍。
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409251"
---
# <a name="documentpageranges"></a>DocumentPageRanges

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述頁面中檔的輸出範圍。 參數值必須符合下列結構：

-   PageRangeText： "*PageRange*" 或 "*PageRange*，*PageRange*"

-   PageRange： "*PageNumber*" 或 "*PageNumber* - *PageNumber*"

-   PageNumber：1到 N，其中 N 是檔中的頁面數目。 如果 *PageNumber* > N，則 *PageNumber* = n。

應忽略字串中的空白字元。

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|-------------------------|
| 項目類型 <br/>   | ParameterDef<br/> |
| 範圍前置詞 <br/> | 文件<br/>     |
| 注意 <br/>          | None<br/>         |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>結構屬性

下表概述 XML 結構中所定義之變數的特性。



| 屬性                | xsi:type           | 值                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | 字串<br/>  | xs:string<br/>       |
| DefaultValue<br/> | 字串<br/>  | 未定義<br/>       |
| MaxLength<br/>    | 整數<br/> | 未定義<br/>       |
| MinLength<br/>    | 整數<br/> | 1<br/>               |
| 強制性<br/>    | string<br/>  | psk：條件式<br/> |
| Unittype.pixel 表示<br/>     | string<br/>  | 字元<br/>      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




