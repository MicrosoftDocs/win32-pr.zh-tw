---
description: 瞭解如何建立裝置特定的 PrintTicket （以特定裝置為目標，並可在多個裝置上移植）。
ms.assetid: 487f294f-dfe0-48f8-9077-06c55c3af8f1
title: 建立 Device-Specific 的 PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b825bd875ada534c8c467cd18d90f2db9a2a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409542"
---
# <a name="creating-a-device-specific-printticket"></a>建立 Device-Specific 的 PrintTicket

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

裝置特定的 PrintTicket 以特定的裝置為目標，因此通常不會在多個裝置上移植。

當您建立裝置特定的 PrintTicket 時，應使用下列清單所示的步驟。

1.  取得僅包含裝置相關功能實例的 PrintCapabilities 檔。 要求預設的 PrintCapabilities 檔。 這不需要您指定輸入 PrintTicket，因為裝置屬性 (功能和用來建立 PrintTicket 的選項實例和參數) ，與設定無關。

2.  建立空白的 XML 檔，其中包含 PrintTicket 根。 將命名空間前置詞指派給列印架構命名空間，並指派 PrintTicket 將使用的所有其他命名空間的前置詞。 指定 PrintTicket 架構版本。

3.  您可以針對 PrintCapabilities 檔中報告的每個功能和 ParameterDef 實例定義 PrintTicket 中的設定，或僅針對您感興趣的設定。 如果將部分的 PrintTicket 呈現給 PrintTicket 介面，在 PrintTicket 驗證期間，會自動為省略的功能和 ParameterDef 實例提供預設值。

4.  檢查 PrintCapabilities 檔中的功能實例，並判斷您想要在 PrintTicket 中定義哪些。 將這些功能實例加入至 PrintTicket，但不要將功能實例的內容傳送至您的 PrintTicket。 如果您傳輸 subfeature，也必須傳送父功能，而且必須在 PrintTicket 中保留父子式關聯性。

    針對您傳送的每個功能，判斷哪些選項實例適用于您的 PrintTicket。 傳送 PrintCapabilities 檔中定義的整個選項，然後移除任何存在的屬性實例。 屬性實例用於 PrintCapabilities 檔中，但在 PrintTicket 中沒有任何用途。 保留所有 ScoredProperty 實例，並確定您保留其位置;它們是選項定義的內建部分。

5.  您也可以將屬性實例加入至任何 ScoredProperty 實例。 只有當 PrintTicket 提供者明確支援其使用時，才會使用屬性實例。 每個提供者都應記錄所有支援之屬性實例的用途和用法。 請注意，在驗證期間，除非目標 PrintCapabilities 或 PrintTicket 提供者可辨識屬性的命名空間，而且在 PrintCapabilities 檔中找到 ScoredProperty 實例完全符合參考選項中所定義的屬性實例，否則會將該選項實例中包含的任何屬性實例移除。

6.  如果 Print Schema 關鍵字將特定功能的 SelectionType 屬性設定為 PickMany，您可以為該功能選取一個以上的選項，但前提是指定為 IdentityOption 的選項不是選取的選項之一。 列印架構中的 IdentityOption 與 Postscript PPD 檔案和 Unidrv GPD 檔案中的 [無] 選項有相同的效果;它是一種無作業的服務。

7.  檢查您的 PrintTicket 中應設定之 ParameterDef 實例的 PrintCapabilities 檔。 針對每個這類 ParameterDef 實例，選取要在 PrintTicket 的 ParameterInit 實例中使用的值。 這個值必須是正確的資料類型，而且必須落在 ParameterDef 實例中定義的範圍內，而且必須符合 ParameterDef 實例中指定的所有其他需求。 使用 ParameterInit 實例將參數初始化為您所選取的值。

8.  檢查 ParameterRef 實例出現的 PrintTicket 中，每個選項實例的內容。 如果對應的 ParameterInit 實例尚未出現在 PrintTicket 中，請依照上一個步驟在 PrintTicket 中建立 ParameterInit 實例。 這個 ParameterInit 實例的目的是要初始化 ParameterRef 實例所參考的參數。

9.  請記住，條件約束衝突可能會導致裝置無法套用您在 PrintTicket 中指定的設定。 如有必要，驗證程式會將 PrintTicket 中定義的設定修改為無衝突的設定。

10. 檢查必須存在於您的 PrintTicket 中之屬性實例的列印架構關鍵字。 針對所需的每個專案，將屬性實例加入至您的 PrintTicket，並使用 Value 元素類型為其提供適當的值。 請確定屬性實例正確地放在 PrintTicket 內。

11. 檢查 PrintTicket 架構中的選擇性屬性實例。 如果您的 PrintTicket 中有任何這類屬性實例，請在您的 PrintTicket 中建立它們。

12. 您也可以在根層級或任何功能、選項或屬性實例中，新增私用定義的屬性實例。 不過請注意，除非目標 PrintCapabilities 或 PrintTicket 提供者可以辨識這些私用的屬性實例，否則在驗證期間會將它們移除。 此外，除非 PrintCapabilities 檔包含完全相符的選項，否則在驗證期間會移除出現在選項實例內任何位置的屬性實例。 如果某個選項實例中的每個 ScoredProperty 都有相對應的 ScoredProperty，而 ScoredProperty 實例的值相同，則兩個選項實例是完全相符的。 請參閱 PrintTicket 提供者的私用架構，以取得可辨識之私用屬性實例及其用法的清單。

13. 相同專案類型的子系不可嵌套至超過10個元素的深度。 這項規則會獨立套用到每個可定義的元素類型。

> [!Note]  
> 必須使用 UTF-8 或 UTF-16 來編碼 PrintTicket XML 內容。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



