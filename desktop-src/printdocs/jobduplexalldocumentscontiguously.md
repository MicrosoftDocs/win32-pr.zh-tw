---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c14e9c536d0ab24fafe308a8b11fa769842aab
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106993805"
---
# <a name="jobduplexalldocumentscontiguously"></a>JobDuplexAllDocumentsContiguously

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述輸出的雙工特性。 雙工功能可在媒體的兩端進行列印。 作業中的所有檔都會連續 duplexed 在一起。 JobDuplexAllDocumentsContiguously 和 DocumentDuplex 互斥。 驅動程式會決定這些關鍵字之間的條件約束處理。

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



| Name                       |                    |
|----------------------------|--------------------|
| 項目類型 <br/>   | 功能<br/> |
| 範圍前置詞 <br/> | 工作 (Job)<br/>     |
| 注意 <br/>          | None<br/>    |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| Name                               | 資料類型         | 單位                  | 支援的值                                                                                                                                                             | 總結                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| \_選項名稱\_<br/>          | 字串<br/> | 字元<br/> | 由定義的有效完整名稱 https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname 。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                                                                                     |
| \_IdentityOptionValue\_<br/> | 字串<br/> | n/a<br/>        | True、False。<br/>                                                                                                                                                      | 定義選項，當選取此選項時，會停用此功能。<br/>                                                           |
| \_DuplexModeValue\_<br/>     | 字串<br/> | n/a<br/>        | 自動、手動。<br/>                                                                                                                                                | 定義雙工模式。 自動雙工是由硬體執行。 手動雙工是由軟體和使用者執行。<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




