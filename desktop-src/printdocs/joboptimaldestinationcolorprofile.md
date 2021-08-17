---
description: 瞭解指定目前裝置設定的最佳色彩設定檔的 JobOptimalDestinationColorProfile 元素。
ms.assetid: 70790dc2-180a-4e04-91a9-a10ee76c836b
title: JobOptimalDestinationColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a63f63993f6a9cf8de8ba0a332407bb645099d98e6d92669c18368bd7629a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099666"
---
# <a name="joboptimaldestinationcolorprofile"></a>JobOptimalDestinationColorProfile

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

指定目前裝置設定的最佳色彩設定檔。

-   [項目資訊](#element-information)
-   [結構化內容](#structural-content)
-   [可延伸標記語言 (XML)  (XML) 內容](#extensible-markup-language-xml-content)

## <a name="element-information"></a>項目資訊



| Name | 值 |
|----------------------------|---------------------|
| 項目類型 <br/>   | 屬性<br/> |
| 範圍前置詞 <br/> | 工作 (Job)<br/>      |
| 注意 <br/>          | None<br/>     |



 

## <a name="structural-content"></a>結構化內容

此元素的 XML 結構為：

``` syntax
<psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_ProfileValue_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_ProfileDataValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_PathValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| Name                            | 資料類型         | 單位           | 支援的值          | 摘要                                        |
|---------------------------------|-------------------|----------------|---------------------------|------------------------------------------------|
| \_ProfileValue\_<br/>     | 字串<br/> | n/a<br/> | RGB、ICC、CMYK<br/> | 指定色彩設定檔。<br/>        |
| \_PathValue\_<br/>        | 字串<br/> | n/a<br/> | n/a<br/>            | 指定設定檔的檔案路徑。<br/> |
| \_ProfileDataValue\_<br/> | 字串<br/> | n/a<br/> | n/a<br/>            | 包含設定檔資料內容。<br/>      |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

公用列印架構關鍵字是在 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 命名空間中定義。 此關鍵字的 public 可延伸標記語言 (XML)  (XML) 內容定義如下：

``` syntax
 <psf:Property name="psk:JobOptimalDestinationColorProfile">
  <psf:Property name="psk:Profile">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    <psf:Property name="psk:ProfileData">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:Path">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




