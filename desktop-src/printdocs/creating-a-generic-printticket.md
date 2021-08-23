---
description: 瞭解如何建立一般的 PrintTicket，以防裝置的 PrintCapabilities 檔無法使用。
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: 建立一般的 PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f660b2f1c015e0d32f5bfd80d58cae96cf3450dfafb13a7758c644ad0a7576b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719728"
---
# <a name="creating-a-generic-printticket"></a>建立一般的 PrintTicket

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

如果裝置的 PrintCapabilities 檔無法使用，或目標裝置不明，您應該建立一般的 PrintTicket。 因為沒有提供一組功能和選項專案的 PrintCapabilities 檔，或參數，所以必須直接從 Print Schema 關鍵字取得這些元素類型支援的實例。

當您建立一般 PrintTicket 時，應使用下列清單中所示的步驟。

1.  建立空白的 XML 檔，其中包含 PrintTicket 根。 將命名空間前置詞指派給列印架構命名空間。 指定架構版本。

2.  檢查 Print Schema 關鍵字中的功能實例，並決定您要在您的 PrintTicket 中定義哪些。 將這些功能實例加入至您的 PrintTicket。 當您傳輸 subfeature 時，您必須傳送父功能，並保留在 PrintTicket 中的功能與 subfeature 之間的父子式關聯性。

    針對您傳送的每個功能實例，判斷哪些選項實例適用于您的 PrintTicket。 從這組選項實例，將每個整個選項實例都傳送在列印架構中，然後移除任何存在的屬性實例，但對於您的 PrintTicket 具有重要性的可能例外狀況。 保留所有 ScoredProperty 實例，並確定您保留其位置;它們是選項定義的內建部分。

3.  您也可以將屬性實例新增至任何 ScoredProperty。 只有當 PrintTicket 提供者明確支援其使用時，屬性元素才適用。 每個提供者都應記錄所有支援之屬性實例的用途和用法。 因為您不知道哪個提供者將處理 PrintTicket，所以您可能只想附加系統 PrintTicket 提供者明確支援的屬性實例。

4.  如果 Print Schema 關鍵字將特定功能的 SelectionType 屬性設定為 PickMany，您可以為該功能選取一個以上的選項，但前提是指定為 IdentityOption 的選項不是選取的選項之一。 列印架構中的 IdentityOption 與 Postscript PPD 檔案和 Unidrv GPD 檔案中的 [無] 選項有相同的效果;它是一種無作業的服務。

5.  檢查 ParameterDef 實例的列印架構關鍵字，這些實例應該在您的 PrintTicket 中初始化。 針對每個這類 ParameterDef 實例，選取要在 PrintTicket 的 ParameterInit 實例中使用的值。 這個值必須是正確的資料類型、必須落在 ParameterDef 實例中定義的範圍內，而且必須符合 ParameterDef 實例中指定的所有其他需求。 使用 ParameterInit 實例將參數初始化為您所選取的值。

    如果您要 (UI) 元件開發使用者介面，請設計您的 PrintTicket 產生方法，讓使用者可以輸入 ParameterInit 元素的值。 此外，UI 輸入方法應該觀察並符合相關聯 ParameterDef 專案所指定的任何輸入限制。

6.  檢查在 PrintTicket 中出現 ParameterRef 的每個選項實例的內容。 如果對應的 ParameterInit 實例尚未出現在 PrintTicket 中，請依照上一個步驟在 PrintTicket 中建立 ParameterInit 實例。 這個 ParameterInit 實例的目的是要初始化 ParameterRef 實例所參考的參數。

7.  請記住，處理作業的裝置可能不支援 PrintTicket 中指定的每項功能。 也請記住，可能會支援已命名的功能，但該功能的指定選項可能不會。 相同的警告適用于參數。 即使裝置支援具名引數，在 ParameterInit 實例中指定的值可能不在裝置的有效範圍內。

8.  檢查必須存在於您的 PrintTicket 中之屬性實例的列印架構關鍵字。 將每個屬性的屬性實例加入至您的 PrintTicket，並使用 Value 元素類型為其提供適當的值。 請確定屬性實例正確地放在 PrintTicket 內。 請確定您查閱了 PrintTicket 架構，而不是 PrintCapabilities 架構。

9.  檢查 PrintTicket 架構中定義的選擇性屬性實例。 如果您的 PrintTicket 中有任何這類屬性實例，請在您的 PrintTicket 中建立它們。

10. 相同專案類型的子系不可嵌套至超過10個元素的深度。 這項規則會獨立套用到每個可定義的元素類型。

> [!Note]  
> 必須使用 UTF-8 或 UTF-16 來編碼 PrintTicket XML 內容。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



