---
description: 最佳檔案系統交易的建議。
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: 交易式 NTFS 的效能考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a71f7e100e1ddd8524932a4a259a12092bddcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944890"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>交易式 NTFS 的效能考慮

交易式 NTFS (TxF) 已針對效能進行謹慎設計，而且在類似案例下的一般用途交易替代方案通常會優於一般用途。 不過，檔案系統交易的額外負荷比非交易作業更多，而且與非交易 i/o 相較之下，i/o 效能的降低是預期的。 效能關鍵的應用程式應該執行技術採用的資格週期，以評估交易檔案系統作業的效能影響。

## <a name="overview-of-txf-operations"></a>TxF 作業總覽

如果發生交易中止，則 TxF 會使用 *復原* 記錄來記錄將檔案系統恢復為一致狀態（也稱為復原）所需的變更。 這項復原記錄會產生額外的 i/o，而且是與非交易式檔案系統作業相較之下，TxF 效能負荷的來源。

TxF 運作方式的高階摘要如下所示：

-   當交易進行時，TxF 會針對檔案系統所進行的每項修改，將 *恢復* 記錄寫入記錄檔中。 如果發生中止，則會剖析這些復原記錄，使檔案系統回到交易開始之前的狀態。
-   *中繼資料變更* 復原記錄只會描述檔案系統中繼資料的變更。 其中一些範例包括移動、重新命名、附加和屬性變更。 針對中繼資料變更復原記錄，復原變更所需的所有資訊都是在記錄中，並儲存在記錄檔中。
-   *覆寫* 復原記錄會描述檔案部分的覆寫。 當檔案遭到覆寫時，檔案的原始內容會儲存在隱藏目錄的特殊復原檔案中，而覆寫復原記錄會指向此檔案。 當檔案更新最後從快取排清到磁片時，也必須清除恢復檔案的內容，因此交易檔案覆寫可能會產生最多兩個額外的隨機 i/o 作業：一個用來讀取舊的資料，另一個則寫入恢復檔案。 這些額外的 i/o 作業是 TxF 的效能成本。
-   當認可發生時，TxF 會先清除所有復原資訊，然後清除實際的檔案變更，然後寫入和清除認可記錄。 如果沒有要排清的復原檔案，則會將記錄檔排清為相對於非交易 i/o 的唯一額外 TxF 負擔。 不過，記錄檔排清會導致有效率的大型連續寫入，因此效能成本最短。
-   TxF 已針對認可優化。 預期大部分的交易都將成功而不需要復原，因此交易的所有恢復記錄都應該不會使用。 從效能的觀點來看，TxF 認可作業很快就會復原，而且需要大量資源。
-   復原比認可更耗用資源。 在復原期間，交易中所做的所有變更都必須取消完成。 一般而言，復原持續時間可能與最初進行變更時所花費的時間大致相同。 例如，如果花了1秒鐘來進行所有變更，則可能需要約1秒才能復原它們。 針對非常長的交易，rollback 可能會造成額外的效能影響。 例如，如果系統必須在系統停止回應且必須執行未排程重新開機的事件中自動回復交易，系統開機時間可能會延遲。

有關可從上一個清單中繪製之效能的摘要結論如下所示：

-   針對涉及檔案覆寫的交易，TxF 的效能成本可能很重要。
-   僅涉及中繼資料作業之交易的 TxF 效能成本可能相對較低，但前提是使用大型交易。 大型交易是針對每個認可記錄有許多恢復記錄。

## <a name="recommendations-for-best-performance"></a>最佳效能建議

針對較大型的交易進行分攤 TxF 負擔。 例如，如果您有 *n* 個變更集，讓每個變更都有 *m* 個步驟，而且您可以選擇將它視為 *n* 個步驟的交易（每個步驟都有 m *個步驟*），或將其全部做為具有 *m* \* *N* 步驟的單一交易，則第二個選項會更有效率。

請考慮對非常大型交易的開機可能造成的影響。 如先前所述，復原可能會很慢，而且如果系統需要以開機時間執行自動回復，則會延遲開機時間。 交易愈大，延遲越久。

將交易保存到大部分的中繼資料作業。 這是 TxF 針對進行優化的功能，一般而言，效能與大型中繼資料交易的非交易式檔案 i/o 相同。 有效率的中繼資料 TxF 函式範例包括 [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)、 [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)、 [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)、 [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)、 [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)和附加的寫入 (呼叫 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 函式（當檔案指標是在檔案結尾時），或是 *EOF*) 。 當檔案指標不在 EOF 時，耗用大量資源的非中繼資料作業的範例就是呼叫 **WriteFile** 函式。

## <a name="summary-of-txf-performance-expectations"></a>TxF 效能預期的摘要

針對就地更新，覆寫檔案的區段會比非交易式檔案 i/o 慢許多，而檔案系統中繼資料作業的 TxF 效能 (例如，建立、移動和附加) 相當於大型交易的非交易式檔案 i/o。

 

 



