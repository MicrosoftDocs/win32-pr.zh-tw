---
description: 深入瞭解 JobNUpAllDocumentsContiguously 元素，其描述多個邏輯頁面至單一實體工作表的輸出。
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef26a28d970d135419a89015761fa33369a2147edd05712ad7671e881aef2c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353591"
---
# <a name="jobnupalldocumentscontiguously"></a>JobNUpAllDocumentsContiguously

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述多個邏輯頁面至單一實體工作表的輸出。 作業中的所有檔都會連續編譯。 JobNUpAllDocumentsContiguously 和 DocumentNUp 互斥。 驅動程式會決定這些關鍵字之間的條件約束處理。

下圖說明含有3個頁面的檔1的範例，以及包含2個頁面的檔2。 作業中的每份檔都會連續 duplexed。 範例中顯示的呈現方向是 RightBottom 選項。

![顯示如何根據 documentnup 設定在單一工作表上設定檔頁面面的圖表](images/local-1242234459-jobduplexpics.gif)

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



| 名稱 | 值 |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目類型 <br/>   | 功能<br/>                                                                                                                             |
| 範圍前置詞 <br/> | 工作 (Job)<br/>                                                                                                                                 |
| 附註 <br/>          | 頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表由高度和寬度的原點表示。<br/> |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
      
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| 名稱                                           | 資料類型          | 單位                     | 支援的值                                                                                                                                                                      | 總結                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_選項名稱\_<br/>                      | string<br/>  | 字元<br/>    | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | string<br/>  | n/a<br/>           | True、False。<br/>                                                                                                                                                               | 定義選項，當選取此選項時，會停用此功能。<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | 整數<br/> | 邏輯頁面<br/> | 所有整數 (大於零) 。<br/>                                                                                                                                          | 指定每個實體工作表的邏輯頁面數目。 支援的集合可以是任何一組整數，例如 {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | string<br/>  | 字元<br/>    | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




