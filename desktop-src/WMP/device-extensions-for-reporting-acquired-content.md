---
title: 用於報告取得內容的裝置擴充功能
description: 用於報告取得內容的裝置擴充功能
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player、裝置擴充功能
- Windows Media Player、延伸模組
- Windows Media Player，報告取得的內容
- 裝置擴充功能，報告取得的內容
- 擴充功能，報告取得的內容
- 報告取得的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831312457427cc9fe4ceed004772f3b174f77989
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965384"
---
# <a name="device-extensions-for-reporting-acquired-content"></a><span data-ttu-id="3035c-109">用於報告取得內容的裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="3035c-109">Device Extensions for Reporting Acquired Content</span></span>

<span data-ttu-id="3035c-110">Windows Media Player 11 引進了新功能，可讓可攜式裝置通知玩家自上次同步處理後新增至裝置的內容。</span><span class="sxs-lookup"><span data-stu-id="3035c-110">Windows Media Player 11 introduces new functionality that enables portable devices to notify the Player about content added to the device since the last synchronization.</span></span> <span data-ttu-id="3035c-111">Windows Media Player 11 可以使用此資訊，將新取得的內容從裝置複製到使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="3035c-111">Windows Media Player 11 can use this information to copy newly acquired content from the device to the user's computer.</span></span> <span data-ttu-id="3035c-112">裝置製造商應該注意下列支援這項功能的需求：</span><span class="sxs-lookup"><span data-stu-id="3035c-112">Device manufacturers should note the following requirements for supporting this functionality:</span></span>

-   <span data-ttu-id="3035c-113">只有已啟用 MTP 的裝置才支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="3035c-113">This feature is supported only for MTP-enabled devices.</span></span>
-   <span data-ttu-id="3035c-114">這項功能只適用于與 Windows Media Player 合作的裝置。</span><span class="sxs-lookup"><span data-stu-id="3035c-114">This feature works only with devices that have a partnership with Windows Media Player.</span></span>
-   <span data-ttu-id="3035c-115">裝置必須只報告裝置所撰寫或下載的內容。</span><span class="sxs-lookup"><span data-stu-id="3035c-115">Devices must report only content that the device authored or downloaded.</span></span> <span data-ttu-id="3035c-116">這包括裝置拍攝的相片;裝置所建立的錄音;語音信箱錄製;從儲存卡下載;以及從網際網路下載。</span><span class="sxs-lookup"><span data-stu-id="3035c-116">This includes photos taken by the device; voice recordings created by the device; voicemail recordings; downloads from a storage card; and downloads from the Internet.</span></span> <span data-ttu-id="3035c-117">由於與另一部裝置的同步處理或不同的合作關係，不應回報儲存在裝置上的內容。</span><span class="sxs-lookup"><span data-stu-id="3035c-117">Content that was stored on the device as a result of synchronization with another device or a different partnership must not be reported.</span></span>

<span data-ttu-id="3035c-118">名為 wmpdevices 的標頭檔（安裝為 Windows Media Player SDK 的一部分）會定義支援 Windows Media Player 裝置延伸模組所需的結構和常數。</span><span class="sxs-lookup"><span data-stu-id="3035c-118">The header file named wmpdevices.h, which is installed as part of the Windows Media Player SDK, defines the structures and constants needed to support Windows Media Player device extensions.</span></span>

<span data-ttu-id="3035c-119">若要將裝置辨識為支援透過 Windows Media Player MTP 裝置延伸模組設定取得內容的報告，必須在 DeviceInfo 資料集中包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="3035c-119">For a device to be recognized as supporting the reporting of acquired content through the Windows Media Player MTP device extension set, it must include the following information in the DeviceInfo dataset.</span></span> <span data-ttu-id="3035c-120"> (如需此資料集的詳細資訊，請參閱 MTP 規格的4.6.1 一節。 ) </span><span class="sxs-lookup"><span data-stu-id="3035c-120">(For more information about this dataset, see section 4.6.1 of the MTP specification.)</span></span>



| <span data-ttu-id="3035c-121">資料集欄位</span><span class="sxs-lookup"><span data-stu-id="3035c-121">Dataset field</span></span>          | <span data-ttu-id="3035c-122">欄位順序</span><span class="sxs-lookup"><span data-stu-id="3035c-122">Field order</span></span> | <span data-ttu-id="3035c-123">資料類型</span><span class="sxs-lookup"><span data-stu-id="3035c-123">Data type</span></span>  | <span data-ttu-id="3035c-124">值</span><span class="sxs-lookup"><span data-stu-id="3035c-124">Value</span></span>                       |
|------------------------|-------------|------------|-----------------------------|
| <span data-ttu-id="3035c-125">VendorExtensionID</span><span class="sxs-lookup"><span data-stu-id="3035c-125">VendorExtensionID</span></span>      | <span data-ttu-id="3035c-126">2</span><span class="sxs-lookup"><span data-stu-id="3035c-126">2</span></span>           | <span data-ttu-id="3035c-127">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3035c-127">**UINT32**</span></span> | <span data-ttu-id="3035c-128">0x00000006</span><span class="sxs-lookup"><span data-stu-id="3035c-128">0x00000006</span></span>                  |
| <span data-ttu-id="3035c-129">VendorExtensionVersion</span><span class="sxs-lookup"><span data-stu-id="3035c-129">VendorExtensionVersion</span></span> | <span data-ttu-id="3035c-130">3</span><span class="sxs-lookup"><span data-stu-id="3035c-130">3</span></span>           | <span data-ttu-id="3035c-131">**UINT16**</span><span class="sxs-lookup"><span data-stu-id="3035c-131">**UINT16**</span></span> | <span data-ttu-id="3035c-132">0x0064 (100) </span><span class="sxs-lookup"><span data-stu-id="3035c-132">0x0064 (100)</span></span>                |
| <span data-ttu-id="3035c-133">VendorExtensionDesc</span><span class="sxs-lookup"><span data-stu-id="3035c-133">VendorExtensionDesc</span></span>    | <span data-ttu-id="3035c-134">4</span><span class="sxs-lookup"><span data-stu-id="3035c-134">4</span></span>           | <span data-ttu-id="3035c-135">**String**</span><span class="sxs-lookup"><span data-stu-id="3035c-135">**String**</span></span> | <span data-ttu-id="3035c-136">"microsoft.com/WMPPD： 11.0"</span><span class="sxs-lookup"><span data-stu-id="3035c-136">"microsoft.com/WMPPD: 11.0"</span></span> |



 

<span data-ttu-id="3035c-137">下表提供報告所取得內容的 MTP 作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3035c-137">The following table provides details about the MTP operation for reporting acquired content.</span></span>



| <span data-ttu-id="3035c-138">項目</span><span class="sxs-lookup"><span data-stu-id="3035c-138">Item</span></span>                  | <span data-ttu-id="3035c-139">描述</span><span class="sxs-lookup"><span data-stu-id="3035c-139">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3035c-140">操作程式碼</span><span class="sxs-lookup"><span data-stu-id="3035c-140">Operation Code</span></span>        | <span data-ttu-id="3035c-141">0x9202</span><span class="sxs-lookup"><span data-stu-id="3035c-141">0x9202</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="3035c-142">Operation 參數1</span><span class="sxs-lookup"><span data-stu-id="3035c-142">Operation Parameter 1</span></span> | <span data-ttu-id="3035c-143">裝置在上一個會話期間提供的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="3035c-143">The transaction ID supplied by the device during the previous session.</span></span> <span data-ttu-id="3035c-144">第一個會話的這個值是零。</span><span class="sxs-lookup"><span data-stu-id="3035c-144">This value is zero for the first session.</span></span>                                                                                                                |
| <span data-ttu-id="3035c-145">Operation 參數2</span><span class="sxs-lookup"><span data-stu-id="3035c-145">Operation Parameter 2</span></span> | <span data-ttu-id="3035c-146">正在開始索引。</span><span class="sxs-lookup"><span data-stu-id="3035c-146">Starting index.</span></span> <span data-ttu-id="3035c-147">會話的第一次呼叫時，這個值一律為零。</span><span class="sxs-lookup"><span data-stu-id="3035c-147">This value is always zero on the first call of a session.</span></span> <span data-ttu-id="3035c-148">在相同同步處理會話中的後續呼叫上，此值會增加先前回應資料傳回的專案計數。</span><span class="sxs-lookup"><span data-stu-id="3035c-148">On subsequent calls within the same synchronization session, this value increases by the count of the items returned from the previous response data.</span></span> |
| <span data-ttu-id="3035c-149">Operation 參數3</span><span class="sxs-lookup"><span data-stu-id="3035c-149">Operation Parameter 3</span></span> | <span data-ttu-id="3035c-150">0x10000.</span><span class="sxs-lookup"><span data-stu-id="3035c-150">0x10000.</span></span> <span data-ttu-id="3035c-151">這個常數定義于 wmpdevices 中，這是可在回應中傳回的最大 PUOIDs 數。</span><span class="sxs-lookup"><span data-stu-id="3035c-151">This constant, defined in wmpdevices.h, is the maximum number of PUOIDs that can be returned in the response.</span></span> <span data-ttu-id="3035c-152">請注意，這個常數的值可能會在此標頭檔的未來版本中修訂。</span><span class="sxs-lookup"><span data-stu-id="3035c-152">Note that the value of this constant may be revised in future releases of this header file.</span></span>              |
| <span data-ttu-id="3035c-153">Operation 參數4</span><span class="sxs-lookup"><span data-stu-id="3035c-153">Operation Parameter 4</span></span> | <span data-ttu-id="3035c-154">0</span><span class="sxs-lookup"><span data-stu-id="3035c-154">0</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3035c-155">Operation 參數5</span><span class="sxs-lookup"><span data-stu-id="3035c-155">Operation Parameter 5</span></span> | <span data-ttu-id="3035c-156">0</span><span class="sxs-lookup"><span data-stu-id="3035c-156">0</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3035c-157">資料</span><span class="sxs-lookup"><span data-stu-id="3035c-157">Data</span></span>                  | <span data-ttu-id="3035c-158">裝置會傳回 MTP 陣列，其中包含已取得的 PUOIDs。</span><span class="sxs-lookup"><span data-stu-id="3035c-158">The device returns an MTP array containing PUOIDs that have been acquired.</span></span> <span data-ttu-id="3035c-159">陣列以 **DWORD** 值開頭，指出陣列中的專案計數，後面接著專案的陣列。</span><span class="sxs-lookup"><span data-stu-id="3035c-159">The array begins with a **DWORD** value indicating the count of items in the array, followed by the array of elements.</span></span>                               |
| <span data-ttu-id="3035c-160">資料方向</span><span class="sxs-lookup"><span data-stu-id="3035c-160">Data Direction</span></span>        | <span data-ttu-id="3035c-161">R->I</span><span class="sxs-lookup"><span data-stu-id="3035c-161">R->I</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="3035c-162">回應碼選項</span><span class="sxs-lookup"><span data-stu-id="3035c-162">Response Code Options</span></span> | <span data-ttu-id="3035c-163">**MTP \_回應 \_ 正常** (0x2001) 或有效的錯誤回應碼。</span><span class="sxs-lookup"><span data-stu-id="3035c-163">**MTP\_RESPONSE\_OK** (0x2001) or valid error response code.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="3035c-164">回應參數1</span><span class="sxs-lookup"><span data-stu-id="3035c-164">Response Parameter 1</span></span>  | <span data-ttu-id="3035c-165">目前的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="3035c-165">The current transaction ID.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="3035c-166">回應參數2</span><span class="sxs-lookup"><span data-stu-id="3035c-166">Response Parameter 2</span></span>  | <span data-ttu-id="3035c-167">未來要求所剩餘的 PUOIDs 數目。</span><span class="sxs-lookup"><span data-stu-id="3035c-167">The number of PUOIDs that remain to be retrieved by future requests.</span></span>                                                                                                                                                            |
| <span data-ttu-id="3035c-168">回應參數3</span><span class="sxs-lookup"><span data-stu-id="3035c-168">Response Parameter 3</span></span>  | <span data-ttu-id="3035c-169">包含狀態資訊的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="3035c-169">**DWORD** containing status information.</span></span> <span data-ttu-id="3035c-170">狀態會以位方式表示。</span><span class="sxs-lookup"><span data-stu-id="3035c-170">Status is indicated in a bitwise fashion.</span></span> <span data-ttu-id="3035c-171">如需所要使用之旗標的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3035c-171">See Remarks for information about flags to use.</span></span>                                                                                              |
| <span data-ttu-id="3035c-172">回應參數4</span><span class="sxs-lookup"><span data-stu-id="3035c-172">Response Parameter 4</span></span>  | <span data-ttu-id="3035c-173">0</span><span class="sxs-lookup"><span data-stu-id="3035c-173">0</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3035c-174">回應參數5</span><span class="sxs-lookup"><span data-stu-id="3035c-174">Response Parameter 5</span></span>  | <span data-ttu-id="3035c-175">0</span><span class="sxs-lookup"><span data-stu-id="3035c-175">0</span></span>                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="3035c-176">備註</span><span class="sxs-lookup"><span data-stu-id="3035c-176">Remarks</span></span>

<span data-ttu-id="3035c-177">狀態是透過使用下列旗標，以位方式透過回應參數3來表示。</span><span class="sxs-lookup"><span data-stu-id="3035c-177">Status is indicated through Response Parameter 3 in a bitwise fashion by using the following flag.</span></span>



| <span data-ttu-id="3035c-178">旗標</span><span class="sxs-lookup"><span data-stu-id="3035c-178">Flag</span></span>                                              | <span data-ttu-id="3035c-179">值</span><span class="sxs-lookup"><span data-stu-id="3035c-179">Value</span></span> | <span data-ttu-id="3035c-180">描述</span><span class="sxs-lookup"><span data-stu-id="3035c-180">Description</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3035c-181">**WMP \_ MDRT \_ 旗標未 \_ 報告的 \_ 取得 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="3035c-181">**WMP\_MDRT\_FLAGS\_UNREPORTED\_ACQUIRED\_ITEMS**</span></span> | <span data-ttu-id="3035c-182">0x1</span><span class="sxs-lookup"><span data-stu-id="3035c-182">0x1</span></span>   | <span data-ttu-id="3035c-183">裝置包含一些無法在 PUOIDS 清單中傳回的已取得專案。</span><span class="sxs-lookup"><span data-stu-id="3035c-183">The device contains some acquired items that cannot be returned in the list of PUOIDS.</span></span> <span data-ttu-id="3035c-184">請注意，此旗標不是重複的回應參數2。</span><span class="sxs-lookup"><span data-stu-id="3035c-184">Note that this flag is not redundant with Response Parameter 2.</span></span> <span data-ttu-id="3035c-185">只有當裝置無法傳回的要求專案時，才設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="3035c-185">Set this flag only when there are requested items that the device cannot return.</span></span> |



 

<span data-ttu-id="3035c-186">位1到31的保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3035c-186">Bits 1 through 31 are reserved for future use.</span></span> <span data-ttu-id="3035c-187">這些位應設定為零。</span><span class="sxs-lookup"><span data-stu-id="3035c-187">These bits should be set to zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3035c-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="3035c-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3035c-189">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="3035c-189">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




