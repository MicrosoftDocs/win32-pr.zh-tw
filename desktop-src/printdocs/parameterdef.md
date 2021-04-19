---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981944"
---
# <a name="parameterdef"></a>ParameterDef

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

ParameterDef 元素會定義參數輸入的有效特性。 藉由 ParameterInit 元素來輸入值。

## <a name="element-tag"></a>元素標記

<ParameterDef>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性   | 詳細資料                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NAME<br/> | 在目前檔的內容中定義參數的唯一名稱。 重複的 ParameterDef 名稱屬性轉譯 PrintCapabilities 檔無效。<br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>類別</th>
<th>詳細資料</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>父元素<br/></td>
<td>PrintCapabilities <br/></td>
</tr>
<tr class="even">
<td>子元素<br/></td>
<td>屬性 (一個或多個)<br/> 下列標準屬性元素必須顯示為 ParameterDef 元素的內容。 <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>強制性 <br/></li>
<li>MaxLength 或 Timespan.maxvalue<br/></li>
<li>MinLength 或 MinValue<br/></li>
<li>名 <br/></li>
<li>Unittype.pixel 表示 <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>這個元素<br/></td>
<td>不允許任何字元資料。<br/> 不允許重複的子同級。<br/></td>
</tr>
</tbody>
</table>



 

\*當資料類型是整數或十進位時，則為必要項。 當 DataType 為 string 時為選擇性。

## <a name="configuration-dependencies"></a>設定相依性

ParameterDef 及其內容到任何嵌套層級都可能沒有任何設定相依性。

## <a name="example"></a>範例

下列範例會為此參數設定所有必要的屬性元素。 [ParameterInit](parameterinit.md)中的範例會示範如何初始化此參數。

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




