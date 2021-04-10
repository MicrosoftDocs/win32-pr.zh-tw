---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player 線上商店，list.csv
- 線上商店、list.csv
- 輸入1個線上商店，list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092530"
---
# <a name="listcsv"></a><span data-ttu-id="08330-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="08330-107">list.csv</span></span>

<span data-ttu-id="08330-108">此檔案包含目錄包含的每個清單專案。</span><span class="sxs-lookup"><span data-stu-id="08330-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="08330-109">清單可以是曲目、專輯、演出者、流派、subgenres 或廣播的清單;或者也可以是其他清單的清單。</span><span class="sxs-lookup"><span data-stu-id="08330-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="08330-110">每個清單專案都是由下表所述定位字元分隔欄位所組成的資料列。</span><span class="sxs-lookup"><span data-stu-id="08330-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="08330-111">欄位必須依列出的順序出現。</span><span class="sxs-lookup"><span data-stu-id="08330-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="08330-112">下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="08330-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="08330-113">它不會參考內容的資料類型。</span><span class="sxs-lookup"><span data-stu-id="08330-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="08330-114">例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。</span><span class="sxs-lookup"><span data-stu-id="08330-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08330-115">欄位</span><span class="sxs-lookup"><span data-stu-id="08330-115">Field</span></span></th>
<th><span data-ttu-id="08330-116">必要</span><span class="sxs-lookup"><span data-stu-id="08330-116">Required</span></span></th>
<th><span data-ttu-id="08330-117">格式</span><span class="sxs-lookup"><span data-stu-id="08330-117">Format</span></span></th>
<th><span data-ttu-id="08330-118">描述</span><span class="sxs-lookup"><span data-stu-id="08330-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08330-119">ListID</span><span class="sxs-lookup"><span data-stu-id="08330-119">ListID</span></span></td>
<td><span data-ttu-id="08330-120">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-120">Yes</span></span></td>
<td><span data-ttu-id="08330-121">非負整數。</span><span class="sxs-lookup"><span data-stu-id="08330-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="08330-122">清單識別碼，在 list.csv 中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="08330-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="08330-123">必須為非負數且小於 2 ^ 32。<strong>在樹狀檢視控制項中顯示清單節點：</strong> 如果 ListID 為0、1、2、3、4、5、6或7，則清單會在您的線上商店的樹狀檢視控制項中，顯示為您的線上商店最上層節點下的自訂節點。</span><span class="sxs-lookup"><span data-stu-id="08330-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="08330-124">自訂節點會出現在線上商店最上層節點下的標準節點之前，並依 ListID 以遞增順序放置。</span><span class="sxs-lookup"><span data-stu-id="08330-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="08330-125">例如，如果有三個自訂節點（Listid 為1、3和5），則會在線上商店的最上層節點下顯示第一、第二和第三個節點。</span><span class="sxs-lookup"><span data-stu-id="08330-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-126">>listtitle</span><span class="sxs-lookup"><span data-stu-id="08330-126">ListTitle</span></span></td>
<td><span data-ttu-id="08330-127">No</span><span class="sxs-lookup"><span data-stu-id="08330-127">No</span></span></td>
<td><span data-ttu-id="08330-128">Unicode 字串。範例：十大點擊數</span><span class="sxs-lookup"><span data-stu-id="08330-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="08330-129">清單標題。</span><span class="sxs-lookup"><span data-stu-id="08330-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08330-130">ListSubtitle</span><span class="sxs-lookup"><span data-stu-id="08330-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="08330-131">No</span><span class="sxs-lookup"><span data-stu-id="08330-131">No</span></span></td>
<td><span data-ttu-id="08330-132">Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="08330-132">Unicode string</span></span></td>
<td><span data-ttu-id="08330-133">列出替代標題，顯示在磚視圖的第二行中。</span><span class="sxs-lookup"><span data-stu-id="08330-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-134">ListDescription</span><span class="sxs-lookup"><span data-stu-id="08330-134">ListDescription</span></span></td>
<td><span data-ttu-id="08330-135">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-135">Yes</span></span></td>
<td><span data-ttu-id="08330-136">Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="08330-136">Unicode string</span></span></td>
<td><span data-ttu-id="08330-137">列出在 [屬性頁]) 中顯示的易記顯示文字 (。</span><span class="sxs-lookup"><span data-stu-id="08330-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08330-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="08330-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="08330-139">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-139">Yes</span></span></td>
<td><span data-ttu-id="08330-140">Unicode 字串。格式： [T |P |A |L | G |S |桌上型電腦主機板</span><span class="sxs-lookup"><span data-stu-id="08330-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="08330-141">範例： T</span><span class="sxs-lookup"><span data-stu-id="08330-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="08330-142">指出連結專案的型別。</span><span class="sxs-lookup"><span data-stu-id="08330-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="08330-143">T = 追蹤</span><span class="sxs-lookup"><span data-stu-id="08330-143">T= Track</span></span></li>
<li><span data-ttu-id="08330-144">P = 執行者</span><span class="sxs-lookup"><span data-stu-id="08330-144">P = Performer</span></span></li>
<li><span data-ttu-id="08330-145">A = 專輯</span><span class="sxs-lookup"><span data-stu-id="08330-145">A = Album</span></span></li>
<li><span data-ttu-id="08330-146">L = 清單</span><span class="sxs-lookup"><span data-stu-id="08330-146">L = List</span></span></li>
<li><span data-ttu-id="08330-147">G = 內容類型</span><span class="sxs-lookup"><span data-stu-id="08330-147">G = Genre</span></span></li>
<li><span data-ttu-id="08330-148">S = Subgenre</span><span class="sxs-lookup"><span data-stu-id="08330-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="08330-149">R = 選項按鈕</span><span class="sxs-lookup"><span data-stu-id="08330-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="08330-150">ListPrice</span></span></td>
<td><span data-ttu-id="08330-151">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-151">Yes</span></span></td>
<td><span data-ttu-id="08330-152">Unicode 字串。範例： $9.99</span><span class="sxs-lookup"><span data-stu-id="08330-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="08330-153">清單的價格。</span><span class="sxs-lookup"><span data-stu-id="08330-153">Price of the list.</span></span> <span data-ttu-id="08330-154">應包含貨幣符號。零表示清單是免費的。</span><span class="sxs-lookup"><span data-stu-id="08330-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="08330-155">無值表示價格不明。</span><span class="sxs-lookup"><span data-stu-id="08330-155">No value means the price is unknown.</span></span> <span data-ttu-id="08330-156">連字號表示無法購買清單。</span><span class="sxs-lookup"><span data-stu-id="08330-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08330-157">熱門程度</span><span class="sxs-lookup"><span data-stu-id="08330-157">Popularity</span></span></td>
<td><span data-ttu-id="08330-158">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-158">Yes</span></span></td>
<td><span data-ttu-id="08330-159">整數或十進位值。範例：1259。3</span><span class="sxs-lookup"><span data-stu-id="08330-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="08330-160">指出此清單出現在其他清單中的熱門等級。</span><span class="sxs-lookup"><span data-stu-id="08330-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="08330-161">如果不適用，則可以為零。</span><span class="sxs-lookup"><span data-stu-id="08330-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-162">IsRecentlyAdded</span><span class="sxs-lookup"><span data-stu-id="08330-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="08330-163">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-163">Yes</span></span></td>
<td><span data-ttu-id="08330-164">布林值。格式： [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="08330-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="08330-165">範例：0</span><span class="sxs-lookup"><span data-stu-id="08330-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="08330-166">指出最近是否加入清單。</span><span class="sxs-lookup"><span data-stu-id="08330-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08330-167">IsFeatured</span><span class="sxs-lookup"><span data-stu-id="08330-167">IsFeatured</span></span></td>
<td><span data-ttu-id="08330-168">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-168">Yes</span></span></td>
<td><span data-ttu-id="08330-169">布林值。格式： [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="08330-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="08330-170">範例：0</span><span class="sxs-lookup"><span data-stu-id="08330-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="08330-171">指出清單是否為精選。</span><span class="sxs-lookup"><span data-stu-id="08330-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="08330-172">可以用來決定排序次序。</span><span class="sxs-lookup"><span data-stu-id="08330-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-173">EditorialGlyph</span><span class="sxs-lookup"><span data-stu-id="08330-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="08330-174">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-174">Yes</span></span></td>
<td><span data-ttu-id="08330-175">非負整數。</span><span class="sxs-lookup"><span data-stu-id="08330-175">Non-negative integer.</span></span> <span data-ttu-id="08330-176">應為0。</span><span class="sxs-lookup"><span data-stu-id="08330-176">Should be 0.</span></span></td>
<td><span data-ttu-id="08330-177">未在此版本中使用。</span><span class="sxs-lookup"><span data-stu-id="08330-177">Not used in this release.</span></span> <span data-ttu-id="08330-178">應為0。</span><span class="sxs-lookup"><span data-stu-id="08330-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08330-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="08330-179">ViewType</span></span></td>
<td><span data-ttu-id="08330-180">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-180">Yes</span></span></td>
<td><span data-ttu-id="08330-181">Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="08330-181">Unicode string.</span></span> <span data-ttu-id="08330-182">格式： [I | T |R |L | O] 範例： T</span><span class="sxs-lookup"><span data-stu-id="08330-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="08330-183">表示要用於清單的檢視類型。</span><span class="sxs-lookup"><span data-stu-id="08330-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="08330-184">I = 圖示</span><span class="sxs-lookup"><span data-stu-id="08330-184">I = Icon</span></span></li>
<li><span data-ttu-id="08330-185">T = 磚</span><span class="sxs-lookup"><span data-stu-id="08330-185">T = Tile</span></span></li>
<li><span data-ttu-id="08330-186">R = 報表</span><span class="sxs-lookup"><span data-stu-id="08330-186">R = Report</span></span></li>
<li><span data-ttu-id="08330-187">L = 清單</span><span class="sxs-lookup"><span data-stu-id="08330-187">L = List</span></span></li>
<li><span data-ttu-id="08330-188">O = 已排序清單</span><span class="sxs-lookup"><span data-stu-id="08330-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-189">ViewImageSize</span><span class="sxs-lookup"><span data-stu-id="08330-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="08330-190">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-190">Yes</span></span></td>
<td><span data-ttu-id="08330-191">非負整數。範例：180</span><span class="sxs-lookup"><span data-stu-id="08330-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="08330-192">顯示清單影像的大小。</span><span class="sxs-lookup"><span data-stu-id="08330-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="08330-193">如果為0，則會自動決定大小。</span><span class="sxs-lookup"><span data-stu-id="08330-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08330-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="08330-194">GroupBy</span></span></td>
<td><span data-ttu-id="08330-195">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-195">Yes</span></span></td>
<td><span data-ttu-id="08330-196">Unicode 字串。格式： [-|P |A |C | R |D</span><span class="sxs-lookup"><span data-stu-id="08330-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="08330-197">範例： P</span><span class="sxs-lookup"><span data-stu-id="08330-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="08330-198">指出用來將清單中的專案分組的欄位。</span><span class="sxs-lookup"><span data-stu-id="08330-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="08330-199">- = 自動</span><span class="sxs-lookup"><span data-stu-id="08330-199">- = Automatic</span></span></li>
<li><span data-ttu-id="08330-200">P = 執行者</span><span class="sxs-lookup"><span data-stu-id="08330-200">P = Performer</span></span></li>
<li><span data-ttu-id="08330-201">A = 專輯</span><span class="sxs-lookup"><span data-stu-id="08330-201">A = Album</span></span></li>
<li><span data-ttu-id="08330-202">C = 編輯器</span><span class="sxs-lookup"><span data-stu-id="08330-202">C = Composer</span></span></li>
<li><span data-ttu-id="08330-203">R = 評等</span><span class="sxs-lookup"><span data-stu-id="08330-203">R = Rating</span></span></li>
<li><span data-ttu-id="08330-204">D = 日期</span><span class="sxs-lookup"><span data-stu-id="08330-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08330-205">ListItemsAreDynamic</span><span class="sxs-lookup"><span data-stu-id="08330-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="08330-206">Yes</span><span class="sxs-lookup"><span data-stu-id="08330-206">Yes</span></span></td>
<td><span data-ttu-id="08330-207">布林值。</span><span class="sxs-lookup"><span data-stu-id="08330-207">Boolean.</span></span> <span data-ttu-id="08330-208">可以是0或1。</span><span class="sxs-lookup"><span data-stu-id="08330-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="08330-209">指出是否動態產生清單。</span><span class="sxs-lookup"><span data-stu-id="08330-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="08330-210">動態清單在 listitem.csv 中沒有專案。</span><span class="sxs-lookup"><span data-stu-id="08330-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="08330-211">如果清單標示為動態，則其專案會由 <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner：： GetListContents 提供。</a></span><span class="sxs-lookup"><span data-stu-id="08330-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





