---
title: 播放清單物件喜好設定的裝置擴充功能
description: 播放清單物件喜好設定的裝置擴充功能
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player、裝置擴充功能
- Windows Media Player、延伸模組
- Windows Media Player，播放清單物件喜好設定
- 裝置延伸模組，播放清單物件喜好設定
- 延伸模組，播放清單物件喜好設定
- 播放清單物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd9c6301e33307fc49e50b8aa9042752e020e32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674688"
---
# <a name="device-extensions-for-playlist-object-preferences"></a><span data-ttu-id="e0fab-109">播放清單物件喜好設定的裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="e0fab-109">Device Extensions for Playlist Object Preferences</span></span>

<span data-ttu-id="e0fab-110">在同步處理過程中，Windows Media Player 10 或更新版本會將播放清單物件複製到已啟用 MTP 的可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="e0fab-110">As part of the synchronization process, Windows Media Player 10 or later copies playlist objects to MTP-enabled portable devices.</span></span> <span data-ttu-id="e0fab-111">Windows Media Player 11 引進了新功能，可讓可攜式裝置限制複製的播放清單物件類型。</span><span class="sxs-lookup"><span data-stu-id="e0fab-111">Windows Media Player 11 introduces new functionality that enables portable devices to limit the types of playlist objects copied.</span></span> <span data-ttu-id="e0fab-112"> (Windows Media Player 一律會將同步處理規則所指定的播放清單內容同步處理。</span><span class="sxs-lookup"><span data-stu-id="e0fab-112">(Windows Media Player always synchronizes playlist content as specified by the synchronization rules.</span></span> <span data-ttu-id="e0fab-113">這項功能只會影響播放清單物件的同步處理。 ) Windows Media Player 會將三種類型的播放清單物件從電腦複製到裝置：</span><span class="sxs-lookup"><span data-stu-id="e0fab-113">This feature affects only the synchronization of playlist objects.) Windows Media Player copies three types of playlist objects from the computer to the device:</span></span>

-   <span data-ttu-id="e0fab-114">**一般播放清單。**</span><span class="sxs-lookup"><span data-stu-id="e0fab-114">**Ordinary playlists.**</span></span> <span data-ttu-id="e0fab-115">這些是在 Windows Media Player 的連結 **庫** 功能中可見的播放清單。</span><span class="sxs-lookup"><span data-stu-id="e0fab-115">These are playlists that are visible in the **Library** feature of Windows Media Player.</span></span> <span data-ttu-id="e0fab-116">這些包括使用者建立的播放清單、線上商店新增至媒體櫃的播放清單，以及隨播放程式一起安裝的範例播放清單。</span><span class="sxs-lookup"><span data-stu-id="e0fab-116">These include playlists created by the user, playlists added to the library by online stores, and sample playlists installed with the Player.</span></span> <span data-ttu-id="e0fab-117">Windows Media Player 只會在使用者選取這些播放程式進行同步處理時，將這些播放清單複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="e0fab-117">Windows Media Player copies only these playlists to the device when the user has selected them for synchronization.</span></span>
-   <span data-ttu-id="e0fab-118">**股票同步播放清單。**</span><span class="sxs-lookup"><span data-stu-id="e0fab-118">**Stock sync playlists.**</span></span> <span data-ttu-id="e0fab-119">這些是隨 Windows Media Player 安裝的特殊播放清單，只能用於同步處理。</span><span class="sxs-lookup"><span data-stu-id="e0fab-119">These are special playlists that are installed with Windows Media Player and used only for synchronization.</span></span> <span data-ttu-id="e0fab-120">這些播放清單只會顯示在 Windows Media Player 裝置設定向導中。</span><span class="sxs-lookup"><span data-stu-id="e0fab-120">These playlists are visible only in the Windows Media Player Device Setup Wizard.</span></span>
-   <span data-ttu-id="e0fab-121">**隱含建立的播放清單。**</span><span class="sxs-lookup"><span data-stu-id="e0fab-121">**Implicitly created playlists.**</span></span> <span data-ttu-id="e0fab-122">當使用者在列出要同步處理之專案的窗格上時，會建立這些播放清單，例如 **演出者** 或 **專輯** 等類別目錄資料夾。</span><span class="sxs-lookup"><span data-stu-id="e0fab-122">These playlists are created when the user drags and drops a category folder, such as **Artist** or **Album**, onto the pane that lists the items to be synchronized.</span></span>

<span data-ttu-id="e0fab-123">名為 wmpdevices 的標頭檔會在此版本中更新，定義支援 Windows Media Player 的裝置延伸模組所需的結構和常數。</span><span class="sxs-lookup"><span data-stu-id="e0fab-123">The header file named wmpdevices.h, which has been updated for this release, defines the structures and constants needed to support Windows Media Player device extensions.</span></span>

<span data-ttu-id="e0fab-124">若要透過 Windows Media Player MTP 裝置延伸模組，將裝置辨識為支援播放清單物件喜好設定，它必須在 DeviceInfo 資料集中包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="e0fab-124">For a device to be recognized as supporting playlist object preferences through the Windows Media Player MTP device extension set, it must include the following information in the DeviceInfo dataset.</span></span> <span data-ttu-id="e0fab-125"> (如需此資料集的詳細資訊，請參閱 MTP 規格的4.6.1 一節。 ) </span><span class="sxs-lookup"><span data-stu-id="e0fab-125">(For more information about this dataset, see section 4.6.1 of the MTP specification.)</span></span>



| <span data-ttu-id="e0fab-126">資料集欄位</span><span class="sxs-lookup"><span data-stu-id="e0fab-126">Dataset field</span></span>          | <span data-ttu-id="e0fab-127">欄位順序</span><span class="sxs-lookup"><span data-stu-id="e0fab-127">Field order</span></span> | <span data-ttu-id="e0fab-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="e0fab-128">Data type</span></span>  | <span data-ttu-id="e0fab-129">值</span><span class="sxs-lookup"><span data-stu-id="e0fab-129">Value</span></span>                       |
|------------------------|-------------|------------|-----------------------------|
| <span data-ttu-id="e0fab-130">VendorExtensionID</span><span class="sxs-lookup"><span data-stu-id="e0fab-130">VendorExtensionID</span></span>      | <span data-ttu-id="e0fab-131">2</span><span class="sxs-lookup"><span data-stu-id="e0fab-131">2</span></span>           | <span data-ttu-id="e0fab-132">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e0fab-132">**UINT32**</span></span> | <span data-ttu-id="e0fab-133">0x00000006</span><span class="sxs-lookup"><span data-stu-id="e0fab-133">0x00000006</span></span>                  |
| <span data-ttu-id="e0fab-134">VendorExtensionVersion</span><span class="sxs-lookup"><span data-stu-id="e0fab-134">VendorExtensionVersion</span></span> | <span data-ttu-id="e0fab-135">3</span><span class="sxs-lookup"><span data-stu-id="e0fab-135">3</span></span>           | <span data-ttu-id="e0fab-136">**UINT16**</span><span class="sxs-lookup"><span data-stu-id="e0fab-136">**UINT16**</span></span> | <span data-ttu-id="e0fab-137">0x0064 (100) </span><span class="sxs-lookup"><span data-stu-id="e0fab-137">0x0064 (100)</span></span>                |
| <span data-ttu-id="e0fab-138">VendorExtensionDesc</span><span class="sxs-lookup"><span data-stu-id="e0fab-138">VendorExtensionDesc</span></span>    | <span data-ttu-id="e0fab-139">4</span><span class="sxs-lookup"><span data-stu-id="e0fab-139">4</span></span>           | <span data-ttu-id="e0fab-140">**String**</span><span class="sxs-lookup"><span data-stu-id="e0fab-140">**String**</span></span> | <span data-ttu-id="e0fab-141">"microsoft.com/WMPPD： 11.0"</span><span class="sxs-lookup"><span data-stu-id="e0fab-141">"microsoft.com/WMPPD: 11.0"</span></span> |



 

<span data-ttu-id="e0fab-142">下表提供有關播放清單物件喜好設定的 MTP 作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e0fab-142">The following table provides details about the MTP operation for playlist object preferences.</span></span>



| <span data-ttu-id="e0fab-143">項目</span><span class="sxs-lookup"><span data-stu-id="e0fab-143">Item</span></span>                  | <span data-ttu-id="e0fab-144">描述</span><span class="sxs-lookup"><span data-stu-id="e0fab-144">Description</span></span>                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fab-145">操作程式碼</span><span class="sxs-lookup"><span data-stu-id="e0fab-145">Operation Code</span></span>        | <span data-ttu-id="e0fab-146">0x9203</span><span class="sxs-lookup"><span data-stu-id="e0fab-146">0x9203</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e0fab-147">Operation 參數1</span><span class="sxs-lookup"><span data-stu-id="e0fab-147">Operation Parameter 1</span></span> | <span data-ttu-id="e0fab-148">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-148">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-149">Operation 參數2</span><span class="sxs-lookup"><span data-stu-id="e0fab-149">Operation Parameter 2</span></span> | <span data-ttu-id="e0fab-150">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-150">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-151">Operation 參數3</span><span class="sxs-lookup"><span data-stu-id="e0fab-151">Operation Parameter 3</span></span> | <span data-ttu-id="e0fab-152">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-152">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-153">Operation 參數4</span><span class="sxs-lookup"><span data-stu-id="e0fab-153">Operation Parameter 4</span></span> | <span data-ttu-id="e0fab-154">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-154">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-155">Operation 參數5</span><span class="sxs-lookup"><span data-stu-id="e0fab-155">Operation Parameter 5</span></span> | <span data-ttu-id="e0fab-156">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-156">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-157">資料</span><span class="sxs-lookup"><span data-stu-id="e0fab-157">Data</span></span>                  | <span data-ttu-id="e0fab-158">裝置會傳迴響應參數1中的值，以指出播放清單物件同步處理喜好設定。</span><span class="sxs-lookup"><span data-stu-id="e0fab-158">The device returns a value in Response Parameter 1 to indicate playlist object synchronization preference.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="e0fab-159">資料方向</span><span class="sxs-lookup"><span data-stu-id="e0fab-159">Data Direction</span></span>        | <span data-ttu-id="e0fab-160">R->I</span><span class="sxs-lookup"><span data-stu-id="e0fab-160">R->I</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e0fab-161">回應碼選項</span><span class="sxs-lookup"><span data-stu-id="e0fab-161">Response Code Options</span></span> | <span data-ttu-id="e0fab-162">MTP \_ 回應 \_ 正常 (0x2001) 或有效的錯誤回應碼。</span><span class="sxs-lookup"><span data-stu-id="e0fab-162">MTP\_RESPONSE\_OK (0x2001) or valid error response code.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="e0fab-163">回應參數1</span><span class="sxs-lookup"><span data-stu-id="e0fab-163">Response Parameter 1</span></span>  | <span data-ttu-id="e0fab-164">0 或 1。</span><span class="sxs-lookup"><span data-stu-id="e0fab-164">0 or 1.</span></span> <span data-ttu-id="e0fab-165">0值表示 Windows Media Player 必須只同步處理一般播放清單物件。</span><span class="sxs-lookup"><span data-stu-id="e0fab-165">A value of 0 indicates that Windows Media Player must synchronize only ordinary playlist objects.</span></span> <span data-ttu-id="e0fab-166">值為1時，表示 Windows Media Player 必須同步處理一般播放清單物件、存貨和隱含建立的同步播放清單物件（這是預設行為）。</span><span class="sxs-lookup"><span data-stu-id="e0fab-166">A value of 1 indicates that that Windows Media Player must synchronize ordinary playlist objects, stock, and implicitly-created sync playlist objects, which is the default behavior.</span></span> |
| <span data-ttu-id="e0fab-167">回應參數2</span><span class="sxs-lookup"><span data-stu-id="e0fab-167">Response Parameter 2</span></span>  | <span data-ttu-id="e0fab-168">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-168">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-169">回應參數3</span><span class="sxs-lookup"><span data-stu-id="e0fab-169">Response Parameter 3</span></span>  | <span data-ttu-id="e0fab-170">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-170">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-171">回應參數4</span><span class="sxs-lookup"><span data-stu-id="e0fab-171">Response Parameter 4</span></span>  | <span data-ttu-id="e0fab-172">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-172">0</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e0fab-173">回應參數5</span><span class="sxs-lookup"><span data-stu-id="e0fab-173">Response Parameter 5</span></span>  | <span data-ttu-id="e0fab-174">0</span><span class="sxs-lookup"><span data-stu-id="e0fab-174">0</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="e0fab-175">備註</span><span class="sxs-lookup"><span data-stu-id="e0fab-175">Remarks</span></span>

<span data-ttu-id="e0fab-176">針對可攜式裝置，執行這項功能是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e0fab-176">Implementing this feature is optional for portable devices.</span></span> <span data-ttu-id="e0fab-177">Windows Media Player 預設會同步處理一般播放清單物件、股票同步播放清單物件，以及隱含建立的播放清單物件。</span><span class="sxs-lookup"><span data-stu-id="e0fab-177">Windows Media Player synchronizes ordinary playlist objects, stock sync playlist objects, and implicitly-created playlist objects by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0fab-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0fab-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0fab-179">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="e0fab-179">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




