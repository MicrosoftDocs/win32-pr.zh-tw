---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player 線上商店，track.csv
- 線上商店、track.csv
- 輸入1個線上商店，track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301208"
---
# <a name="trackcsv"></a><span data-ttu-id="39fb3-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="39fb3-107">track.csv</span></span>

<span data-ttu-id="39fb3-108">此檔案包含目錄中每個追蹤的專案。</span><span class="sxs-lookup"><span data-stu-id="39fb3-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="39fb3-109">每個專案都是由下表所述定位字元分隔欄位所組成的資料列。</span><span class="sxs-lookup"><span data-stu-id="39fb3-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="39fb3-110">欄位必須依列出的順序出現。</span><span class="sxs-lookup"><span data-stu-id="39fb3-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="39fb3-111">下表中的 Format 資料行描述每個 Unicode 文字欄位的格式化方式。</span><span class="sxs-lookup"><span data-stu-id="39fb3-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="39fb3-112">它不會參考內容的資料類型。</span><span class="sxs-lookup"><span data-stu-id="39fb3-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="39fb3-113">例如，如果 [格式] 資料行中指出了整數，則表示該欄位包含表示整數值的 Unicode 字串，而不是實際的整數。</span><span class="sxs-lookup"><span data-stu-id="39fb3-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39fb3-114">欄位</span><span class="sxs-lookup"><span data-stu-id="39fb3-114">Field</span></span></th>
<th><span data-ttu-id="39fb3-115">必要</span><span class="sxs-lookup"><span data-stu-id="39fb3-115">Required</span></span></th>
<th><span data-ttu-id="39fb3-116">格式</span><span class="sxs-lookup"><span data-stu-id="39fb3-116">Format</span></span></th>
<th><span data-ttu-id="39fb3-117">描述</span><span class="sxs-lookup"><span data-stu-id="39fb3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39fb3-118">用於 trackid</span><span class="sxs-lookup"><span data-stu-id="39fb3-118">TrackID</span></span></td>
<td><span data-ttu-id="39fb3-119">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-119">Yes</span></span></td>
<td><span data-ttu-id="39fb3-120">非負整數。範例：32789</span><span class="sxs-lookup"><span data-stu-id="39fb3-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="39fb3-121">內容提供者所提供的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="39fb3-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="39fb3-122">必須小於 2 ^ 32。效能提示：如果指派給相同專輯追蹤的識別碼連續編號，目錄壓縮將會更有效率。</span><span class="sxs-lookup"><span data-stu-id="39fb3-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="39fb3-123">但是，不需要連續的專輯曲目編號。</span><span class="sxs-lookup"><span data-stu-id="39fb3-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-124">TrackTitle</span><span class="sxs-lookup"><span data-stu-id="39fb3-124">TrackTitle</span></span></td>
<td><span data-ttu-id="39fb3-125">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-125">Yes</span></span></td>
<td><span data-ttu-id="39fb3-126">Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="39fb3-126">Unicode string.</span></span> <span data-ttu-id="39fb3-127">範例： Raygun Robbers 的藍色</span><span class="sxs-lookup"><span data-stu-id="39fb3-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="39fb3-128">資料軌的名稱。</span><span class="sxs-lookup"><span data-stu-id="39fb3-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-129">持續時間</span><span class="sxs-lookup"><span data-stu-id="39fb3-129">Duration</span></span></td>
<td><span data-ttu-id="39fb3-130">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-130">Yes</span></span></td>
<td><span data-ttu-id="39fb3-131">非負整數。範例：543</span><span class="sxs-lookup"><span data-stu-id="39fb3-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="39fb3-132">追蹤的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="39fb3-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-133">TrackNumber</span><span class="sxs-lookup"><span data-stu-id="39fb3-133">TrackNumber</span></span></td>
<td><span data-ttu-id="39fb3-134">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-134">Yes</span></span></td>
<td><span data-ttu-id="39fb3-135">非負整數。範例：7</span><span class="sxs-lookup"><span data-stu-id="39fb3-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="39fb3-136">曲目專輯上的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="39fb3-136">Track number on the track's album.</span></span> <span data-ttu-id="39fb3-137">曲目編號從1開始，並在各磁片組之間增加。</span><span class="sxs-lookup"><span data-stu-id="39fb3-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="39fb3-138">曲目編號必須小於256。</span><span class="sxs-lookup"><span data-stu-id="39fb3-138">The track number must be less than 256.</span></span> <span data-ttu-id="39fb3-139">大於或等於256的曲目編號會在 Windows Media Player 中造成未預期的行為。</span><span class="sxs-lookup"><span data-stu-id="39fb3-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-140">TrackPrice</span><span class="sxs-lookup"><span data-stu-id="39fb3-140">TrackPrice</span></span></td>
<td><span data-ttu-id="39fb3-141">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-141">Yes</span></span></td>
<td><span data-ttu-id="39fb3-142">Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="39fb3-142">Unicode string.</span></span> <span data-ttu-id="39fb3-143">範例： $0.99。</span><span class="sxs-lookup"><span data-stu-id="39fb3-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="39fb3-144">追蹤價格。</span><span class="sxs-lookup"><span data-stu-id="39fb3-144">Track price.</span></span> <span data-ttu-id="39fb3-145">應包含貨幣符號。</span><span class="sxs-lookup"><span data-stu-id="39fb3-145">The currency symbol should be included.</span></span> <span data-ttu-id="39fb3-146">空字串0和-具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="39fb3-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="39fb3-147">空字串表示價格未知。</span><span class="sxs-lookup"><span data-stu-id="39fb3-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="39fb3-148">此欄位中的零表示曲目是免費的，而連字號 (-) 表示無法購買該曲目。</span><span class="sxs-lookup"><span data-stu-id="39fb3-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-149">CanStream</span><span class="sxs-lookup"><span data-stu-id="39fb3-149">CanStream</span></span></td>
<td><span data-ttu-id="39fb3-150">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-150">Yes</span></span></td>
<td><span data-ttu-id="39fb3-151">布林值。</span><span class="sxs-lookup"><span data-stu-id="39fb3-151">Boolean.</span></span> <span data-ttu-id="39fb3-152">可以是0或1。範例：0</span><span class="sxs-lookup"><span data-stu-id="39fb3-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="39fb3-153">指出是否可以串流處理此追蹤。</span><span class="sxs-lookup"><span data-stu-id="39fb3-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-154">CanDownload</span><span class="sxs-lookup"><span data-stu-id="39fb3-154">CanDownload</span></span></td>
<td><span data-ttu-id="39fb3-155">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-155">Yes</span></span></td>
<td><span data-ttu-id="39fb3-156">布林值。</span><span class="sxs-lookup"><span data-stu-id="39fb3-156">Boolean.</span></span> <span data-ttu-id="39fb3-157">可以是0或1。範例：0</span><span class="sxs-lookup"><span data-stu-id="39fb3-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="39fb3-158">指出是否可以下載此追蹤。</span><span class="sxs-lookup"><span data-stu-id="39fb3-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-159">HasPreviewClip</span><span class="sxs-lookup"><span data-stu-id="39fb3-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="39fb3-160">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-160">Yes</span></span></td>
<td><span data-ttu-id="39fb3-161">布林值。</span><span class="sxs-lookup"><span data-stu-id="39fb3-161">Boolean.</span></span> <span data-ttu-id="39fb3-162">可以是0或1。範例：0</span><span class="sxs-lookup"><span data-stu-id="39fb3-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="39fb3-163">指出曲目是否有預覽剪輯。</span><span class="sxs-lookup"><span data-stu-id="39fb3-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-164">HasVideoClip</span><span class="sxs-lookup"><span data-stu-id="39fb3-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="39fb3-165">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-165">Yes</span></span></td>
<td><span data-ttu-id="39fb3-166">布林值。</span><span class="sxs-lookup"><span data-stu-id="39fb3-166">Boolean.</span></span> <span data-ttu-id="39fb3-167">可以是0或1。範例：0</span><span class="sxs-lookup"><span data-stu-id="39fb3-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="39fb3-168">指出曲目是否有影片剪輯。</span><span class="sxs-lookup"><span data-stu-id="39fb3-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-169">ParentalRating</span><span class="sxs-lookup"><span data-stu-id="39fb3-169">ParentalRating</span></span></td>
<td><span data-ttu-id="39fb3-170">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-170">Yes</span></span></td>
<td><span data-ttu-id="39fb3-171">列舉。</span><span class="sxs-lookup"><span data-stu-id="39fb3-171">Enumeration.</span></span> <span data-ttu-id="39fb3-172">可以是 N、E 或 C。範例： N</span><span class="sxs-lookup"><span data-stu-id="39fb3-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="39fb3-173">指出家長諮詢評等。</span><span class="sxs-lookup"><span data-stu-id="39fb3-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="39fb3-174">N、E 和 C 的值為正常、明確和清除。</span><span class="sxs-lookup"><span data-stu-id="39fb3-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-175">LinkedAlbumID</span><span class="sxs-lookup"><span data-stu-id="39fb3-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="39fb3-176">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-176">Yes</span></span></td>
<td><span data-ttu-id="39fb3-177">非負整數。</span><span class="sxs-lookup"><span data-stu-id="39fb3-177">Non-negative integer.</span></span> <span data-ttu-id="39fb3-178">必須是專輯的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39fb3-178">Must be the ID of an Album.</span></span> <span data-ttu-id="39fb3-179">範例：32423</span><span class="sxs-lookup"><span data-stu-id="39fb3-179">Example: 32423</span></span></td>
<td><span data-ttu-id="39fb3-180">包含此播放軌之專輯的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39fb3-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="39fb3-181">每個播放軌都必須屬於一個專輯。</span><span class="sxs-lookup"><span data-stu-id="39fb3-181">Every track must belong to an album.</span></span> <span data-ttu-id="39fb3-182">也就是說，針對每個追蹤，LinkedAlbumID 欄位必須等於 album.csv 檔案中的其中一個專輯識別碼。</span><span class="sxs-lookup"><span data-stu-id="39fb3-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="39fb3-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="39fb3-184">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-184">Yes</span></span></td>
<td><span data-ttu-id="39fb3-185">整數的清單。</span><span class="sxs-lookup"><span data-stu-id="39fb3-185">List of integers.</span></span> <span data-ttu-id="39fb3-186">此清單包含演出者識別碼，並以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="39fb3-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="39fb3-187">範例： 41322; 12321;82123;</span><span class="sxs-lookup"><span data-stu-id="39fb3-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="39fb3-188">對應于參與演出者的識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="39fb3-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-189">編輯器</span><span class="sxs-lookup"><span data-stu-id="39fb3-189">Composer</span></span></td>
<td><span data-ttu-id="39fb3-190">No</span><span class="sxs-lookup"><span data-stu-id="39fb3-190">No</span></span></td>
<td><span data-ttu-id="39fb3-191">Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="39fb3-191">Unicode string.</span></span> <span data-ttu-id="39fb3-192">範例： Beethoven</span><span class="sxs-lookup"><span data-stu-id="39fb3-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="39fb3-193">播放軌的編輯器。如果追蹤的類型沒有設定 HasComposer 欄位，則會忽略編輯器欄位的值。</span><span class="sxs-lookup"><span data-stu-id="39fb3-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="39fb3-194">通常只用于爵士樂或傳統的曲目。</span><span class="sxs-lookup"><span data-stu-id="39fb3-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb3-195">熱門程度</span><span class="sxs-lookup"><span data-stu-id="39fb3-195">Popularity</span></span></td>
<td><span data-ttu-id="39fb3-196">Yes</span><span class="sxs-lookup"><span data-stu-id="39fb3-196">Yes</span></span></td>
<td><span data-ttu-id="39fb3-197">非負整數或浮點數。範例：1252。6</span><span class="sxs-lookup"><span data-stu-id="39fb3-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="39fb3-198">決定依熱門程度排序時，清單在清單中的位置。</span><span class="sxs-lookup"><span data-stu-id="39fb3-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="39fb3-199">較低的數位表示較熱門。</span><span class="sxs-lookup"><span data-stu-id="39fb3-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb3-200">>system.starrating.average</span><span class="sxs-lookup"><span data-stu-id="39fb3-200">StarRating</span></span></td>
<td><span data-ttu-id="39fb3-201">No</span><span class="sxs-lookup"><span data-stu-id="39fb3-201">No</span></span></td>
<td><span data-ttu-id="39fb3-202">Float。範例：4.21</span><span class="sxs-lookup"><span data-stu-id="39fb3-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="39fb3-203">星級評等會先 Windows Media Player 舍入至最接近的1/4 星形，然後才會顯示在 Windows Media Player 使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="39fb3-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





