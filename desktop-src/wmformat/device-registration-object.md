---
title: 裝置註冊物件
description: 裝置註冊物件
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK，裝置註冊物件
- Advanced Systems Format (ASF) 、裝置註冊物件
- ASF (Advanced 系統格式) 、裝置註冊物件
- 物件、裝置註冊物件
- 裝置註冊物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966231"
---
# <a name="device-registration-object"></a><span data-ttu-id="7fb6c-108">裝置註冊物件</span><span class="sxs-lookup"><span data-stu-id="7fb6c-108">Device Registration Object</span></span>

<span data-ttu-id="7fb6c-109">裝置註冊物件會管理裝置註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="7fb6c-110">此資料庫會儲存連線至用戶端電腦的網路裝置相關資訊，例如機頂尖的影片播放程式。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="7fb6c-111">裝置註冊資料庫的主要目的是要管理使用「網路裝置的 Windows Media DRM 10」通訊協定來接收安全資料流程的裝置。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="7fb6c-112">如果您的應用程式支援網路裝置的 Windows Media DRM 10，您必須使用此物件的介面來註冊網路裝置，以及驗證這些裝置。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="7fb6c-113">您也可以使用裝置註冊資料庫來儲存有關網路裝置的資訊，這些資訊不會將 Windows Media DRM 10 用於網路裝置，但資料庫中的所有資訊都不會套用到這類裝置。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="7fb6c-114">裝置註冊物件是由 [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) 函式所建立，該函式會將指標設定為 **IWMDeviceRegistration** 介面。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="7fb6c-115">您可以藉由呼叫 **QueryInterface** 方法來取得裝置註冊物件的其他方法。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="7fb6c-116">裝置註冊物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="7fb6c-117">介面</span><span class="sxs-lookup"><span data-stu-id="7fb6c-117">Interface</span></span>                                              | <span data-ttu-id="7fb6c-118">描述</span><span class="sxs-lookup"><span data-stu-id="7fb6c-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="7fb6c-119">**IWMDeviceRegistration**</span><span class="sxs-lookup"><span data-stu-id="7fb6c-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="7fb6c-120">管理裝置註冊資料庫。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="7fb6c-121">**IWMDRMMessageParser**</span><span class="sxs-lookup"><span data-stu-id="7fb6c-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="7fb6c-122">剖析裝置所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="7fb6c-123">**IWMProximityDetection**</span><span class="sxs-lookup"><span data-stu-id="7fb6c-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="7fb6c-124">管理裝置驗證。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="7fb6c-125">下列回呼介面必須由應用程式執行，才能使用 **IWMProximityDetection** 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="7fb6c-126">介面</span><span class="sxs-lookup"><span data-stu-id="7fb6c-126">Interface</span></span>                                      | <span data-ttu-id="7fb6c-127">描述</span><span class="sxs-lookup"><span data-stu-id="7fb6c-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="7fb6c-128">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="7fb6c-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="7fb6c-129">接收在個別執行緒中執行之進程的狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb6c-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7fb6c-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fb6c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb6c-131">**物件**</span><span class="sxs-lookup"><span data-stu-id="7fb6c-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




