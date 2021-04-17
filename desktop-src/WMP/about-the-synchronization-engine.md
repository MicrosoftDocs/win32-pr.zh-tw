---
title: 關於同步處理引擎
description: 關於同步處理引擎
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player，同步處理引擎
- Windows Media Player 物件模型，同步處理引擎
- 物件模型，同步處理引擎
- Windows Media Player ActiveX 控制項，同步處理引擎
- ActiveX 控制項，同步處理引擎
- Windows Media Player Mobile ActiveX 控制項，同步處理引擎
- Windows Media Player Mobile，同步處理引擎
- 同步處理裝置，同步處理引擎
- 裝置同步處理，同步處理引擎
- 同步處理引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374498"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="8133d-113">關於同步處理引擎</span><span class="sxs-lookup"><span data-stu-id="8133d-113">About the Synchronization Engine</span></span>

<span data-ttu-id="8133d-114">同步處理引擎是管理將數位媒體內容複寫到可攜式裝置的 Windows Media Player 元件。</span><span class="sxs-lookup"><span data-stu-id="8133d-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="8133d-115">Windows Media Player 支援每個裝置的單一同步處理引擎實例。</span><span class="sxs-lookup"><span data-stu-id="8133d-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="8133d-116">您必須使用 Windows Media Player 控制項的遠端實例，以程式設計的方式執行同步處理工作。</span><span class="sxs-lookup"><span data-stu-id="8133d-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="8133d-117">實際上，您的程式會與 Windows Media Player 以及使用播放程式介面進行裝置同步處理的所有其他程式共用同步處理引擎實例。</span><span class="sxs-lookup"><span data-stu-id="8133d-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="8133d-118">您可以使用 [IWMPSyncDevice：： start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) 和 [IWMPSyncDevice：： stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) 來控制同步處理引擎執行其工作的時間。</span><span class="sxs-lookup"><span data-stu-id="8133d-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="8133d-119">在大多數情況下，您不應該使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="8133d-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="8133d-120">相反地，您應該讓同步處理引擎自動排程其工作。</span><span class="sxs-lookup"><span data-stu-id="8133d-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="8133d-121">如果您的程式是設計來取代 Windows Media Player 的使用者介面，則會有 **start** 和 **stop** 方法，因此您可以使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="8133d-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="8133d-122">在此情況下，您可能會想要提供與 [ **裝置** ] 索引標籤中所提供的 [啟動/停止] 按鈕類似的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="8133d-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="8133d-123">您可以藉由輪詢 [IWMPSyncDevice：： get \_ 進度](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)來監視裝置的同步處理進度。</span><span class="sxs-lookup"><span data-stu-id="8133d-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="8133d-124">這個方法會使用特定裝置來抓取整個同步處理常式的進度值。</span><span class="sxs-lookup"><span data-stu-id="8133d-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="8133d-125">抓取的值是代表同步處理完成百分比的數位。</span><span class="sxs-lookup"><span data-stu-id="8133d-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="8133d-126">您可以接收與同步處理相關的兩個事件。</span><span class="sxs-lookup"><span data-stu-id="8133d-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="8133d-127">**DeviceSyncError** 事件會在發生問題時通知您。</span><span class="sxs-lookup"><span data-stu-id="8133d-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="8133d-128">當同步處理引擎變更目前裝置的狀態時， **DeviceSyncStateChange** 事件會發出警示。</span><span class="sxs-lookup"><span data-stu-id="8133d-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="8133d-129">您可以藉由呼叫 [IWMPSyncDevice2：： setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) 與 **PercentSpaceReserved** 屬性，限制 Windows Media Player 用於同步處理的裝置儲存空間量。</span><span class="sxs-lookup"><span data-stu-id="8133d-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="8133d-130">使用這個介面需要 Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="8133d-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8133d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="8133d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8133d-132">**關於裝置同步處理**</span><span class="sxs-lookup"><span data-stu-id="8133d-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="8133d-133">**IWMPEvents2 介面**</span><span class="sxs-lookup"><span data-stu-id="8133d-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="8133d-134">**顯示同步處理進度**</span><span class="sxs-lookup"><span data-stu-id="8133d-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 




