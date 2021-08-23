---
description: 閱讀 PageDeviceColorSpaceProfileURI 參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a979ed2bdabd9d31be44942de2a8fbe47119f2e27c77041b2410413d9e43ece6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554608"
---
# <a name="pagedevicecolorspaceprofileuri"></a>PageDeviceColorSpaceProfileURI

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

針對包含在 XPS 檔中的 ICC 設定檔，指定套件根目錄的相對 URI。 此選項的處理取決於 PageDeviceColorSpaceUsage 功能的設定。 使用該設定檔的所有元素都會假設已經在適當的裝置色彩空間中，而且不會在驅動程式或裝置中進行色彩管理。

-   [項目資訊](#element-information)
-   [結構內容](#structure-content)

## <a name="element-information"></a>項目資訊



| 名稱 | 值 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目類型 <br/>   | ParameterDef<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 範圍前置詞 <br/> | 頁面<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 備註 <br/>          | 這僅適用于 XPS 檔，不應該用於任意 PrintTickets。<br/> 符合 XPS 規範的取用者必須在列印功能檔或 PrintTicket 中，強制資源的 URI 參考（例如影像或色彩設定檔）必須參考元件名稱， (在包含結果 PrintTicket 的相同 XPS 檔封裝內的封裝根目錄) 的相對 URI。 相容的 XPS 取用者不能使用不符合元件名稱語法規范的 URI。 這些設定是 XPS 專用的。 <br/> 在列印功能檔或 PrintTicket 中參考的 Uri 不得解析為 Url。 這是不安全的，因為它們可能無法如預期地解決，而且可能會產生驅動程式和作業系統的有害安全性風險。<br/> |



 

## <a name="structure-content"></a>結構內容

此元素的 XML 結構為：

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
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
| 強制性<br/>    | 字串<br/>  | psk：條件式<br/> |
| Unittype.pixel 表示<br/>     | 字串<br/>  | 字元<br/>      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




