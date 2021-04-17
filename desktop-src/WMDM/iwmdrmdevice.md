---
title: IWMDRMDevice 介面
description: 這個介面不是由服務提供者所執行，而是為了完成檔的目的而提供。IWMDRMDevice 介面可讓安全的內容提供者與針對可攜式裝置使用 Windows Media DRM 10 的裝置進行通訊。
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- IWMDRMDevice 介面 windows Media 裝置管理員
- IWMDRMDevice interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315475"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="446db-105">IWMDRMDevice 介面</span><span class="sxs-lookup"><span data-stu-id="446db-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="446db-106">這個介面不是由服務提供者所執行，而是為了完成檔的目的而提供。</span><span class="sxs-lookup"><span data-stu-id="446db-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="446db-107">**IWMDRMDevice** 介面可讓安全的內容提供者與針對可攜式裝置使用 WINDOWS Media DRM 10 的裝置進行通訊。</span><span class="sxs-lookup"><span data-stu-id="446db-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="446db-108">成員</span><span class="sxs-lookup"><span data-stu-id="446db-108">Members</span></span>

<span data-ttu-id="446db-109">**IWMDRMDevice** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="446db-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="446db-110">**IWMDRMDevice** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="446db-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="446db-111">方法</span><span class="sxs-lookup"><span data-stu-id="446db-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="446db-112">方法</span><span class="sxs-lookup"><span data-stu-id="446db-112">Methods</span></span>

<span data-ttu-id="446db-113">**IWMDRMDevice** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="446db-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="446db-114">方法</span><span class="sxs-lookup"><span data-stu-id="446db-114">Method</span></span>                                                                  | <span data-ttu-id="446db-115">描述</span><span class="sxs-lookup"><span data-stu-id="446db-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="446db-116">**CleanDataStore**</span><span class="sxs-lookup"><span data-stu-id="446db-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="446db-117">開始在裝置上清除 DRM 資料存放區的進程。</span><span class="sxs-lookup"><span data-stu-id="446db-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="446db-118">**GetDeviceCertificate**</span><span class="sxs-lookup"><span data-stu-id="446db-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="446db-119">抓取裝置憑證。</span><span class="sxs-lookup"><span data-stu-id="446db-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="446db-120">**GetMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="446db-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="446db-121">捕獲計量挑戰。</span><span class="sxs-lookup"><span data-stu-id="446db-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="446db-122">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="446db-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="446db-123">抓取安全時鐘。</span><span class="sxs-lookup"><span data-stu-id="446db-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="446db-124">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="446db-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="446db-125">捕獲安全的時鐘挑戰。</span><span class="sxs-lookup"><span data-stu-id="446db-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="446db-126">**GetSyncList**</span><span class="sxs-lookup"><span data-stu-id="446db-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="446db-127">抓取授權同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="446db-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="446db-128">**IsWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="446db-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="446db-129">判斷裝置是否支援可攜式裝置的 Windows Media DRM 10。</span><span class="sxs-lookup"><span data-stu-id="446db-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="446db-130">**SetLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="446db-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="446db-131">設定授權回應。</span><span class="sxs-lookup"><span data-stu-id="446db-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="446db-132">**SetMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="446db-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="446db-133">設定計量回應。</span><span class="sxs-lookup"><span data-stu-id="446db-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="446db-134">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="446db-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="446db-135">設定安全時鐘回應。</span><span class="sxs-lookup"><span data-stu-id="446db-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="446db-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="446db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446db-137">**服務提供者的介面**</span><span class="sxs-lookup"><span data-stu-id="446db-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

