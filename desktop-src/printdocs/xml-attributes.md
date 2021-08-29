---
description: 瞭解 Print Schema Framework 中的 XML 屬性。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa19a64dd5d3c59f7c5d26b86186912065a5f1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883475"
---
# <a name="xml-attributes"></a>XML 屬性

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

在列印架構架構中定義的數個元素類型中，會出現一些 XML 屬性。 具有相同名稱的 XML 屬性通常具有相同的意義，並遵循相同的規則，而不論其所在的元素類型為何。 因此，XML 屬性會依名稱（而不是其主控制項類型）列在這裡。 不允許私下定義的 XML 屬性。 只有在此處定義的 XML 屬性可用於 PrintCapabilities 檔或 PrintTicket，然後才可用於定義的內容中。

雖然私用的合作物件不允許將新的定義引入另一個合作物件的命名空間，但它們可以利用另一個私人命名空間的現有名稱，只要其使用方式與其他合作物件建立的使用量一致即可。 因此，選項可能包含由數個不同的合作物件所定義的 ScoredProperty 元素，每個都位於不同的命名空間中。



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性名稱</th>
<th>資料類型和值</th>
<th>目的</th>
<th>注意</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>NAME <br/></td>
<td>XML QName<br/></td>
<td>這個 XML 屬性會識別元素實例。 它會區分一個專案與相同元素類型的另一個專案。 這個 XML 屬性很廣泛地使用，稱為 name 屬性。<br/></td>
<td>下列限制與 name 屬性相關。<br/>
<ul>
<li>Name 屬性的格式必須是有效的 XML 定義 QName。 也就是說，它必須由有效的 XML 命名空間限定。 QNames 顯示為 name 屬性的值，即使已定義預設命名空間，也必須明確限定命名空間。 <br/></li>
<li>字元內容必須是有效的 XML 定義 QName 的字元內容。 <br/></li>
<li>私用定義的名稱必須以命名空間限定的命名空間，此命名空間與引進 name 屬性的合作物件具有唯一關聯性。<br/></li>
<li>同輩唯一性需求：兩個屬於相同元素類型的同一個同級元素可能具有相同的名稱屬性。 唯一的例外是 Option 元素，其中 name 屬性可以用來定義選項。 因此，多個同級的選項元素可能具有相同的名稱屬性。<br/></li>
<li>下列元素類型可能包含 name 屬性： Property、ScoredProperty、ParameterDef、Option 和 Feature。<br/></li>
<li>名稱屬性必須出現在包含它們的每個元素類型中，但某些先前定義的公用列印架構選項元素（例如 DocumentNUp）的情況除外。<br/></li>
</ul>
下列範例顯示如何使用 ' name ' 屬性來識別選項實例。 這是定義 Option 元素的正確方式。 提供者不應具有未命名的選項，除非它們是在列印架構中公開定義的，例如 DocumentNUp。<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  &lt;/psf:Option&gt;</code></pre></td>
</tr>
<tr class="even">
<td>傳播 <br/></td>
<td>列舉型別<br/> 目前未定義任何值。<br/></td>
<td>「傳播」屬性不會用於「列印架構」架構的初始版本。 它記載于此處，讓針對 Print Schema Framework 初始版本所執行的 PrintCapabilities 或 PrintTicket 驗證程式代碼可以處理任何後續的架構版本，而不會發生錯誤。<br/></td>

</tr>
<tr class="odd">
<td>約束 <br/></td>
<td>列舉型別<br/> 允許的值：<br/>
<ul>
<li>無 <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>指出選項是否可供選取或使用。 <br/></td>
<td>受條件約束屬性的允許值具有下列意義。 請注意，這些值依順序列出，從最嚴格的 (無) 到最嚴格的 (DeviceSettings) 。<br/> 無 <br/>
<ul>
<li>此選項不受限制。 <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>選項受限於 PrintTicket 設定。 這表示變更設定可以移除條件約束。 <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>選項受限於系統管理員的設定;使用者無法啟用此選項。<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>選項受限於裝置設定或實際安裝的裝置選項;使用者或系統管理員無法啟用此選項。<br/></li>
</ul>
當 PrintCapabilities 提供者報告條件約束屬性的值時，應該會報告最嚴格的限制條件約束。 例如，如果某個選項受限於系統管理員設定和裝置設定，則 PrintCapabilities 提供者應該報告 DeviceSettings。<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>這個 XML 屬性會在命名空間統一資源識別項 (URI) 和出現在 XML QName 中的命名空間前置詞之間建立連結。 您必須先建立針對 Print Schema Framework 所定義之命名空間 URI 的連結，才能使用任何架構定義的專案標記、屬性、名稱屬性等等。 您可以將此命名空間宣告為預設值，以避免實際以命名空間前置詞來限定元素標記，不過所有其他 QNames 都必須明確限定。 標準命名空間必須在適當的根項目中定義。 觀察有關使用 xmlns 屬性的所有 XML 規則和慣例。<br/> Print Schema Framework 的 URI 為 http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework 。<br/> 列印架構關鍵字的 URI 是 https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords 。<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




