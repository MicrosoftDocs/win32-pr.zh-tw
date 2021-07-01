---
description: 瞭解檔和列印中的屬性元素。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: '屬性 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e43b52c054972ee0ee2b8a535021581c05e7d96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120293"
---
# <a name="property-documents-and-printing"></a>屬性 (檔和列印) 

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

屬性專案會宣告裝置、作業格式或其他相關屬性，其名稱是由其名稱屬性所指定。 值元素用來將值指派給屬性。

屬性可能很複雜，可能包含多個子屬性。 子屬性也會以屬性元素表示。

## <a name="element-tag"></a>元素標記

<Property>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性   | 詳細資料                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| NAME<br/> | 保存屬性（attribute）的 name 屬性（property），該屬性（property）是標準屬性（property）或私用屬性（attribute）。 <br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素<br/> | PrintCapabilities <br/> 功能<br/> PrintTicket<br/> 選項<br/> ParameterDef<br/> 屬性<br/> ScoredProperty<br/>                                                                                                                                                              |
| 子元素<br/>  | 系統不會將任何意義指派給元素的順序。 如果用戶端選擇歸屬元素順序中的一些重要性，則可以隨意進行。 <br/> *屬性* (一或多個) *值* (零或多個) <br/> 或 <br/> *屬性* (零或多個) *值* (一或多個) <br/> |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 允許同級的重複子值元素。<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>設定相依性

屬性可能具有設定相依性，除非它出現在 ParameterDef 元素中。

## <a name="element-usage"></a>專案使用方式

除了出現在功能和選項專案中之外，屬性專案也可以出現在個別基礎技術的根層級上。 列印架構會定義一組屬性元素，可用來以可移植的方式描述裝置。 但是，如果這些屬性不符合您的需求做為 PrintCapabilities 提供者 (通常是因為支援的裝置具有列印架構) 不預期的新穎層面，您可能會引進自己的私用屬性元素。 您可以藉由將一或多個私用子屬性新增為公用屬性的元素內容，來增強或詳細地增強或詳細說明公用屬性所提供的資訊。

您可以使用 XML 專案標記來定義屬性元素 <Property> 。 每個屬性都會透過其 name 屬性來指派名稱。 名稱必須是 XML QName，而且必須符合命名空間慣例。 如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md)。 屬性名稱屬性及其在父屬性專案階層中的位置 (如果它是子屬性) 可唯一識別 PrintCapabilities 檔內的屬性或 PrintTicket。

屬性可包含一或多個值元素，或是一或多個子屬性元素 (稱為子屬性) ，或兩者的組合。 當屬性本身由多個元件組成時，子屬性會很有用。 例如，"ConsumableColor" 屬性可能具有 "C"、"M" 和 "Y" 元件。

## <a name="example"></a>範例

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




