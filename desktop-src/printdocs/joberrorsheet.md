---
description: 瞭解 JobErrorSheet 元素，其描述錯誤表輸出。 整個作業將會有一個錯誤工作表。
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5489e83ec866da1a8c8ead4b237bcb1ea8ca660363fad9b902271af8db04874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686460"
---
# <a name="joberrorsheet"></a>JobErrorSheet

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述錯誤表輸出。 整個作業將會有一個錯誤工作表。 錯誤工作表應該會輸出在預設 PageMediaSize 上，並使用預設 PageMediaType。 錯誤工作表應該與作業的其餘部分隔離。 這表示任何精加工或處理選項 (例如 JobDuplex、JobStaple 或 JobBinding) 都不應包含錯誤工作表。 錯誤工作表應該會以工作的最終工作表的形式出現。

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



| 名稱 | 值 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目類型 <br/>   | 功能<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 範圍前置詞 <br/> | 工作 (Job)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 備註 <br/>          | 符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。 相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。 這些設定是 XPS 專用的。 <br/> 在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。 這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。<br/> |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| 名稱                                             | 資料類型         | 單位                  | 支援的值                                                                                                                                                                      | 摘要                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_ErrorSheetWhenOptionName\_<br/>          | 字串<br/> | 字元<br/> | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                           |
| \_ErrorSheetWhenIdentityOptionValue\_<br/> | 字串<br/> | n/a<br/>        | True、False。<br/>                                                                                                                                                               | 定義使用者介面 (UI) 選取準則。<br/>               |
| \_選項名稱\_<br/>                        | 字串<br/> | n/a<br/>        | 由定義的有效完整名稱 https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname 。 如果未指定命名空間，則會假設為預設命名空間。<br/>          | 選項的名稱。<br/>                                           |
| \_IdentityOptionValue\_<br/>               | 字串<br/> | n/a<br/>        | True、False。<br/>                                                                                                                                                               | 定義選項，當選取此選項時，會停用此功能。<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




