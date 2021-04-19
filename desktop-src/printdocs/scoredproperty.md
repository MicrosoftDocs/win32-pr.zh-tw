---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: ScoredProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106988116"
---
# <a name="scoredproperty"></a>ScoredProperty

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

ScoredProperty 元素會宣告選項定義內建的屬性。 當評估要求的選項符合裝置支援的選項時，應該比較這類屬性。

## <a name="element-tag"></a>元素標記

<ScoredProperty>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性   | 詳細資料                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| NAME<br/> | 保留 ScoredProperty 的 name 屬性，也就是標準屬性或私用定義的屬性。 <br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素<br/> | *選項*<br/> *ScoredProperty*<br/>                                                                                                                          |
| 子元素<br/>  | 或<br/> *ParameterRef* (一) <br/> 或<br/> *值* (一) <br/> *屬性* (零或多個) <br/> *ScoredProperty* (零或多個) <br/> |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 不允許重複的子同級。<br/>                                                                        |



 

## <a name="configuration-dependencies"></a>設定相依性

ScoredProperty 元素可能沒有任何設定相依性。

## <a name="example"></a>範例

宣告名為 MediaSizeWidth 的 ScoredProperty 元素，其值為11。

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




