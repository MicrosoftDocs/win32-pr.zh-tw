---
title: 關於合作關係
description: 關於合作關係
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player，合作關係
- Windows Media Player 物件模型，合作關係
- 物件模型，合作關係
- Windows Media Player ActiveX 控制項，合作關係
- ActiveX 控制項，合作關係
- Windows Media Player 的行動 ActiveX 控制項，合作關係
- Windows Media Player 行動裝置、合作關係
- 同步處理裝置，合作關係
- 裝置同步處理，合作關係
- 裝置與 Windows Media Player 之間的合作關係
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104462708"
---
# <a name="about-partnerships"></a><span data-ttu-id="f458f-113">關於合作關係</span><span class="sxs-lookup"><span data-stu-id="f458f-113">About Partnerships</span></span>

<span data-ttu-id="f458f-114">合作關係是可攜式裝置與 Windows Media Player 之間的特殊關聯性。</span><span class="sxs-lookup"><span data-stu-id="f458f-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="f458f-115">使用者可以使用 Windows Media Player 使用者介面，建立特定裝置的合作關係。</span><span class="sxs-lookup"><span data-stu-id="f458f-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="f458f-116">您可以使用 [IWMPSyncDevice：： createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) 和 [IWMPSyncDevice：:d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership)，以程式設計方式管理合作關係。</span><span class="sxs-lookup"><span data-stu-id="f458f-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="f458f-117">**CreatePartnership** 方法會啟動非同步進程，該進程會在透過 **IWMPEvents2** 介面收到 **CreatePartnershipComplete** 事件時結束。</span><span class="sxs-lookup"><span data-stu-id="f458f-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="f458f-118">Windows Media Player 10 或更新版本支援建立與最多16部裝置的合作關係。</span><span class="sxs-lookup"><span data-stu-id="f458f-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="f458f-119">每個合作關係都有相關聯的合作關係索引。</span><span class="sxs-lookup"><span data-stu-id="f458f-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="f458f-120">您可以藉由呼叫 [IWMPSyncDevice：： get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)，來取得特定裝置的合作關係索引。</span><span class="sxs-lookup"><span data-stu-id="f458f-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="f458f-121">合作關係索引的編號是從1到16。</span><span class="sxs-lookup"><span data-stu-id="f458f-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="f458f-122">當特定裝置與 Windows Media Player 沒有合作關係時， **getPartnershipIndex** 會針對索引傳回零。</span><span class="sxs-lookup"><span data-stu-id="f458f-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="f458f-123">您可以藉由呼叫 [IWMPSyncDevice：： get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ，然後檢查已抓取的 [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) 值，來取得特定裝置的合作關係狀態。</span><span class="sxs-lookup"><span data-stu-id="f458f-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="f458f-124">Windows Media Player 可讓每個裝置在一部電腦上有一個使用者的程式庫合作。</span><span class="sxs-lookup"><span data-stu-id="f458f-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="f458f-125">這表示建立新的合作關係會終結目前裝置可能與另一部電腦之間的任何現有合作關係。</span><span class="sxs-lookup"><span data-stu-id="f458f-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="f458f-126">若要知道裝置狀態變更的時間，您可以接收 **DeviceStatusChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="f458f-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="f458f-127">Windows Media Player 無法與狀態為 **wmpdsManualDevice** 的裝置建立合作關係。</span><span class="sxs-lookup"><span data-stu-id="f458f-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f458f-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f458f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f458f-129">**關於裝置同步處理**</span><span class="sxs-lookup"><span data-stu-id="f458f-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="f458f-130">**IWMPEvents2 介面**</span><span class="sxs-lookup"><span data-stu-id="f458f-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="f458f-131">**使用可攜式裝置**</span><span class="sxs-lookup"><span data-stu-id="f458f-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




