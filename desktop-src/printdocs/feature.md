---
description: 檢查功能元素，其中包含描述裝置屬性、作業格式設定或其他相關特性的選項和屬性專案清單。
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d35686674d08ea0ea4030648b06803919e5d07
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882498"
---
# <a name="feature"></a>功能

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

Feature 元素包含選項和屬性專案的完整清單，可完整描述裝置屬性、作業格式設定或其他相關特性。

## <a name="element-tag"></a>元素標記

&lt;功能&gt;

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性   | 詳細資料                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| NAME<br/> | 保存功能的名稱，也就是標準功能或私下定義的功能。 <br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。




| 類別 | 詳細資料 | 
|----------|---------|
| 父元素<br /> | PrintCapabilities <br /> PrintTicket <br /> 功能<br /> | 
| 子元素<br /> | 下列其中一個群組：<br /><ul><li><em>功能</em> (零或多個) <br /></li><li><em>選項</em> (一或多個) <br /></li><li><em>屬性</em> (零或多個) <br /></li></ul>或 <br /><ul><li><em>功能</em> (一或多個) <br /></li><li><em>選項</em> (零或多個) <br /></li><li><em>屬性</em> (零或多個) <br /></li></ul> | 
| 這個元素<br /> | 不允許任何字元資料。<br /> 允許有同級的重複子選項元素。 允許重複的名稱屬性快捷方式。 <br /> | 




 

## <a name="configuration-dependencies"></a>設定相依性

功能元素可能沒有任何設定相依性。

## <a name="element-usage"></a>專案使用方式

### <a name="relationship-to-xml-attributes"></a>與 XML 屬性的關聯性

在功能/選項標記法中，裝置屬性是由 Feature 元素表示。 裝置屬性是由裝置屬性的 Feature 元素中的 name 屬性唯一識別，如下列範例所示。 在此範例中，裝置屬性為「解析」。

``` syntax
<Feature name="Resolution" />
```

列印架構會定義特定功能實例的一組名稱屬性。 這些名稱屬性會用來識別一組與特定可設定裝置屬性相關聯的預先定義功能實例。 您應該在適當的情況下使用這些功能實例名稱，因為它們會增加 PrintCapabilities 檔的可攜性，以及從中衍生的 PrintTickets。 如果某些裝置屬性未對應到任何架構定義的功能實例，可能會引進私用定義的功能實例。 如需名稱屬性語法的詳細資訊，以及適用于架構定義和私人定義名稱的慣例，請參閱 [XML 屬性](xml-attributes.md)。

### <a name="relationship-to-option-element"></a>Option 元素的關聯性

每個可能的狀態都會以 Option 元素表示。 每個選項定義都包含一或多個 ScoredProperty 元素，這些元素會以獨特的方式來描述或描述所表示的狀態。 [選項定義](option-definitions.md)中說明用來建立選項定義的技巧。 所有與特定功能專案相關聯的選項元素都會作為 Feature 專案的子專案。

### <a name="subfeatures"></a>釋放

Print Schema Framework 也可讓您以階層方式將功能專案群組在一起。 也就是說，Feature 元素本身可以包含一或多個子功能元素， (子功能) 。 這有助於組織相關的功能專案，或用於控制裝置功能各個層面的功能元素。 其中一個範例是支援裝訂的裝置。 這類裝置可讓使用者選擇要在哪裡找到裝訂，例如左上角或右上角，或是沿著上邊緣，或是沿著左邊緣。 此裝置 (UI) 的使用者介面應該能夠先顯示最高層級選項的使用者，在此案例中是要使用裝訂。 只有在使用者決定使用裝訂之後，使用者才會看到第二層選擇：裝訂位置。 功能階層會新增可讓這類使用者介面成為可能的額外結構。 Print Schema Framework 可讓子功能擁有自己的子功能，因此允許無限制的嵌套層級。

Print Schema Framework 也可讓選項元素出現在與子功能相同的層級;亦即相同父項功能專案內的同級。 這可讓使用者進行高階決策 (是否要在進行 subfeature 選擇之前使用裝訂) 。 在此範例中，根功能元素 "裝訂" 可能包含兩個選項元素： "On" 和 "Off"，以及名為 "StapleLocation" 的 subfeature。

## <a name="example"></a>範例

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




