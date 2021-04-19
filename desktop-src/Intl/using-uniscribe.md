---
description: Uniscribe 提供 Api 來支援印刷樣式，並支援顯示和編輯國際文字，包括中東和亞洲腳本的複雜規則。
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: 使用 Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986399"
---
# <a name="using-uniscribe"></a>使用 Uniscribe

Uniscribe 提供 Api 來支援印刷樣式，並支援顯示和編輯國際文字，包括中東和亞洲腳本的複雜規則。 Uniscribe 提供低層級常式來處理完整格式化的文字，以及針對未格式化的文字設定簡單的 ScriptString API。

使用 Uniscribe 時，應用程式只需要管理 Unicode 字元碼的備份存放區。 文字版面配置應用程式不需要維護任何其他緩衝區或對應表來追蹤字元順序。 每個應用程式只需要儲存和管理使用者輸入字元的順序，此順序與 Unicode 所定義的邏輯順序相同。 因為版面配置作業的結果，備份存放區永遠不會變更。 Uniscribe 會維護索引，從重新排序的叢集到應用程式所傳遞的原始字元界限。

本節涵蓋下列主題。

**塑形**

-   [判斷腳本是否需要圖像成形](determining-if-a-script-requires-glyph-shaping.md)
-   [使用成形引擎](using-shaping-engines.md)

**其他處理**

-   [Caching](caching.md)
-   [使用 Uniscribe 顯示文字](displaying-text-with-uniscribe.md)
-   [處理複雜的腳本](processing-complex-scripts.md)
-   [使用字型回復](using-font-fallback.md)
-   [使用 ScriptString 函數](using-the-scriptstring-functions.md)

**插入點**

-   [以雙向字串顯示插入號](displaying-the-caret-in-bidirectional-strings.md)
-   [管理插入號放置和點擊測試](managing-caret-placement-and-hit-testing.md)
-   [將滑鼠點擊次數 X 位移轉換成插入號位置](translating-mouse-hit-x-offset-to-caret-position.md)

**單字和字元叢集**

-   [使用字元叢集](using-character-clusters.md)
-   [使用斷詞點](using-word-break-points.md)
-   [使用插入號位置、對齊點和叢集之間的關聯性](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



