---
description: '深入瞭解：交易 (Windows 事件) '
title: 交易 (Windows 事件)
TOCTitle: Transactions
ms:assetid: 1ceb362c-1efe-439b-b10a-016c8a54f27b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269197(v=EXCHG.10)
ms:contentKeyID: 32765500
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 90b5b566f5ff961ce7b0ae3725f580e1f39c041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319759"
---
# <a name="transactions-windows-events"></a>交易 (Windows 事件)


_**適用于：** Windows |Windows Server_

## <a name="transactions"></a>交易

ESE 交易是處理的邏輯單元，可控制應用程式如何查看和運算元據庫中的資料列。 您的應用程式可以使用交易儲存點來判斷是否要保留或捨棄資料庫的特定變更集。 ESE 中的所有交易都是不可部分完成、一致、隔離且持久的 (ACID) ，如下所述：

  - 不可部分完成 **：** 交易中的所有更新都會出現在資料庫中，或被捨棄。

<!-- end list -->

  - **一致：** 資料庫一律會以合法的狀態啟動，而且一律會以另一個合法的狀態結束。 若為 ESE 應用程式，database engine 將會控制一些簡單的條件約束，例如唯一索引的唯一性，但應用程式本身將會定義其代表資料庫處於合法狀態的所有其他層面。

<!-- end list -->

  - **隔離：** 交易與其他會話的更新隔離。 交易永遠不會看到一組由另一筆交易所做的部分變更。

<!-- end list -->

  - **耐用：** 在資料庫引擎確認交易已認可之後，其變更會在資料庫中持續存在。 基於效能考慮，可能會選擇性地放棄交易的持久性。

交易是在呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) 和 [JetCommitTransaction](./jetcommittransaction-function.md) 或 [JetRollback](./jetrollback-function.md)的範圍內執行。 當應用程式進入交易時，資料庫會在交易開始時出現在實例上。 這稱為快照集隔離。 如果透過呼叫 [JetRollback](./jetrollback-function.md)來終止交易，則在交易中執行的任何作業都不會認可至資料庫。 如果在呼叫 [JetCommitTransaction](./jetcommittransaction-function.md) 之前，進程或機器當機，則與呼叫 [JetRollback](./jetrollback-function.md)相同。

此程式示範如何啟動和認可交易，以讀取和更新資料庫中的資料。

### <a name="to-start-and-commit-a-transaction"></a>若要啟動和認可交易

1.  使用會話識別碼呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) 或 [JetBeginTransaction2](./jetbegintransaction2-function.md) ，以啟動交易。

2.  藉由呼叫 [JetMove](./jetmove-function.md) 與 *魚尾紋* 參數中指定的 JET_MoveFirst，將游標移到所需的記錄。 如需如何移動游標的詳細資訊，請參閱 [資料表主題中的索引](./indexing-in-the-table.md) 。

3.  使用 *InfoLevel* 參數中指定的 JET_ColInfo，在目前記錄上呼叫 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) ，以抓取資料行的資料行識別碼。 [JET_COLUMNDEF](./jet-columndef-structure.md)結構中會傳回資料行識別碼。

4.  使用已更新之資料行的會話識別碼、資料表識別碼和資料行識別碼來呼叫 [JetSetColumn](./jetsetcolumn-function.md) 。 資料行資料會包含在 *pvData* 參數中。

5.  呼叫 [JetCommitTransaction](./jetcommittransaction-function.md) 將交易認可到資料庫。

ESE 資料庫引擎執行快照集隔離的方式與傳統的關係資料庫隔離和鎖定模型有一些重要的差異。 當交易讀取資料列時，它一律可以存取該資料列，而不會發生失敗或等候其他會話釋放鎖定。 當交易嘗試更新資料列時，如果它是更新該資料列的第一個會話，也就是第一個寫入器獲勝，則會成功。 如果會話不是第一個寫入器，則會立即失敗，並產生寫入衝突錯誤。 然後，會話必須中止其交易、等候 (通常透過隨機延遲) ，讓其他交易認可其變更，然後重試交易。 資料庫引擎將不會自動導致該會話等到另一個交易完成其更新。 通常，交易會測試是否可以更新 [JetUpdate](./jetupdate-function.md) 呼叫內的資料列。 如果它無法鎖定資料列進行更新， [JetUpdate](./jetupdate-function.md) 將會失敗，並 JET_errWriteConflict。

從交易開始到交易結束時，會話會限制為一個執行緒。 建議您在交易中執行所有更新和取出作業。 ESE 也支援架構修改，例如建立資料表，以及在交易內加入資料行。 更新和架構修改都可以在相同交易中執行。 使用 [JetCommitTransaction](./jetcommittransaction-function.md)完成交易之後，更新會記錄在交易記錄檔中。 這些檔案可在發生未預期的進程終止或系統關機時，用來維護邏輯上一致的狀態。

交易最多可以嵌套至7個層級，並對[JetBeginTransaction](./jetbegintransaction-function.md)和[JetCommitTransaction](./jetcommittransaction-function.md)或 JetRollback 中的[](./jetrollback-function.md)進行互相對應的呼叫。 這可讓應用程式回復交易的一部分，而不需要離開整個交易。 [JetCommitTransaction](./jetcommittransaction-function.md)的嵌套呼叫表示此層級的處理已完成;不過，在外部最常呼叫以[JetCommitTransaction](./jetcommittransaction-function.md)認可交易之前，不會將交易認可到資料庫。

您可以透過多個會話同時更新「保管更新」資料行，而不會因 Jet_errWriteConflict 而失敗。 [JetEscrowUpdate](./jetescrowupdate-function.md)函式只能在已建立的資料行上呼叫，而這些資料行是使用 Jet_bitColumnEscrowUpdate 所建立。
