---
title: 適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能
description: 適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player、裝置擴充功能
- Windows Media Player、延伸模組
- Windows Media Player，中繼資料
- Windows Media Player，加速中繼資料傳輸
- Windows Media Player，中繼資料加速傳送
- 中繼資料，裝置延伸模組
- 中繼資料，延伸模組
- 裝置延伸模組，中繼資料傳輸
- 延伸模組，中繼資料傳輸
- 加速中繼資料傳輸
- 中繼資料，加速傳送
- 裝置延伸模組，加速中繼資料傳輸
- 延伸模組，加速中繼資料傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462305"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a><span data-ttu-id="4f06b-116">適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="4f06b-116">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>

<span data-ttu-id="4f06b-117">若要啟用加速中繼資料傳送，不支援 MTP 的裝置製造商必須在原始程式碼中執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="4f06b-117">To enable accelerated metadata transfer, manufacturers of devices that do not support MTP must do the following in source code:</span></span>

-   <span data-ttu-id="4f06b-118">定義 **WMP \_ WMDM \_ 裝置 \_ 支援**。</span><span class="sxs-lookup"><span data-stu-id="4f06b-118">Define **WMP\_WMDM\_DEVICE\_SUPPORT**.</span></span>
-   <span data-ttu-id="4f06b-119">包含 wmpdevices，它會安裝為 Windows Media Player SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4f06b-119">Include wmpdevices.h, which is installed as part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="4f06b-120">Wmpdevices 會定義下列結構。</span><span class="sxs-lookup"><span data-stu-id="4f06b-120">Wmpdevices.h defines the following structures.</span></span>



| <span data-ttu-id="4f06b-121">結構</span><span class="sxs-lookup"><span data-stu-id="4f06b-121">Structure</span></span>                                                                                 | <span data-ttu-id="4f06b-122">Description</span><span class="sxs-lookup"><span data-stu-id="4f06b-122">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f06b-123">WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ PC2DEVICE</span><span class="sxs-lookup"><span data-stu-id="4f06b-123">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | <span data-ttu-id="4f06b-124">Windows Media Player 用來向不支援 MTP 的可攜式裝置要求加速元資料同步處理資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="4f06b-124">Structure used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |
| [<span data-ttu-id="4f06b-125">WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ DEVICE2PC</span><span class="sxs-lookup"><span data-stu-id="4f06b-125">WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC</span></span>](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | <span data-ttu-id="4f06b-126">Windows Media Player 用來從不支援 MTP 的可攜式裝置接收加速元資料同步處理資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="4f06b-126">Structure used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.</span></span> |



 

<span data-ttu-id="4f06b-127">若要向裝置要求已變更中繼資料的資訊，Windows Media Player 10 或更新版本會呼叫 Windows Media 裝置管理員方法 **IWMDMDevice3：:D eviceiocontrol**。</span><span class="sxs-lookup"><span data-stu-id="4f06b-127">To request information from the device about metadata that has changed, Windows Media Player 10 or later calls the Windows Media Device Manager method **IWMDMDevice3::DeviceIoControl**.</span></span> <span data-ttu-id="4f06b-128">進行此呼叫時，播放玩家會遵循特定的步驟，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4f06b-128">When making this call, the Player follows specific steps, as follows:</span></span>

-   <span data-ttu-id="4f06b-129">第一個參數 *dwIoControlCode* 包含常數 **IOCTL \_ WMP \_ 中繼資料 \_ 來回 \_ 行程**。</span><span class="sxs-lookup"><span data-stu-id="4f06b-129">The first parameter, *dwIoControlCode*, contains the constant **IOCTL\_WMP\_METADATA\_ROUND\_TRIP**.</span></span> <span data-ttu-id="4f06b-130">這個常數定義于 wmpdevices 中。</span><span class="sxs-lookup"><span data-stu-id="4f06b-130">This constant is defined in wmpdevices.h.</span></span>
-   <span data-ttu-id="4f06b-131">第二個參數 *lpInBuffer* 會指向 **WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ PC2DEVICE** 結構。</span><span class="sxs-lookup"><span data-stu-id="4f06b-131">The second parameter, *lpInBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_PC2DEVICE** structure.</span></span>
-   <span data-ttu-id="4f06b-132">第三個參數 *nInBufferSize* 包含輸入緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="4f06b-132">The third parameter, *nInBufferSize*, contains the size of the input buffer.</span></span>
-   <span data-ttu-id="4f06b-133">第四個參數 *lpOutBuffer* 會指向 **WMP \_ WMDM \_ 中繼資料 \_ 來回 \_ 行程 \_ DEVICE2PC** 結構。</span><span class="sxs-lookup"><span data-stu-id="4f06b-133">The fourth parameter, *lpOutBuffer*, points to a **WMP\_WMDM\_METADATA\_ROUND\_TRIP\_DEVICE2PC** structure.</span></span> <span data-ttu-id="4f06b-134">裝置必須在此結構中填入變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f06b-134">The device must fill in this structure with information about changes.</span></span>
-   <span data-ttu-id="4f06b-135">第五個參數 *pnOutBufferSize* 會接收輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="4f06b-135">The fifth parameter, *pnOutBufferSize*, receives the size of the output buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f06b-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f06b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f06b-137">**加速中繼資料傳輸的裝置擴充功能**</span><span class="sxs-lookup"><span data-stu-id="4f06b-137">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




