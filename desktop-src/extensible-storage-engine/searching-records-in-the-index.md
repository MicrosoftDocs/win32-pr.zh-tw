---
description: 深入瞭解：搜尋索引中的記錄
title: 搜尋索引中的記錄
TOCTitle: Searching Records in the Index
ms:assetid: 9141b1d6-81b6-49ad-a5d4-2409fe0d511a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269342(v=EXCHG.10)
ms:contentKeyID: 32765631
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 89a4ffe1f1c13280f236442ae218580fa5699741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971834"
---
# <a name="searching-records-in-the-index"></a>搜尋索引中的記錄


_**適用于：** Windows |Windows Server_

## <a name="searching-records-in-the-index"></a>搜尋索引中的記錄

系統會建立搜尋索引鍵，以搜尋索引中的單一專案或一組專案。 搜尋索引鍵只能針對索引中的索引鍵資料行而建立，而且可能包含一或多個資料行值。 搜尋索引鍵的建立方式為單一呼叫或一系列的 [JetMakeKey](./jetmakekey-function.md)呼叫，並且可使用 JET_bitRetrieveCopy 以 [JetRetrieveKey](./jetretrievekey-function.md) 抓取。 在建立搜尋索引鍵之後，您可以使用它將資料指標移至索引中的記錄。

有三種方法可在資料表中尋找記錄：

1.  搜尋單一索引項目。 若要這樣做，請使用 [JetMakeKey](./jetmakekey-function.md)建立搜尋金鑰，然後使用 [JetSeek](./jetseek-function.md)移至該記錄。

2.  依記錄搜尋索引記錄。 您可以呼叫 [JetMove](./jetmove-function.md)，一次一筆記錄一筆記錄。 您可以在 [JetMove](./jetmove-function.md)的 [*魚尾紋*] 參數中指定 JET_MoveFirst，將資料指標移至索引中的第一筆記錄。 同樣地，資料指標可以向前、向後或移至索引中的最後一個專案。

3.  搜尋一組記錄。 若要這樣做，請設定要搜尋的索引項目範圍，然後依序移動記錄。 For more information, see [Searching Through a Set of Records]() section of this topic.

### <a name="searching-through-a-set-of-records"></a>搜尋一組記錄

這裡的圖表顯示資料指標，會在呼叫 [JetSeek](./jetseek-function.md) 和 [JetSetIndexRange](./jetsetindexrange-function.md)的呼叫所定義的索引項目範圍內移動。

使用下列程式來搜尋索引中的一組記錄。

### <a name="to-search-a-set-of-records-in-an-index"></a>搜尋索引中的一組記錄

1.  針對要使用 [JetMakeKey](./jetmakekey-function.md)搜尋的記錄集內的第一筆記錄，建立搜尋索引鍵。

2.  使用 [JetSeek](./jetseek-function.md)將游標移至搜尋索引鍵中指定的記錄。

3.  使用 [JetMakeKey](./jetmakekey-function.md)為範圍中的最後一個索引項目建立另一個搜尋索引鍵。

4.  使用在步驟3中建立的索引鍵，設定 [JetSetIndexRange](./jetsetindexrange-function.md) 的索引範圍。

5.  呼叫 [JetMove](./jetmove-function.md) 以依序在索引範圍中的每筆記錄移動，如下圖所示。

![ESE_Documentation_IndexRange](images/Gg269342.ESE_Documentation_IndexRange(EXCHG.10).gif "ESE_Documentation_IndexRange")

圖中的資料指標只能移動至 [JetSetIndexRange](./jetsetindexrange-function.md)呼叫中所設定的索引範圍。 如果應用程式嘗試將資料指標移到索引範圍之外，ESE 會從呼叫 [JetMove](./jetmove-function.md)傳回 Jet_errNoCurrentRecord 錯誤。 請注意，除了移至下一個或上一個記錄之外，任何與此資料指標的導覽類型都會取消索引範圍。 如需詳細資訊，請參閱 [JetSetIndexRange](./jetsetindexrange-function.md) 。

在 [JetMakeKey](./jetmakekey-function.md)的 *pvData* 參數中輸入的資料類型，必須符合針對資料行所指定的資料類型和屬性。 例如，在資料行 JET_coltypText 類型的 *pvData* 參數中指定 "Ben 莎莎" 來呼叫 [JetMakeKey](./jetmakekey-function.md)是有效的資料類型相符。 如果您想要建立搜尋索引鍵，以在索引中的名稱 "Ben 莎莎" 和 "Max Stevens" 之間搜尋，請呼叫 [JetSeek](./jetseek-function.md)，將資料指標移至名稱為 "ben 莎莎" 的記錄。 第二次呼叫 [JetMakeKey](./jetmakekey-function.md) ，並指定包含 "Max Stevens" 名稱之字串的指標。 索引範圍設定為限制資料指標在呼叫 [JetSetIndexRange](./jetsetindexrange-function.md)時，于名稱 "Ben 莎莎" 和 "Max Stevens" 之間移動。
