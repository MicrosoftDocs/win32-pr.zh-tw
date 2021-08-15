---
description: 深入瞭解 DocumentCoverFront 使用者可設定的元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2552ec33acce2d86af824450bdd9c38de8763ab21d7c6202d9b3da646efda78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732928"
---
# <a name="documentcoverfront"></a>DocumentCoverFront

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述) 封面頁開始 (。 每份檔都有個別的工作表。 在檔的第一頁所使用的 PageMediaSize 和 PageMediaType 上，應該列印封面表。 封面工作表應該整合至處理選項 (例如 DocumentDuplex、DocumentNUp) ，如指定的選項所指定。

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目類型 <br/>   | 功能<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 範圍前置詞 <br/> | 文件<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 備註 <br/>          | 符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。 相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。 這些設定是 XPS 專用的。 <br/> 在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。 這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。<br/> |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| Name                               | 資料類型         | 單位                  | 支援的值                                                                                                                                                                      | 摘要                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_選項名稱\_<br/>          | string<br/> | 字元<br/> | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/a<br/>        | True、False。<br/>                                                                                                                                                               | 定義選項，當選取此選項時，會停用此功能。<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




