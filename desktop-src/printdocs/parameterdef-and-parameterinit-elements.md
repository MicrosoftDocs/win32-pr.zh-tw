---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: ParameterDef 和 ParameterInit 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106985829"
---
# <a name="parameterdef-and-parameterinit-elements"></a>ParameterDef 和 ParameterInit 元素

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

ParameterDef 元素與 ParameterInit 元素不同之處在于，它會描述 ParameterInit 元素可包含的值，而 ParameterInit 專案則會將值指派給參數。 ParameterDef 元素是由一組特定的屬性元素所組成，也就是 ParameterDef 元素的子系，可指定資料的類型、最大值、最小值和預設值，以及其他資訊。 本主題稍後會討論這些屬性元素。

ParameterDef 元素只能出現在其允許的內容中。 針對列印架構的初始版本，它們可能位於 PrintCapabilities 檔的根層級。 ParameterDef 元素的 name 屬性會定義參數名稱。 PrintCapabilities 檔中的每個 ParameterDef 元素都必須被指派一個唯一的名稱屬性。

> [!Note]
> 若要列印功能檔提供者：
> 
> 參數名稱的意義是通用的;也就是說，如果某個 PrintCapabilities 檔中的 ParameterDef 專案具有相同的名稱屬性 (命名空間所形成的字串，以及 ParameterDef 專案的描述性名稱) 為另一個 PrintCapabilities 檔中的 ParameterDef 專案，則會假設這兩個元素都代表相同的概念，而且應該以相同的方式加以解讀。 因此，在一個 PrintCapabilities 檔的 PrintTicket 中定義的 ParameterDef 元素可以用來初始化不同 PrintCapabilities 檔中所定義之相同名稱的 ParameterInit 專案。

 

## <a name="relationship-to-xml-attributes"></a>與 XML 屬性的關聯性

如同所有 name 屬性的 true，參數名稱的格式為 XML QName。 架構定義的參數結構具有由公用命名空間限定的名稱，形成 name 屬性，而私用定義的參數結構名稱屬性則是由 creator 的唯一私用命名空間限定。

## <a name="relationship-between-parameterdef-and-property-element-types"></a>ParameterDef 和 Property 元素類型之間的關聯性

ParameterDef 在列印架構關鍵字中定義的元素必須在 PrintCapabilities 檔中完整定義。 Print Schema 關鍵字檔提供 ParameterDef 專案的某些屬性專案的名義值 (例如 DefaultValue 和其他) ，但 PrintCapabilities 檔的作者必須負責定義其餘的屬性元素。 在任何情況下，所有屬性專案都必須在 ParameterDef 專案中明確定義，包括在 Print Schema 關鍵字中定義的元素。

顯示在列印架構關鍵字中的每個 ParameterDef 專案的特定屬性元素會指定為 *不可變*。 這表示，列印架構關鍵字定義 ParameterDef 專案的所有 PrintCapabilities 檔定義都必須保留這些屬性元素，而不需要修改。 這些不可變的屬性元素可讓參數結構在所有 PrintCapabilities 檔中都是可移植且不明確的。 ParameterDef 元素中使用的單位是主要範例。 這些單位應該是不可變的，以促進對其意義的一致理解。 在 PrintCapabilities 檔中，可重新定義指定為不可變之 ParameterDef 的屬性元素。

ParameterDef 元素是由下列屬性元素所組成。 除非另有說明，否則全部都必須存在。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性名稱</th>
<th>值</th>
<th>描述</th>
<th>變？</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataType <br/></td>
<td>整數 <br/> decimal<br/> 字串<br/> 無預設值。<br/></td>
<td>指定參數值是整數、浮點數或文字字串。 參數的值會使用與對應的 XSD 基本資料類型相同的格式來表示;也就是整數、十進位或字串。 <br/></td>
<td>Yes<br/></td>
</tr>
<tr class="even">
<td>DefaultValue <br/></td>
<td>DataType 屬性指定的型別。<br/> 無預設值。<br/></td>
<td>指定用來初始化使用者介面 (UI) 控制項的值。<br/>
<ul>
<li>或 <br/></li>
</ul>
指定當 PrintTicket 中缺少相關的參數專案時，所要使用的值。<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>強制性 <br/></td>
<td>無條件：必須一律提供 ParameterInit 元素。 <br/> 條件式：只有在 PrintTicket 的 Option 元素內參考參數時，才需要 ParameterInit 元素。<br/> DefaultValue：條件式。<br/></td>
<td>指出 ParameterInit 元素必須明確出現的時間。 如果是條件式，則如果 PrintTicket 包含參考參數的選項，則 ParameterInit 必須初始化。<br/> 由 UI 用戶端和 PrintCapabilities 或 PrintTicket 提供者使用。 請注意，在任何條件約束中，ParameterDef 元素的強制屬性必須設定為無條件。 ParameterDef 必須有定義的值，否則無法評估相依的值或條件約束。<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MaxLength <br/></td>
<td>如果 DataType 屬性指定 string，則為整數。<br/> DefaultValue：不會強制執行最大值。<br/></td>
<td>若為字串值參數，則指定允許的最長字串。 UI 和 PrintCapabilities 或 PrintTicket 提供者會使用這個屬性來驗證 ParameterDef 元素。<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MaxValue <br/></td>
<td>如果 DataType 屬性指定整數，則為整數。<br/> 如果 DataType 屬性指定 decimal，則為 decimal。<br/> DefaultValue：不會強制執行最大值。<br/></td>
<td>若為整數或十進位值 ParameterDef 元素，則會定義最大的允許值。<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MinLength <br/></td>
<td>如果 DataType 屬性指定 string，則為整數。 <br/> DefaultValue：不會強制執行最小值。<br/></td>
<td>針對字串值，定義允許的最短字串。 UI 和 PrintCapabilities 或 PrintTicket 提供者會使用這個屬性來驗證 ParameterDef 元素。<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MinValue <br/></td>
<td>如果 DataType 屬性指定整數，則為整數。<br/> 如果 DataType 屬性指定 decimal，則為 decimal。<br/> DefaultValue：不會強制執行最小值。<br/></td>
<td>針對整數或十進位值參數，定義最小的允許值。 <br/></td>
<td>否<br/></td>
</tr>
<tr class="even">
<td>多個 <br/></td>
<td>如果 DataType 屬性指定整數，則為整數。<br/> 如果 DataType 屬性指定 decimal，則為 decimal。<br/> DefaultValue：1<br/></td>
<td>若為整數或十進位值參數，參數的值應該是這個數位的倍數。 如需詳細資訊，請參閱下表的 <a href="#notes-on-multiple">多個注意事項</a> 。<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>Unittype.pixel 表示 <br/></td>
<td>字串值，表示用於參數的單位。<br/> 無預設值。<br/></td>
<td>表示用來表示參數的單位。 例如，以十分之一度為單位的角度、microns 中的長度等等。<br/></td>
<td>Yes<br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a>多個筆記

對於具有整數或十進位值的 ParameterInit 元素，ParameterInit 的值應該是此數位的倍數。 例如，您可以將此屬性設定為0.1，將十進位值 ParameterInit 元素限制為十分之一。 UI 元素在建立對話方塊和 UI 控制項時，會使用這個屬性。 此外，PrintTicket 驗證程式代碼可以使用這個屬性，將 ParameterInit 的值四捨五入為多個指定的最接近值。 注意：設備磁碟機與 PrintCapabilities 提供者不應假設 ParameterInit 值是此屬性值的倍數。 每個提供者都必須能夠將任意值舍入為最接近的可用值，因為可能是不同的提供者可能會為此屬性指定不同和衝突的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




