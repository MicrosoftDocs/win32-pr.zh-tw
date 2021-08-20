---
description: 深入瞭解 Value 元素，這會將常值與型別產生關聯。 值的資料類型必須是字串、整數、十進位或 QName。
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739ce465408d1cd1447de5aeac2e314e879f48f69f13735855e628c8901c2c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685859"
---
# <a name="value"></a>值

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

值元素會將常值與型別產生關聯。

## <a name="element-tag"></a>元素標記

<Value>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性       | 詳細資料                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | 指定值的資料類型，其必須是下列其中一個 XSD 定義類型： string、integer、decimal、QName。 如果遺失，則預設資料類型為 string。<br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素<br/> | ParameterInit <br/> 屬性<br/> ScoredProperty<br/>                                                                                   |
| 子元素<br/>  | 只允許字元或整數內容。<br/>                                                                                                |
| 這個元素<br/>    | 允許 Null 內容。 字元內容必須符合資料類型所定義的語法。<br/> 不允許重複的子同級。<br/> |



 

## <a name="configuration-dependencies"></a>設定相依性

出現在 ScoredProperty 元素內的值元素可能沒有任何設定相依性。 出現在屬性專案內的值元素可能會對設定有任意的相依性。

## <a name="element-usage"></a>專案使用方式

值元素可能會出現在屬性或 ScoredProperty 元素中。 Value 元素的目的是要將值表示為標準 XML 資料類型。 資料類型會指定為 Value 元素（xsi： type）的 XML 屬性。 請注意，不支援所有 XSD 定義或 XML 定義的類型。 如需支援類型的清單，請參閱 [元素類型的摘要](summary-of-element-types.md)。 值元素只能包含字元內容。 任何其他專案可能會顯示為值元素中的內容。

> [!Note]  
> 某些列印架構定義的屬性和 ScoredProperty 元素不包含值元素，因為它們的用途只是子屬性的父系。 您不應該將值專案加入至這些屬性（property），這些屬性不包含值元素。

 

若要符合 Print Schema Framework （需要值元素或子項目存在於支援值的元素中），則應該將值元素呈現為空白元素來表示不存在或未定義的值。也就是 <Value></Value>.

## <a name="example"></a>範例

定義 decimal 類型的值，並將其初始化為 "128.5"。

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




