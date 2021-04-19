---
title: IMsRdpDeviceV2 介面
description: 包含裝置物件的相關資訊。 這是 IMsRdpDevice 介面的增強功能。
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceV2 介面遠端桌面服務
- IMsRdpDeviceV2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967713"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="265fd-106">IMsRdpDeviceV2 介面</span><span class="sxs-lookup"><span data-stu-id="265fd-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="265fd-107">包含裝置物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="265fd-107">Contains information about a device object.</span></span> <span data-ttu-id="265fd-108">這是 [**IMsRdpDevice**](imsrdpdevice.md) 介面的增強功能。</span><span class="sxs-lookup"><span data-stu-id="265fd-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="265fd-109">成員</span><span class="sxs-lookup"><span data-stu-id="265fd-109">Members</span></span>

<span data-ttu-id="265fd-110">**IMsRdpDeviceV2** 介面繼承自 [**IMsRdpDevice**](imsrdpdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="265fd-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="265fd-111">**IMsRdpDeviceV2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="265fd-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="265fd-112">屬性</span><span class="sxs-lookup"><span data-stu-id="265fd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="265fd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="265fd-113">Properties</span></span>

<span data-ttu-id="265fd-114">**IMsRdpDeviceV2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="265fd-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="265fd-115">屬性</span><span class="sxs-lookup"><span data-stu-id="265fd-115">Property</span></span>                                                                 | <span data-ttu-id="265fd-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="265fd-116">Access type</span></span>          | <span data-ttu-id="265fd-117">Description</span><span class="sxs-lookup"><span data-stu-id="265fd-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="265fd-118">**CmClassGuid**</span><span class="sxs-lookup"><span data-stu-id="265fd-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="265fd-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-119">Read-only</span></span><br/> | <span data-ttu-id="265fd-120">包含裝置的 configuration manager 安裝類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="265fd-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="265fd-121">**CmDeviceInstance**</span><span class="sxs-lookup"><span data-stu-id="265fd-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="265fd-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-122">Read-only</span></span><br/> | <span data-ttu-id="265fd-123">包含裝置的 configuration manager 裝置實例。</span><span class="sxs-lookup"><span data-stu-id="265fd-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="265fd-124">**DeviceText**</span><span class="sxs-lookup"><span data-stu-id="265fd-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="265fd-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-125">Read-only</span></span><br/> | <span data-ttu-id="265fd-126">包含裝置文字。</span><span class="sxs-lookup"><span data-stu-id="265fd-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="265fd-127">**DriveLetterBitmap**</span><span class="sxs-lookup"><span data-stu-id="265fd-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="265fd-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-128">Read-only</span></span><br/> | <span data-ttu-id="265fd-129">包含代表裝置內所含之磁碟機號對應的位位。</span><span class="sxs-lookup"><span data-stu-id="265fd-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="265fd-130">**IsCompositeDevice**</span><span class="sxs-lookup"><span data-stu-id="265fd-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="265fd-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-131">Read-only</span></span><br/> | <span data-ttu-id="265fd-132">指定裝置是否為複合裝置。</span><span class="sxs-lookup"><span data-stu-id="265fd-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="265fd-133">**IsOptionalDevice**</span><span class="sxs-lookup"><span data-stu-id="265fd-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="265fd-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-134">Read-only</span></span><br/> | <span data-ttu-id="265fd-135">指定裝置是否為 USB 重新導向的選用裝置。</span><span class="sxs-lookup"><span data-stu-id="265fd-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="265fd-136">**IsUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="265fd-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="265fd-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="265fd-137">Read-only</span></span><br/> | <span data-ttu-id="265fd-138">指定裝置是否用於 USB 重新導向。</span><span class="sxs-lookup"><span data-stu-id="265fd-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="265fd-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="265fd-139">Requirements</span></span>



| <span data-ttu-id="265fd-140">需求</span><span class="sxs-lookup"><span data-stu-id="265fd-140">Requirement</span></span> | <span data-ttu-id="265fd-141">值</span><span class="sxs-lookup"><span data-stu-id="265fd-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="265fd-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="265fd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="265fd-143">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="265fd-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="265fd-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="265fd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="265fd-145">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="265fd-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="265fd-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="265fd-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="265fd-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265fd-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="265fd-148">DLL</span><span class="sxs-lookup"><span data-stu-id="265fd-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="265fd-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265fd-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="265fd-150">IID</span><span class="sxs-lookup"><span data-stu-id="265fd-150">IID</span></span><br/>                      | <span data-ttu-id="265fd-151">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="265fd-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





