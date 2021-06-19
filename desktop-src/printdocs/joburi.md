---
description: 深入瞭解 JobURI 元素，此元素會為檔指定 (URI) 的統一資源識別項。
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: JobURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408611"
---
# <a name="joburi"></a>JobURI

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

為檔指定 (URI) 的統一資源識別項。

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

此元素的 XML 結構如下所示：

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a>結構變數

下表概述 XML 結構中所定義之變數的特性。



| Name                       | 資料類型         | 單位 | 支援的值 | 總結 |
|----------------------------|-------------------|------|------------------|---------|
| \_JobURIValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>可延伸標記語言 (XML)  (XML) 內容

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




