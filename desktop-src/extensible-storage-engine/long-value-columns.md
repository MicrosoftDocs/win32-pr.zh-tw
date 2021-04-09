---
description: 深入瞭解： Long 值資料行
title: Long 值資料行
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026124"
---
# <a name="long-value-columns"></a>Long 值資料行


_**適用于：** Windows |Windows Server_

## <a name="long-value-columns"></a>Long 值資料行

ESE 資料行類型 JET_coltypLongText 和 JET_coltypLongBinary 稱為 long 值資料行類型。 這些資料行是大型字串和大型二進位物件，這些物件可能會儲存在不同的 B + 樹狀結構中，而不是主要索引。 當 long 值與主要記錄分開儲存時，它們會在內部以較長的值識別碼作為索引鍵， (蓋) 和位元組位移，然後以資料流程形式存取。 在 [JetAddColumn](./jetaddcolumn-function.md)的呼叫中，將 Long 值資料行新增至資料表，並將 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **coltyp** 成員設為 JET_coltypLongText 或 JET_coltypLongBinary。 長文字或長二進位資料行值的大小上限為 2 GB-1。

ESE 支援附加、位元組範圍覆寫，以及設定 long 值資料行的大小作業，以支援在這些資料行類型上有效率的資料流程執行。 依預設，如果長數值資料儲存在記錄中，則 [長值資料] 會儲存在另一個 B + 樹狀結構中（如果大於1024個位元組），或記錄不符合單一資料庫頁面。 應用程式可以選擇覆寫預設行為，方法是設定選項以將長數值資料儲存在記錄 (JET_bitSetIntrinsicLV) 或強制它們儲存在個別的 B + 樹 (JET_bitSetIntrinsicLV) 中。 這些值是在 [JetSetColumn](./jetsetcolumn-function.md)的 *grbit* 參數中設定，或是在 [JetSetColumns](./jetsetcolumns-function.md)呼叫中使用的 **grbit** 成員 [JET_SETCOLUMN](./jet-setcolumn-structure.md) ，如下所示：

  - 附加： (JET_bitSetAppendLV) 

  - 位元組範圍覆寫： (JET_bitSetOverwriteLV) 

  - 設定大小： (JET_bitSetSizeLV) 

  - 強制個別： (JET_bitSetSeparateLV) 

  - 存放區記錄： (JET_bitSetIntrinsicLV) 

Long 值資料的設定方式是將位移指出為 long 值 blob，並在 blob 中指出 long 值資料的長度。 Long 值 blob 的位移是設定在 [JET_SETINFO](./jet-setinfo-structure.md)結構 (的 **ibLongValue** 成員中，用於 [JetSetColumn](./jetsetcolumn-function.md)) 或 [JetSetColumns](./jetsetcolumns-function.md) (之 [JET_SETCOLUMN](./jet-setcolumn-structure.md)結構) 的 **ibLongValue** 成員。 [JET_SETCOLUMN](./jet-setcolumn-structure.md)的 **pvData** 成員，以及在 [JetSetColumn](./jetsetcolumn-function.md)的呼叫中， *pvData* 參數包含 long 值資料。 Long 值資料行的更新必須在交易內執行。

Long 值資料一律儲存在個別的資料表中，就是當應用程式設定 JET_bitSetSeparateLV 或 JET_bitSetIntrinsicLV 時，否則會啟發式地決定。 如果 ESE 儲存的長度超過1024個位元組，或如果記錄儲存在記錄中，則 ESE 儲存的 long 值會分開。

下圖顯示儲存在個別資料表中的長數值資料。 當長數值儲存在記錄之外時，會建立新的完整值識別碼來參考其值。 這可讓多個記錄參考相同的資料行值。 如果資料中有一個以上的記錄指向相同的 long 值資料，則資料的參考計數會增加。

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE 也支援單一實例存放區功能，可讓多個記錄參考相同的大型二進位物件，就像每一筆記錄都有自己的資訊複本一樣。因此，請避免重複的資料行值資料複本。 使用 *準備* 參數中設定的 JET_prepInsertCopy 選項，即可在 [JetPrepareUpdate](./jetprepareupdate-function.md)呼叫中啟用這項功能。
