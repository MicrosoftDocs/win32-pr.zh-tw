---
title: IWMDRMDeviceApp 介面
description: IWMDRMDeviceApp 介面可讓應用程式計量、同步處理授權，以及更新裝置的 DRM 元件。
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- IWMDRMDeviceApp 介面 windows Media 裝置管理員
- IWMDRMDeviceApp interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965253"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="1f10e-105">IWMDRMDeviceApp 介面</span><span class="sxs-lookup"><span data-stu-id="1f10e-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="1f10e-106">\[Windows Media DRM 功能已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="1f10e-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="1f10e-107">請改用 [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) 。\]</span><span class="sxs-lookup"><span data-stu-id="1f10e-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="1f10e-108">**IWMDRMDeviceApp** 介面可讓應用程式計量、同步處理授權，以及更新裝置的 DRM 元件。</span><span class="sxs-lookup"><span data-stu-id="1f10e-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="1f10e-109">此介面只適用于支援可攜式裝置之 Windows Media DRM 10 的裝置。</span><span class="sxs-lookup"><span data-stu-id="1f10e-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="1f10e-110">若要取得此介面，請呼叫 **CoCreateInstance**，並傳入 CLSID \_ WMDRMDeviceApp。</span><span class="sxs-lookup"><span data-stu-id="1f10e-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="1f10e-111">此介面定義于從 WMDRMDeviceApp 建立的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="1f10e-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="1f10e-112">此標頭 **\# 包含** s "wmdm .h"。</span><span class="sxs-lookup"><span data-stu-id="1f10e-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="1f10e-113">您可能需要變更這個檔案名，以符合 WMDM 所建立的標頭。</span><span class="sxs-lookup"><span data-stu-id="1f10e-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="1f10e-114">成員</span><span class="sxs-lookup"><span data-stu-id="1f10e-114">Members</span></span>

<span data-ttu-id="1f10e-115">**IWMDRMDeviceApp** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1f10e-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1f10e-116">**IWMDRMDeviceApp** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1f10e-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="1f10e-117">方法</span><span class="sxs-lookup"><span data-stu-id="1f10e-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1f10e-118">方法</span><span class="sxs-lookup"><span data-stu-id="1f10e-118">Methods</span></span>

<span data-ttu-id="1f10e-119">**IWMDRMDeviceApp** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1f10e-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="1f10e-120">方法</span><span class="sxs-lookup"><span data-stu-id="1f10e-120">Method</span></span>                                                                   | <span data-ttu-id="1f10e-121">描述</span><span class="sxs-lookup"><span data-stu-id="1f10e-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f10e-122">**AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="1f10e-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="1f10e-123">初始化或重設裝置安全時鐘</span><span class="sxs-lookup"><span data-stu-id="1f10e-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="1f10e-124">**GenerateMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="1f10e-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="1f10e-125">從裝置取得計量資料。</span><span class="sxs-lookup"><span data-stu-id="1f10e-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1f10e-126">**ProcessMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="1f10e-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="1f10e-127">重設裝置上的部分或所有計量計數（從裝置的資料傳送到伺服器並處理）之後。</span><span class="sxs-lookup"><span data-stu-id="1f10e-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="1f10e-128">**QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="1f10e-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="1f10e-129">查詢裝置的目前 DRM 狀態和功能。</span><span class="sxs-lookup"><span data-stu-id="1f10e-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="1f10e-130">**SynchronizeLicenses**</span><span class="sxs-lookup"><span data-stu-id="1f10e-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="1f10e-131">當裝置上的授權接近到期時，更新該裝置上的授權。</span><span class="sxs-lookup"><span data-stu-id="1f10e-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="1f10e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f10e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f10e-133">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="1f10e-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="1f10e-134">**應用程式的介面**</span><span class="sxs-lookup"><span data-stu-id="1f10e-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="1f10e-135">**計量內容使用方式**</span><span class="sxs-lookup"><span data-stu-id="1f10e-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

