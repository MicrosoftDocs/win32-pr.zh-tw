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
# <a name="using-uniscribe"></a><span data-ttu-id="35b66-103">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="35b66-103">Using Uniscribe</span></span>

<span data-ttu-id="35b66-104">Uniscribe 提供 Api 來支援印刷樣式，並支援顯示和編輯國際文字，包括中東和亞洲腳本的複雜規則。</span><span class="sxs-lookup"><span data-stu-id="35b66-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="35b66-105">Uniscribe 提供低層級常式來處理完整格式化的文字，以及針對未格式化的文字設定簡單的 ScriptString API。</span><span class="sxs-lookup"><span data-stu-id="35b66-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="35b66-106">使用 Uniscribe 時，應用程式只需要管理 Unicode 字元碼的備份存放區。</span><span class="sxs-lookup"><span data-stu-id="35b66-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="35b66-107">文字版面配置應用程式不需要維護任何其他緩衝區或對應表來追蹤字元順序。</span><span class="sxs-lookup"><span data-stu-id="35b66-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="35b66-108">每個應用程式只需要儲存和管理使用者輸入字元的順序，此順序與 Unicode 所定義的邏輯順序相同。</span><span class="sxs-lookup"><span data-stu-id="35b66-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="35b66-109">因為版面配置作業的結果，備份存放區永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="35b66-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="35b66-110">Uniscribe 會維護索引，從重新排序的叢集到應用程式所傳遞的原始字元界限。</span><span class="sxs-lookup"><span data-stu-id="35b66-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="35b66-111">本節涵蓋下列主題。</span><span class="sxs-lookup"><span data-stu-id="35b66-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="35b66-112">**塑形**</span><span class="sxs-lookup"><span data-stu-id="35b66-112">**Shaping**</span></span>

-   [<span data-ttu-id="35b66-113">判斷腳本是否需要圖像成形</span><span class="sxs-lookup"><span data-stu-id="35b66-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="35b66-114">使用成形引擎</span><span class="sxs-lookup"><span data-stu-id="35b66-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="35b66-115">**其他處理**</span><span class="sxs-lookup"><span data-stu-id="35b66-115">**Other Processing**</span></span>

-   [<span data-ttu-id="35b66-116">Caching</span><span class="sxs-lookup"><span data-stu-id="35b66-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="35b66-117">使用 Uniscribe 顯示文字</span><span class="sxs-lookup"><span data-stu-id="35b66-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="35b66-118">處理複雜的腳本</span><span class="sxs-lookup"><span data-stu-id="35b66-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="35b66-119">使用字型回復</span><span class="sxs-lookup"><span data-stu-id="35b66-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="35b66-120">使用 ScriptString 函數</span><span class="sxs-lookup"><span data-stu-id="35b66-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="35b66-121">**插入點**</span><span class="sxs-lookup"><span data-stu-id="35b66-121">**Caret**</span></span>

-   [<span data-ttu-id="35b66-122">以雙向字串顯示插入號</span><span class="sxs-lookup"><span data-stu-id="35b66-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="35b66-123">管理插入號放置和點擊測試</span><span class="sxs-lookup"><span data-stu-id="35b66-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="35b66-124">將滑鼠點擊次數 X 位移轉換成插入號位置</span><span class="sxs-lookup"><span data-stu-id="35b66-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="35b66-125">**單字和字元叢集**</span><span class="sxs-lookup"><span data-stu-id="35b66-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="35b66-126">使用字元叢集</span><span class="sxs-lookup"><span data-stu-id="35b66-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="35b66-127">使用斷詞點</span><span class="sxs-lookup"><span data-stu-id="35b66-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="35b66-128">使用插入號位置、對齊點和叢集之間的關聯性</span><span class="sxs-lookup"><span data-stu-id="35b66-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



