---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 6f99f54b-c401-42ea-8715-95a2aad73042
title: PageMediaSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbaef403027190676b57455aa460198c2868424
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995517"
---
# <a name="pagemediasize"></a>PageMediaSize

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述用於輸出的實體媒體維度。

下圖說明 PageMediaSize 變數使用量 (選項 ISOA4 作為範例) 使用。

![顯示頁面維度的圖表](images/local-1594393517-pagemediasizepic.gif)

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



|                            |                    |
|----------------------------|--------------------|
| Name | 值 |
| 項目類型 <br/>   | 功能<br/> |
| 範圍前置詞 <br/> | 頁面<br/>    |
| 注意 <br/>          | None<br/>    |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">_MediaSizeWidth_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">_MediaSizeHeight_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| Name                                | 資料類型          | 單位                  | 支援的值                                                                                                                                                                      | 總結                                                                                                                                                                   |
|-------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_選項名稱\_<br/>           | 字串<br/>  | 字元<br/> | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 指定媒體的名稱。 命名應使用下列慣例： " \_ OptionNameStandard \_ " " \_ OptionNameCommonName \_ " " \_ OptionNameDescriptor \_ "。<br/> |
| \_IdentityOptionValue\_<br/>  | 字串<br/>  | n/a<br/>        | True、False。<br/>                                                                                                                                                               | 定義選項，當選取此選項時，會停用此功能。<br/>                                                                                              |
| \_OptionNameStandard\_<br/>   | 字串<br/>  | 字元<br/> | 「ISO」、「JIS」、「日本」、「北美洲」、「OtherMetric」、「中國」、「無」。<br/>                                                                                                         | 指出媒體大小是否由特定標準定義。<br/>                                                                                               |
| \_OptionNameCommonName\_<br/> | 字串<br/>  | 字元<br/> | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 媒體大小的一般名稱。<br/>                                                                                                                                |
| \_OptionNameDescriptor\_<br/> | 字串<br/>  | 字元<br/> | 大型、信封、額外的加號、明信片、旋轉、紙、' none '。<br/>                                                                                                              | 大型、信封、額外的加號、明信片、旋轉、紙、' none '。<br/>                                                                                                  |
| \_MediaSizeWidth\_<br/>       | 整數<br/> | 微米<br/>    | 大於0，小於裝置的支援媒體大小上限。<br/>                                                                                                           | 指定實體媒體的寬度。<br/>                                                                                                                     |
| \_MediaSizeHeight\_<br/>      | 整數<br/> | 微米<br/>    | 大於0，小於裝置的支援媒體大小上限。<br/>                                                                                                           | 指定實體媒體的高度。<br/>                                                                                                                    |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom media size.  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:CustomMediaSize">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom media size (PostScript specific).  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:PSCustomMediaSize">
    <!-- Specifies the height of the page parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeight">
      <psf:ParameterRef name="psk:PageMediaSizePSHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the offset parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeightOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSHeightOffset" />
    </psf:ScoredProperty>
    <!-- Specifies the orientation relative to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSOrientation">
      <psf:ParameterRef name="psk:PageMediaSizePSOrientation" />
    </psf:ScoredProperty>
    <!-- Specifies the width of the page perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidth">
      <psf:ParameterRef name="psk:PageMediaSizePSWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the offset perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidthOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSWidthOffset" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1189000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">26000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">322000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">445000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235500</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">174000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1414000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">31000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">201000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">276000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">28000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6C5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOSRA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">320000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">450000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanQuadrupleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">296000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1456000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">32000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x14">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica11x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica9x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureASheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureBSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1219200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1117600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaExecutive">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">184150</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">266700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanLegalFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanStandardFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegal">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegalExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetter">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterPlus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322326</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaMonarchEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNote">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">225425</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber11Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">263525</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber12Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120650</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber14Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">292100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaPersonalEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">92075</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaQuarto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">275000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaStatement">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">139700</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperA">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">227000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">356000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperB">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">305000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">487000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloid">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloidExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">296926</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA4Plus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA3Plus">
    - <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">329000</psf:Value>
    </psf:ScoredProperty>
    - <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">483000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricFolio">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricInviteEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricItalianEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KBig">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Roll04Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll06Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">152400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll08Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll12Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll15Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll18Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll22Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll24Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll30Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">762000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll36Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll54Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1371600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanLPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">89000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Japan2LPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">178000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">152400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica5x7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica8x10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x12">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica14x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">355600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:BusinessCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">55000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CreditCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">54000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">86000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>   
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
