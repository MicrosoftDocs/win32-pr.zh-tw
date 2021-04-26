---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7d3ba5b55ece6d7237846ae8ef969c0a3d17e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998355"
---
# <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

描述輸出的排序特性。 每個個別工作中的所有檔都會進行定序。 DocumentCollate 和 JobCollateAlldocuments 互斥。 無論是否已執行這兩個關鍵字的行為和執行，都是由驅動程式所決定。

以下是進行 Collate 執行時應遵循的規則。

## <a name="element-definition-and-rules"></a>元素定義和規則

您必須先遵循 JobCollateAllDocument 的規則，然後套用適用于 DocumentCollate 的規則，才能讓案例運作。 請注意，在「PrintTicket 至 Devmode」轉換設定中（此驅動程式不支援 JobCollateAllDocuments），會由驅動程式選擇適當的行為來採取 (JobCollateAllDocuments = ON 或 OFF) 。 此外，您也可以根據其他的 PrintTicket 設定來變更選擇。

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

ON：列印 (DocumentCopiesAllPages) 每份檔的複本，重複 JobCopiesAllDocuments 時間。

OFF：對於每份檔，列印 (JobCopiesAllDocuments x DocumentCopiesAllPages) 會一起複製。

### <a name="documentcollate"></a>DocumentCollate

ON：適用于所有複本 (JobCopiesAllDocuments x) DocumentCopiesAllPages 檔中連續列印的檔，該檔中的分頁表。

OFF：針對 (JobCopiesAllDocuments x DocumentCopiesAllPages 的所有複本，) 連續列印，將每個工作表 (JobCopiesAllDocuments x DocumentCopiesAllPages) 的所有複本一起列印。

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

### <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|--------------------|
| 項目類型 <br/>   | 功能<br/> |
| 範圍前置詞 <br/> | 工作 (Job)<br/>     |
| 注意 <br/>          | None<br/>    |



 

### <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
  <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

### <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| Name                               | 資料類型         | 單位                  | 支援的值                                                                                                                                                                      | 總結                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_選項名稱\_<br/>          | 字串<br/> | 字元<br/> | 以 [XML 命名空間](https://www.w3.org/TR/1999/REC-xml-names-19990114/)所定義的有效完整名稱。 如果未指定命名空間，則會假設為預設命名空間。<br/> | 選項的名稱。<br/>                                           |
| \_IdentityOptionValue\_<br/> | 字串<br/> | n/a<br/>        | True、False。<br/>                                                                                                                                                               | 定義選項，當選取此選項時，會停用此功能。<br/> |



 

### <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




