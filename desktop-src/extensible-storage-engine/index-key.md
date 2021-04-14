---
description: 深入瞭解：索引鍵
title: 索引鍵
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568683"
---
# <a name="index-key"></a>索引鍵


_**適用于：** Windows |Windows Server_

## <a name="index-key"></a>索引鍵

建立索引時，會在具有[JetCreateIndex](./jetcreateindex-function.md)的資料表中建立資料，或使用[JET_INDEXCREATE](./jet-indexcreate-structure.md)結構，同時建立多個索引與[JetCreateIndex2](./jetcreateindex2-function.md) 。 索引是以依優先順序排列的資料行陣列來定義。 此資料行的陣列也稱為索引鍵。 當在 [JetCreateIndex](./jetcreateindex-function.md)或 [JET_INDEXCREATE](./jet-indexcreate-structure.md)的 *grbit* 參數中設定 JET_bitIndexPrimary 選項時，索引鍵可能會定義為主要索引。 索引鍵是 null 終止權杖的 null 結束字串，如下列範例所示：

\+Col1 \\ 0-Col2 \\ 0 + Col3 \\ 0 \\ 0

您可以使用範例中的索引鍵，在資料表中的三個數據行上建立索引。 索引中指定的每個資料行都稱為「索引區段」或「索引鍵資料行」。 索引區段可能是遞增或遞減的順序貢獻。 在上述範例中，索引中第一個資料行的名稱是 Col1。 + 表示 Col1 以遞增順序編制索引。 –之前的 Col2 表示以遞減順序編制索引。

當索引中出現條件資料行時，會使用 [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) 結構來指出如何編制索引。 條件式資料行可用來根據對應的條件式資料行中的值，控制索引中的索引項目目是否存在，而不會影響索引的排序次序。 如果對應記錄的條件式資料行值為 Null，條件資料行可能會包含或排除索引中的索引項目。

根據預設，索引鍵的大小上限是由 JET_cbKeyMost 常數所提供，其一律為255位元組的正規化資料 (位元組的資料，包括編制索引的額外負荷) 。 從 Windows Vista 開始，可以使用 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構來設定索引鍵的大小上限。 索引鍵的大小上限會對應到資料庫頁面大小。 若要啟用自訂的最大索引鍵大小，請在 [JET_INDEXCREATE](./jet-indexcreate-structure.md)的 grbits 成員中指定 Jet_bitIndexKeyMost 選項，然後將 **cbKeyMost** 成員設定為下列其中一個值：

  - JET_cbKeyMost2KBytePage：當資料庫頁面大小為2048個位元組時，最大的索引鍵大小可介於255個位元組之間，最大可達500個位元組。

  - JET_cbKeyMost4KBytePage：當資料庫頁面大小為4096個位元組時，最大的索引鍵大小可介於255個位元組之間，最大可達1000個位元組。

  - JET_cbKeyMost8KBytePage：當資料庫頁面大小為8196個位元組時，最大的索引鍵大小可介於255個位元組之間，最大可達2000個位元組。

下圖中的範例顯示包含員工資訊的資料表。 資料表有6個數據行，每個資料行都定義了特定的 employee 屬性。 資料表中的記錄包含員工的值，例如資料行1中的員工名稱和資料行2中的員工識別碼。 針對此資料表所建立的主要索引會根據員工名稱和員工識別碼（第二個）來組織資料。 名稱和識別碼都會以遞增的順序編制索引。 例如，包含名稱 Johnson 和員工識別碼12345的記錄會列在具有員工名稱的記錄之前，識別碼為10000。 所有的放置記錄都會一起儲存在資料表中，其員工識別碼的遞增順序如下表所示。

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

主要索引中的索引鍵必須是唯一的，但次要索引中的索引鍵可能是重複的。 例如，如果索引是以姓氏建立的，而且資料庫中有兩個使用者 Stevens，則當應用程式嘗試插入第二個 "Stevens" 時，ESE 會從 [JetUpdate](./jetupdate-function.md) 或 [JetUpdate2](./jetupdate2-function.md)傳回 Jet_errKeyDuplicate 錯誤。 當實際索引鍵大於最大金鑰大小時，就會截斷金鑰。 搜尋和唯一性的主要截斷效果，應該由應用程式管理。 例如，如果 "Stevens" 和 "Stevenson" 儲存于姓氏的索引中，而最大金鑰大小太小，無法儲存 "Stevenson" 的 "on" 部分，則金鑰截斷會導致資料庫引擎宣告 "Stevens" 和 "Stevenson" 是重複的，即使它們不是也是一樣。 如果索引定義和它所編制索引的資料行值都是可能的，應用程式必須準備好在搜尋和更新期間處理這類案例。 從 Windows Vista 開始，應用程式可以在 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 或 [JetMakeKey](./jetmakekey-function.md)中指定 Jet_bitIndexDisallowTruncation 選項。 指定此旗標會導致索引的任何更新會導致截斷的金鑰因 JET_errKeyTruncated 而失敗。 否則，將會以無訊息方式截斷金鑰。 這可讓應用程式在不考慮先前所述的金鑰截斷所造成的成品的情況下運作。
