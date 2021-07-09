---
description: 瞭解 PrintCapabilities 架構中的選項定義。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: 選項定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc7dddb4840de8bc91c7f9ab127fd31319e5399
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549366"
---
# <a name="option-definitions"></a>選項定義

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

當您定義選項時，最重要的考慮就是這麼做，因為它可以有意義的方式，相較于相同功能中包含的其他選項實例。 比較必須有意義，因為選項實例是用來定義不只是裝置的設定，而不是與用於建立設定的裝置或 PrintCapabilities 無關的工作。 這項功能中的其他選項實例可能會出現在相同的 PrintCapabilities 檔中，或是另一個代表不同裝置的 PrintCapabilities 檔中，另一個合作物件所定義的 PrintCapabilities 檔會獨立運作。 在用戶端選取用來轉譯作業或檔的裝置設定之後，通常會以 PrintTicket 的形式儲存該設定以及作業或檔。 PrintTicket 包含一組選項實例，通常是 PrintCapabilities 檔中所定義之每項功能的一組。 選項實例必須是可移植的，而且必須保留列印意圖，如此一來，當這個 PrintTicket 提供給不同的裝置時，就可以傳達意圖，即使有不同的作者所撰寫的不同 PrintCapabilities 檔也是如此。 這種可攜性的主要優點是，如果不同的裝置並未特別支援 PrintTicket 中包含的選項，設備磁碟機或子系統就能識別並選取最接近功能的選項。

其中一個驅動程式的主要 PrintTicket 函數是識別 PrintCapabilities 檔中最符合 PrintTicket 所列特定選項的 [裝置] 選項。 在這個比對或設備磁碟機定義評分程式期間，PrintTicket 中的選項稱為 *參考* 選項，而 PrintCapabilities 檔中的選項則稱為 *候選* 選項。 一般比對度量是候選和參考選項實例中相符的 ScoredProperty 實例數目;較多的相符專案通常表示較妥善保留列印意圖。 在您的評分流程中，您可能會選擇對某些 ScoredProperty 元素提供較高的權數，而非其他專案。

您可以藉由確保屬於相同功能的所有選項實例都有一個或多個 ScoredProperty *元素*，讓您可以移植選項實例。 這表示每個選項實例中都會出現一組 ScoredProperty 元素， (屬於相同的功能) 。 例如，如果每個選項實例都包含定義內建 PageMediaSize 屬性的 ScoredProperty 元素，則 PageMediaSize 功能的選項實例可以是可移植的： MediaSizeWidth 和 MediaSizeHeight。 然後，設備磁碟機或子系統程式碼可以藉由比較這些 ScoredProperty 值的差異來判斷兩個選項實例的同意程度。 如果 PrintCapabilities 檔中沒有完全符合 PrintTicket 中的選項，設備磁碟機可以輕鬆地判斷並選取具有最相符媒體維度的選項。

在此情況下， (選項實例的兩個物件) 說，如果滿足下列三個條件，就會有 *相同* 的專案，或同等 *的元素。*

1.  這兩個元素屬於相同的元素類型。

2.  這兩個元素的 name 屬性相同 (或兩個專案都不包含名稱屬性) 。

3.  要比較之元素的父系鏈（由所考慮的兩個物件）必須滿足條件1和2。

例如，假設有兩個選項實例，其中每個都包含一個 ScoredProperty 實例，而且每個 ScoredProperty 實例都包含一個屬性實例。 明確地說，第一個條件的滿足 (兩個屬性實例的類型) 相同，而第三個條件的一部分符合 (屬性實例的父系是相同類型 ScoredProperty，而這些專案的父系也是相同類型) 的選項實例。 如果分別是屬性實例、ScoredProperty 實例和選項實例的名稱屬性，則兩個選項實例都有共通的元素。

上述步驟中，建立選項實例的第一個步驟是定義一組存在於大部分或所有選項實例中的 ScoredProperty 元素。 如果您的裝置設定屬性可以用標準功能表示， ([列印架構關鍵字]) 中所列的專案，請注意標準選項實例中常見的 ScoredProperty 元素。 您應確定您引入的任何新選項實例也都包含這些 ScoredProperty 元素。 您隨時都可以視需要新增其他 ScoredProperty 元素，以區分您的選項實例與標準選項實例。 如果有原因，您甚至可能會刪除一或多個常見的 ScoredProperty 元素，雖然這樣可以減少這類選項的可攜性。 當然，可攜性考慮建議使用未修改的標準選項實例，除非您的選項與標準選項實例之間有一些內部差異，而且必須反映在新的選項實例中。

下列範例說明您可能想要將 ScoredProperty 元素加入至選項實例的情況。 PageMediaSize 功能的所有標準選項實例都有共同的 MediaSizeWidth 和 MediaSizeHeight ScoredProperty 元素。 假設您的裝置可以透過將紙張 transversely (LongEdgeFirst) 或 longitudinally (ShortEdgeFirst) ，來支援其中一種標準信件媒體大小。 假設您不想要引入新的摘要方向功能來公開這種程度的自由度，可以改為修改字母的兩個 PageMediaSize 選項實例，以納入紙紙方向。 針對這兩個字母選項實例，請從標準 PageMediaSize 選項實例開始，然後加入新的 ScoredProperty 專案來代表 FeedDirection。 在一個選項實例中，將 FeedDirection ScoredProperty 設定為 LongEdgeFirst;在另一個選項實例中，將 FeedDirection 設定為 ShortEdgeFirst。 請注意，這些新的選項實例會維持其可攜性。 如果代表字母的選項，ShortEdgeFirst 會儲存至 PrintTicket，而選取的不同裝置僅支援字母標準選項，以轉譯作業，選項比對程式碼可以快速判斷標準選項字母是否最符合選項字母、ShortEdgeFirst。 這是最符合的原因，就是所有的 ScoredProperty 實例都同意，但不存在於字母標準選項中的 FeedDirection ScoredProperty 除外。

您也可能會遇到選項的修改實際變更意義，因此修改過的選項不會再被視為原始案例的特殊情況。 在這種情況下，您應該變更選項的名稱，以反映修改過的選項實例與未修改的選項實例之間的差異。 只有特定裝置的 PrintCapabilities 檔作者可以決定裝置所提供的選項是否與標準選項實例有足夠的差異，以保證不相容的定義。

現在請考慮您裝置的裝置設定屬性未對應到任何標準功能實例的情況。 在此情況下，您不能依賴標準選項實例來提供共同 ScoredProperty 元素的清單。 當您建立 ScoredProperty 實例時，您的主要目標是要區分功能中其他選項的每個選項，並說明為何使用者會選擇另一個選項。 基準是以唯一的 name 屬性來描述每個選項，而且保存 name 屬性的 ScoredProperty 會變成用來判斷通用元素的。

一旦建立了一組共通的 ScoredProperty 元素之後，將適當的值指派給每個 ScoredProperty，以建立每個選項是很簡單的事。 如同上述範例，針對特定的選項實例，您可能需要新增其他 ScoredProperty 實例，或刪除一些通用的元素，以建立適當的選項實例。

請注意，列印架構會要求 ScoredProperty 實例、其位置以及指派給選項中每個 ScoredProperty 的值，都必須保持不變，而不受設定影響。 列印架構的整個概念依賴選項實例，這些實例具有在許多裝置間共用的固定、可辨識的屬性和 ScoredProperty 實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



