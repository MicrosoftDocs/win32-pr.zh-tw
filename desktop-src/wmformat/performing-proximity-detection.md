---
title: 執行鄰近性偵測
description: 執行鄰近性偵測
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows Media Format SDK，執行鄰近性偵測
- Windows Media Format SDK，鄰近性偵測
- Advanced Systems Format (ASF) ，執行鄰近性偵測
- ASF (Advanced 系統格式) ，執行鄰近性偵測
- Advanced Systems Format (ASF) 、鄰近性偵測
- ASF (Advanced 系統格式) 、鄰近偵測
- 數位版權管理 (DRM) ，執行鄰近性偵測
- DRM (數位版權管理) ，執行鄰近性偵測
- 數位版權管理 (DRM) ，鄰近性偵測
- DRM (數位版權管理) ，鄰近性偵測
- 鄰近性偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374362"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="b3679-114">執行鄰近性偵測</span><span class="sxs-lookup"><span data-stu-id="b3679-114">Performing Proximity Detection</span></span>

<span data-ttu-id="b3679-115">您必須先執行稱為鄰近偵測的進程， (也稱為驗證) ，才能將加密資料串流至 Windows Media DRM 10 for Network Devices 通訊協定中的已註冊裝置。</span><span class="sxs-lookup"><span data-stu-id="b3679-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="b3679-116">此程式牽涉到將訊息傳送至裝置，並接收回應。</span><span class="sxs-lookup"><span data-stu-id="b3679-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="b3679-117">接收回應所需的時間是用來判斷裝置是否接近網路上的電腦，以接收安全的資料。</span><span class="sxs-lookup"><span data-stu-id="b3679-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="b3679-118">確認裝置實際接近網路上的用戶端電腦有助於防止詐騙和其他未經授權的存取。</span><span class="sxs-lookup"><span data-stu-id="b3679-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="b3679-119">當近接偵測順利完成時，裝置就會被視為有效。</span><span class="sxs-lookup"><span data-stu-id="b3679-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="b3679-120">您可以藉由呼叫 [**IWMRegisteredDevice：： IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) 方法來檢查裝置是否有效。</span><span class="sxs-lookup"><span data-stu-id="b3679-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="b3679-121">裝置必須每隔48小時進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b3679-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="b3679-122">在您的程式執行之前經過驗證超過48小時的裝置，必須重新驗證，方法是再次執行鄰近性偵測處理常式。</span><span class="sxs-lookup"><span data-stu-id="b3679-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="b3679-123">若要執行鄰近性偵測，您必須建立與裝置的通訊，然後呼叫 [**IWMProximityDetection：： StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3679-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="b3679-124">偵測程式是由 Windows Media Format SDK 的內部 DRM 元件以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="b3679-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="b3679-125">您的應用程式必須包含 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 介面的執行，以處理鄰近性偵測訊息。</span><span class="sxs-lookup"><span data-stu-id="b3679-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="b3679-126">近接偵測程式會傳送兩則訊息：結果訊息和完成訊息。</span><span class="sxs-lookup"><span data-stu-id="b3679-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="b3679-127">\_ \_ 當偵測程式完成時，會傳送結果訊息 WMT 鄰近結果。</span><span class="sxs-lookup"><span data-stu-id="b3679-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="b3679-128">[**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)回呼方法的 *hr* 參數會指出裝置是否夠接近用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="b3679-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="b3679-129">如果結果訊息的 *hr* 參數表示成功，則 *pValue* 參數會包含 **DWORD** ，以指定裝置的測量延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b3679-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="b3679-130">完成偵測時，會傳送完成訊息（WMT \_ 鄰近性 \_ 已完成）。</span><span class="sxs-lookup"><span data-stu-id="b3679-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="b3679-131">只有在收到此訊息之後，您才應該釋放 [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) 介面。</span><span class="sxs-lookup"><span data-stu-id="b3679-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="b3679-132">裝置的鄰近性偵測成功時，會自動更新裝置註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="b3679-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="b3679-133">[**IWMRegisteredDevice：： IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid)的後續呼叫會傳回 **TRUE** ，直到超過48小時，而且必須重新驗證裝置。</span><span class="sxs-lookup"><span data-stu-id="b3679-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="b3679-134">**注意** 此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="b3679-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3679-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3679-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3679-136">**使用 Windows Media DRM 10 進行網路裝置通訊協定**</span><span class="sxs-lookup"><span data-stu-id="b3679-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




