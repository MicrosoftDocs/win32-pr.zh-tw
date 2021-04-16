---
description: 合併模組資料庫的主鍵名稱必須遵守標準命名慣例。
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: 命名合併模組資料庫中的主鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512780"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>命名合併模組資料庫中的主鍵

合併模組資料庫的主鍵名稱必須遵守標準命名慣例。 此命名慣例的目的是要降低在合併模組和目標安裝封裝的資料表資料行之間建立名稱衝突的可能性。 命名慣例無法套用至主要索引鍵是可安裝資料的資料表。 請勿將命名慣例套用至下列資料表：

-   [MIME 資料表](mime-table.md)
-   [延伸模組資料表](extension-table.md)
-   [圖示表](icon-table.md)
-   [動詞資料表](verb-table.md)
-   [ProgId 資料表](progid-table.md)

例如，請勿將用於 MIME 資料表的主鍵，因為這是 MIME 類型，而套用命名程式會變更其意義。 在這些情況下，名稱衝突取決於各模組之間唯一的資料意義。

合併模組中的主鍵名稱必須由可讀取的名稱所組成，並附加自合併模組之 GUID 所建立的字串。 每個合併模組都必須有自己的 [*GUID*](g-gly.md)。 合併模組的 GUID 也應該撰寫到合併模組的 [ [**修訂編號摘要**](revision-number-summary.md) ] 屬性中。 開發人員可以使用 GUIDGEN 之類的公用程式來建立 Guid。

下列程式描述如何產生遵守標準命名慣例的主資料庫索引鍵。 僅將下列程式套用至主要索引鍵不是安裝資料的資料表。

**在合併模組中命名資料表記錄的主鍵**

1.  撰寫主要金鑰名稱的可讀取部分。 挑選可識別此記錄的可讀取名稱，例如，MyRowEntry。
2.  產生或取得合併模組的 GUID。 請注意，所有 Guid 都必須以大寫撰寫。 如需有關 Guid 的詳細資訊，請參閱 [guid](guid.md)。 以下是 GUID： {880DE2F0-CDD8-11D1-A849-006097ABDE17} 的範例。 在下列步驟中，您會將此修改為必須附加至合併模組中每個主鍵名稱的字元字串。
3.  從 GUID 的開頭和結尾移除大括弧。
4.  將所有的連字號變更為底線。
5.  將結果附加至主要金鑰名稱可讀取部分的結尾。 以句點分隔已修改 GUID 的可讀取名稱。 上述範例 GUID 的主要金鑰名稱會變成 MyRowEntry. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17。
6.  重複以命名合併模組中所有資料表的所有主要索引鍵。

 

 



