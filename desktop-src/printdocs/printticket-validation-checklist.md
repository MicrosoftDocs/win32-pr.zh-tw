---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: PrintTicket 驗證檢查清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a0e9f3eb71b1e9a3b670456e04e2efa3c8b15
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975610"
---
# <a name="printticket-validation-checklist"></a>PrintTicket 驗證檢查清單

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintTicket 提供者必須先驗證 PrintTicket，才能使用它來進行任何用途。 當 PrintTicket 經過驗證之後，它可能會傳回給用戶端，或在使用之後捨棄。 這份檢查清單涵蓋了提供者在驗證期間必須執行的工作。 驗證程式會經常改變 PrintTicket 的內容，不過它不會改變先前驗證的 PrintTicket。

針對在 PrintCapabilities 檔中定義的一組功能、選項和 ParameterDef 實例的特定裝置，一律會執行驗證。 驗證程式代碼應該可存取一組功能實例 (以及特定裝置的包含選項實例) 和 ParameterDef 實例，而且不應該存取 PrintCapabilities。 在驗證程式的某些部分中，需要功能、選項和 ParameterDef 實例的資訊。

1.  在嘗試尋找對應或比對專案的期間，請注意，元素的命名空間必須符合，才能將任何限定名稱視為相符。 所有專案名稱、屬性名稱和實例名稱都是限定命名空間。 針對已嵌套的專案，其位置必須符合，才能將專案視為相符。

2.  確認所有元素標記都在公用命名空間中、由 PrintTicket 架構定義、包含適當的 XML 屬性和屬性值，而且每個專案類型的位置符合 PrintTicket 架構定義的使用方式。

3.  判斷 PrintCapabilities 檔所報告的所有命名空間。 從 PrintCapabilities 檔所報告的命名空間所屬的 PrintTicket 中，移除所有 (和其子系) 的元素。 請注意此案例與下列案例之間的差異，這牽涉到已知命名空間內無法辨識的實例名稱。

4.  由於架構會持續擴充，並新增新的元素實例定義，因此不應該在假設指定命名空間中的每個實例名稱都知道時，撰寫驗證碼。 驗證程式代碼無法在已知的命名空間中將無法辨識的實例名稱視為錯誤，也無法從 PrintTicket 刪除它們。

5.  如果任何專案實例具有 PrintTicket 架構不允許的重複同級，請只保留第一個出現的專案，然後刪除重複專案，包括重複專案的內容。

6.  從 PrintTicket 的任何功能或 subfeature (，以及 PrintCapabilities 檔中沒有對應功能的所有子系) 移除。

7.  針對 PrintTicket 中的每個剩餘功能實例，檢查 PrintCapabilities 檔中定義的 SelectionType 屬性。 SelectionType 屬性設定為 PickOne 的任何功能，都必須只有一個選項實例存在於 PrintTicket 中，而 SelectionType 屬性為 PickMany 的功能可能會有一個以上的選項實例。 如果 PrintTicket 功能沒有選項實例，請提供預設選項實例。 由於您是提供者，因此您知道哪一個選項是每項功能的預設選項。

    針對 SelectionType 屬性為 PickMany 的功能，在 PrintTicket 中選取一個以上的選項時，請確認未將任何選項指定為 IdentityOption。 如果有，請刪除每個其他選項，只留下一個指定的 IdentityOption。

8.  移除在 PrintCapabilities 檔中沒有對應 ParameterDef 實例之 PrintTicket 中的任何 ParameterInit 實例。

    針對 PrintTicket 中的任何其他 ParameterInit 實例，請確認每個實例的值都符合 PrintCapabilities 檔的 ParameterDef 實例。 如果缺少值，請提供 ParameterDef 中提供的預設值。

9.  根據評分流程的結果，將 PrintTicket 中的每個選項實例與 PrintCapabilities 檔中對應功能所列的選項配對。 評分是在 PrintCapabilities 檔中尋找最符合 PrintTicket 中所指定選項之選項的程式。 如需評分程式期間所考慮之事項的說明，請參閱 [選項定義](option-definitions.md)。 以對應的最符合候選 PrintCapabilities 檔選項取代 PrintTicket 中的每個參考選項。 您也可以藉由分數來將這項資訊排名，並將這項資訊傳遞給解決階段，以防條件約束衝突導致無法使用最符合的候選項目。 在這種情況下，解析程式可以使用第二個最佳候選項，而不是隨機挑選另一個候選項。

10. 若為 SelectionType 屬性設定為 PickMany 的功能，且在 PrintTicket 中選取了一個以上的選項，請確認沒有任何選項指定為 IdentityOption。 如果有這樣的選項，請刪除每個其他選項，只留下一個指定的 IdentityOption。 您必須在套用評分程式之前和之後執行此步驟。

    此步驟必須執行兩次的原因是，評分程式可能會將多個參考選項實例對應至相同的候選選項。 如果發生這種情況，請刪除任何重複的選項實例，讓針對特定 PickMany 功能列出的選項是唯一的。

11. 將任何存在於 PrintCapabilities 檔中且未出現在 PrintTicket 中的功能加入至 PrintTicket。 針對這類功能，請指定預設選項做為選取的選項。

12. 判斷是否有任何符合下列條件的 ParameterDef 實例：

    -   ParameterDef 實例會出現在 PrintCapabilities 檔中，但不會出現在 PrintTicket 中。

    -   ParameterDef 實例的必要屬性會設定為無條件或條件式。

    -   ParameterDef 實例是由選項實例內的 PrintTicket 中的 ParameterRef 實例所參考。

    針對 PrintCapabilities 檔中的每個這類 ParameterDef 實例，將對應的 ParameterInit 實例加入至 PrintTicket。 將新加入的 ParameterInit 實例值設定為對應 ParameterDef 實例所指定的預設值。

13. 執行條件約束衝突偵測並修改設定，以排除任何這類衝突。 本主題不會定義用來解決條件約束衝突的特定處理常式。 您必須決定可以變更哪些功能或 ParameterInit 實例，以及分別選取適當的選項或值，以針對 PrintTicket 中指定之設定的整體意圖產生最小的影響。 如先前所述，您可能會想要使用每個選項的對應分數，並使用具有第二個最高分分數的選項。 若要判斷要變更的功能或 ParameterInit，您可能會想要定義用戶端可以加入至 PrintTicket 的私用屬性。 這個屬性可以定義 Feature 和 ParameterInit 實例的優先順序，讓解析程式知道哪些功能或 ParameterInit 實例對用戶端而言是很重要的 (而且需要保留在 PrintTicket) 中，這一點比較不重要。

14. 如果條件約束解析程式造成將 PrintTicket 變更為 [強制] 屬性設定為 [條件] 的任何 ParameterRef 實例，請使用現在顯示的預設值來加入 ParameterInit 實例，然後移除不再出現之 ParameterRef 實例的任何 ParameterInit 實例。

15. 移除在 PrintTicket 的選項實例內出現的所有屬性實例及其內容。 屬性元素在 PrintTicket 中沒有任何角色。 如果特定功能的已驗證選項完全符合 prevalidated 選項，請將該選項中的所有屬性實例從 prevalidation 的 PrintTicket 傳送至立即驗證的 PrintTicket，受限於在 PrintCapabilities 檔中註冊屬性實例命名空間的條件。 請注意，若要將兩個選項實例視為完全相符，請針對一個選項中找到的每個 ScoredProperty，在其他選項中都必須有對應的 ScoredProperty，而且兩個 ScoredProperty 實例的值都必須相同。

16. 如果您的 PrintTicket 提供者可辨識並支援任何已在此點存活的私用或公用屬性實例，請在這些實例上執行驗證。 請勿在此時刪除屬性，因為您無法辨識該屬性，它可能適用于另一個檔處理階段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



