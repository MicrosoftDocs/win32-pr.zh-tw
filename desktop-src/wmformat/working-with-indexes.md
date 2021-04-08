---
title: 使用索引
description: 使用索引
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK，索引
- Advanced Systems Format (ASF) 、索引
- ASF (Advanced Systems Format) ，索引
- 索引，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839648"
---
# <a name="working-with-indexes"></a>使用索引

Windows Media Format SDK 支援透過內容搜尋和是昂首闊步。 搜尋可讓您指定檔案時間軸上的位置以開始播放。 是昂首闊步可讓您向前快轉和倒轉檔案的輸出。 您必須編制檔案的索引，才能利用這些功能。 索引是一系列的值，代表檔案中的位置 (呈現時間、框架數或 SMTPE 時間碼) ，其中每個都有相對應的位移至檔案的資料區段。 對於影片串流來說最重要的是，因為可以輕鬆地估計音訊串流呈現時間。 不過，某些音訊串流也可能需要索引。 根據預設，寫入器會為每個新的 ASF 檔案編制索引。 如果對檔案內容進行變更，您必須使用索引子物件自行重新整理索引。

索引子支援時態和以框架為基礎的索引編制，以及根據 SMPTE 時間代碼編制索引 (如果存在) 。 寫入器預設會針對編碼為檔案的每個新影片資料流程建立時態索引。 您必須明確地設定和呼叫索引子，以建立以框架為基礎或 SMPTE 時間的程式碼索引。

對 ASF 檔案的內容進行變更時，必須重新編制其索引。

下列各節提供執行一般編制索引工作的範例程式碼。

-   [停用自動編制索引](to-disable-automatic-indexing.md)
-   [設定索引子](to-configure-the-indexer.md)
-   [為 ASF 檔案編制索引](to-index-an-asf-file.md)
-   [若要停止進行編制索引](to-stop-indexing-in-progress.md)

此外，DSCopy 範例應用程式會示範如何使用索引子。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

 

 




