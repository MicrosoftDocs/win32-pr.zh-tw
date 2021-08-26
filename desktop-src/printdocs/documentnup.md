---
description: 深入瞭解 DocumentNUp 元素，其描述單一實體工作表的多個邏輯頁面的輸出和格式。
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0804d38bdb60cd28ba88832b21abe8426d8aaf3b4fedf6ce5ad38f624f10c596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949721"
---
# <a name="documentnup"></a>DocumentNUp

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述單一實體工作表的多個邏輯頁面的輸出和格式。 每份檔都是分開編譯的。 DocumentNUp 和 JobNUpAllDocumentsContiguously 互斥。 驅動程式會決定這些關鍵字之間的條件約束處理。

下圖說明含有3個頁面的檔1的範例，以及包含2個頁面的檔2。 每份檔都是分開 duplexed。 以下顯示的呈現方向是 RightBottom 選項。

![顯示如何根據 documentnup 設定在單一工作表上設定檔頁面面的圖表](images/local-1663869164-docduplex1.gif)

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



| 名稱 | 值 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目類型 <br/>   | 功能<br/>                                                                                                                              |
| 範圍前置詞 <br/> | 文件<br/>                                                                                                                             |
| 備註 <br/>          | 頂端、底部、左方和右邊都是相對於 PageImageableSize，其中下拉式功能表是以 X 軸和 y 軸的原點表示。<br/> |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構如下所示：

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
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



| 名稱                                           | 資料類型          | 單位                     | 支援的值                                                                                                                                                                      | 摘要                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_選項名稱\_<br/>                      | 字串<br/>  | 字元<br/>    | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | 字串<br/>  | n/a<br/>           | True、False。<br/>                                                                                                                                                               | 定義選項，當選取此選項時，會停用此功能。<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | 整數<br/> | 邏輯頁面<br/> | 所有整數 (大於零) 。<br/>                                                                                                                                          | 指定每個實體工作表的邏輯頁面數目。 支援的集合可以是任何一組整數，例如 {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | 字串<br/>  | 字元<br/>    | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




