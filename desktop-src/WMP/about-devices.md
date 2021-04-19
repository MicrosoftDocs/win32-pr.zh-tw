---
title: 關於裝置
description: 關於裝置
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player，同步處理裝置
- Windows Media Player 物件模型，同步處理裝置
- 物件模型，同步處理裝置
- Windows Media Player ActiveX 控制項，同步處理裝置
- ActiveX 控制項，同步處理裝置
- Windows Media Player 的行動 ActiveX 控制項，同步處理裝置
- Windows Media Player 行動裝置，同步處理裝置
- 正在同步處理裝置，關於
- 裝置同步處理，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966019"
---
# <a name="about-devices"></a><span data-ttu-id="478f4-112">關於裝置</span><span class="sxs-lookup"><span data-stu-id="478f4-112">About Devices</span></span>

<span data-ttu-id="478f4-113">可攜式裝置是一種硬體裝置，當使用者離開電腦時，使用者就能享受數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="478f4-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="478f4-114">通常，可攜式裝置是以電池運作。</span><span class="sxs-lookup"><span data-stu-id="478f4-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="478f4-115">有些裝置只能播放音樂。</span><span class="sxs-lookup"><span data-stu-id="478f4-115">Some devices can play music only.</span></span> <span data-ttu-id="478f4-116">其他裝置可以播放影片和音樂。</span><span class="sxs-lookup"><span data-stu-id="478f4-116">Other devices can play video and music.</span></span>

<span data-ttu-id="478f4-117">某些裝置支援自動同步處理數位媒體內容與 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="478f4-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="478f4-118">其他裝置僅支援手動傳送。</span><span class="sxs-lookup"><span data-stu-id="478f4-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="478f4-119">您可以藉由呼叫 [IWMPSyncDevice：： get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ，然後檢查已抓取的 [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) 值，來判斷特定裝置是否支援自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="478f4-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="478f4-120">如果取出的值是 **wmpdsManualDevice**，則裝置不支援自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="478f4-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="478f4-121">您可以列舉連接到使用者電腦的裝置。</span><span class="sxs-lookup"><span data-stu-id="478f4-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="478f4-122">若要這樣做，請先使用 [IWMPSyncServices：： get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) 取得裝置計數。</span><span class="sxs-lookup"><span data-stu-id="478f4-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="478f4-123">然後，在迴圈中呼叫 [IWMPSyncServices：： getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice)，每次傳遞適當的索引值。</span><span class="sxs-lookup"><span data-stu-id="478f4-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="478f4-124">您可以使用 [IWMPSyncDevice：： get \_ connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) 來評估特定裝置目前是否已連接。</span><span class="sxs-lookup"><span data-stu-id="478f4-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="478f4-125">若要知道裝置連接或中斷連線的時間，您可以接收 **>deviceconnect** 和 **DeviceDisconnect** 事件。</span><span class="sxs-lookup"><span data-stu-id="478f4-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="478f4-126">這些事件會透過 **IWMPEvents2** 介面接收。</span><span class="sxs-lookup"><span data-stu-id="478f4-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="478f4-127">**IWMPSyncDevice** 介面提供了其他方法，可讓您取得或設定裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="478f4-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="478f4-128">例如：</span><span class="sxs-lookup"><span data-stu-id="478f4-128">For example:</span></span>

-   <span data-ttu-id="478f4-129">**取得 \_ friendlyname** 和 **put \_ friendlyname** 方法可讓您取得並指定使用者定義的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="478f4-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="478f4-130">**Get \_ deviceName** 方法可讓您取得使用者在 Windows XP shell 中看到的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="478f4-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="478f4-131">**GetItemInfo** 方法可讓您從裝置取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="478f4-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="478f4-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="478f4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="478f4-133">**關於裝置同步處理**</span><span class="sxs-lookup"><span data-stu-id="478f4-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="478f4-134">**IWMPEvents2 介面**</span><span class="sxs-lookup"><span data-stu-id="478f4-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="478f4-135">**IWMPSyncDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="478f4-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="478f4-136">**使用可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="478f4-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




