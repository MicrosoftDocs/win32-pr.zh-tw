---
description: 本文提供檢查清單，說明 PrintCapabilities 檔的作者可用來建立描述裝置的 PrintCapabilities 檔。
ms.assetid: 4b8fa1a4-6461-4722-861b-354f206b2a73
title: PrintCapabilities 檔結構檢查清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee309c96cf7b2d70cb78f125e7783668fb2298da
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407111"
---
# <a name="printcapabilities-document-construction-checklist"></a>PrintCapabilities 檔結構檢查清單

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

[元素類型的摘要](summary-of-element-types.md)會討論群組成 PrintCapabilities 檔的各種專案。 本節提供 PrintCapabilities 檔作者可用來建立描述裝置之 PrintCapabilities 檔的檢查清單。

1.  識別參與裝置設定的所有裝置屬性。 針對每個這類裝置屬性，判斷是否應該將它表示為特徵/選項結構或作為參數結構。

2.  針對每個裝置功能，判斷是否可由列印架構關鍵字中定義的功能來表示。 如果不是，您將需要引入新的私用自訂功能 (以及對應的名稱屬性) 。

    -   針對列印架構關鍵字定義的功能實例，識別可設定此功能的每個可用狀態。 每個狀態都對應至功能實例的選項。 判斷哪一個狀態對應至與這項功能相關聯之列印架構定義的選項實例，以及哪些狀態需要自訂的選項實例。 [選項定義](option-definitions.md)主題提供如何建立新選項實例的相關資訊，以及如何從現有的選項實例衍生新的選項實例。

    -   針對非標準的功能實例，識別可用來區別某個選項與另一個選項的特性。 代表 ScoredProperty 專案的每個這類特性，並在每個選項實例中，為每個 ScoredProperty 指派該選項的特定值。 確定有足夠的 ScoredProperty 元素，讓指定功能的每個選項都是唯一的。 非標準的功能和選項實例的本質是 nonportable。 也就是說，另一個驅動程式將無法找到任何對等的功能或選項，以符合您的驅動程式所建立之 PrintTicket 中指定的非標準功能或選項。

3.  判斷任何選項是否必須包含 ParameterRef 元素。 如需詳細資訊，請參閱 [參數結構](parameter-constructs.md) 和 [參數參考元素](parameter-reference-elements.md)。

4.  針對參數，請判斷列印架構關鍵字中定義的其中一個 ParameterDef 實例是否為適當的相符項。 如果是的話，請從 Print Schema 關鍵字複製 ParameterDef 實例，然後調整每個可變屬性實例的值，以獲得最佳的配合。 如果 Print Schema 關鍵字中的 ParameterDef 實例都沒有足夠的相符項，請建立您自己的 ParameterDef 實例。 如需詳細資訊，請參閱 [PrintCapabilities 檔中的參數](parameters-in-the-printcapabilities-document.md)。

5.  確定您的 PrintCapabilities 檔中有列印架構關鍵字檔所需的所有屬性和 ScoredProperty 實例，而且這些實例已正確初始化。

6.  視需要新增其他屬性和子屬性實例。 如果您需要描述的裝置部分，不是由列印架構關鍵字中定義的屬性實例所涵蓋，您可能會引進私用定義的屬性實例。

7.  觀察 name 屬性的命名空間慣例。 這適用于私用定義的名稱屬性，以及在 Print Schema 關鍵字中定義的屬性。

8.  相同專案類型的子系不可嵌套至超過10個元素的深度。 這項規則會獨立套用到每個可定義的元素類型。

請注意，列印功能檔 XML 內容必須使用 UTF-8 或 UTF-16 進行編碼。

請注意，不論快照集為何，所報告的一組功能、選項和 ParameterDef 實例都不能變更。 組成每個選項實例以及指派給每個 ScoredProperty 元素之值的 ScoredProperty 實例也不得變更。 這也適用于組成每個 ParameterDef 實例的屬性實例。

如需必須提供才能完整定義功能/選項結構和參數的其他屬性實例清單，請參閱 [ParameterDef](parameterdef.md) 和 [ParameterInit](parameterinit.md)。 例如，每個功能都必須將其使用者介面指定 (UI) 的行為，特別是是否可以一次為每項功能選取一個或多個選項實例。 列印架構關鍵字檔會定義這些屬性實例，其中必須出現在 PrintCapabilities 檔中，而且可以使用列印架構關鍵字中所定義的值實例。

PrintCapabilities 提供者負責針對所有設定相依的屬性實例發出適當的值。 例如，如果列印速率取決於所使用的色彩模式和解析度，則 PrintCapabilities 提供者必須注意在用戶端提供的 PrintTicket 中所指定的色彩模式和解析度設定，並且必須針對列印速率報告適當的值。 請注意，每個 ScoredProperty 實例都必須是單一值;當裝置設定變更時，其值實例無法變更。

另外也請注意，在 [列印架構] 關鍵字中定義的屬性實例，必須出現在指定的位置。 它們不能出現在 PrintCapabilities 檔中的任意位置。 私用定義的屬性實例可能會出現在任何地方，甚至是在架構定義的屬性實例中的子屬性。

請注意，設定之間的功能衝突定義為兩個不衝突的列印架構元素，這些專案具有類似的功能，但功能不同。 例如，JobDuplexAllDocumentsContiguously 和 DocumentDuplex;兩者都代表裝置的雙工函式，但在函式的應用程式中不同，一個會連續套用至整個作業，另一個則是檔。 在指定兩個這類元素的情況下，優先順序取決於 PrintCapabilities 生產者和 PrintTicket 取用者。 PrintCapabilities 產生者必須負責適當地指出透過「受限」屬性的衝突元素之間的條件約束。 公開列印架構中展示此語義衝突的專案會在其定義中識別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



