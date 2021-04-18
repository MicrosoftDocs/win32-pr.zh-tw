---
title: IMsRdpDevice 介面
description: 包含裝置物件的相關資訊。
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- IMsRdpDevice 介面遠端桌面服務
- IMsRdpDevice 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968541"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="8b95b-105">IMsRdpDevice 介面</span><span class="sxs-lookup"><span data-stu-id="8b95b-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="8b95b-106">包含裝置物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8b95b-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="8b95b-107">成員</span><span class="sxs-lookup"><span data-stu-id="8b95b-107">Members</span></span>

<span data-ttu-id="8b95b-108">**IMsRdpDevice** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8b95b-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b95b-109">**IMsRdpDevice** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8b95b-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="8b95b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8b95b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b95b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8b95b-111">Properties</span></span>

<span data-ttu-id="8b95b-112">**IMsRdpDevice** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8b95b-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="8b95b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8b95b-113">Property</span></span>                                                               | <span data-ttu-id="8b95b-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="8b95b-114">Access type</span></span>           | <span data-ttu-id="8b95b-115">Description</span><span class="sxs-lookup"><span data-stu-id="8b95b-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b95b-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="8b95b-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="8b95b-117">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b95b-117">Read-only</span></span><br/>  | <span data-ttu-id="8b95b-118">抓取顯示名稱無法使用時，要向使用者顯示的裝置描述。</span><span class="sxs-lookup"><span data-stu-id="8b95b-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="8b95b-119">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="8b95b-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="8b95b-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b95b-120">Read-only</span></span><br/>  | <span data-ttu-id="8b95b-121">抓取裝置的裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b95b-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="8b95b-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="8b95b-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="8b95b-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b95b-123">Read-only</span></span><br/>  | <span data-ttu-id="8b95b-124">抓取裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8b95b-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="8b95b-125">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="8b95b-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="8b95b-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8b95b-126">Read/write</span></span><br/> | <span data-ttu-id="8b95b-127">指出裝置的重新導向狀態。</span><span class="sxs-lookup"><span data-stu-id="8b95b-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="8b95b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b95b-128">Requirements</span></span>



| <span data-ttu-id="8b95b-129">需求</span><span class="sxs-lookup"><span data-stu-id="8b95b-129">Requirement</span></span> | <span data-ttu-id="8b95b-130">值</span><span class="sxs-lookup"><span data-stu-id="8b95b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b95b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b95b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b95b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b95b-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8b95b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b95b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b95b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b95b-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8b95b-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8b95b-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b95b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b95b-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b95b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8b95b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b95b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b95b-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b95b-139">IID</span><span class="sxs-lookup"><span data-stu-id="8b95b-139">IID</span></span><br/>                      | <span data-ttu-id="8b95b-140">IID \_ IMsRdpDevice 定義為60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="8b95b-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8b95b-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b95b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b95b-142">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="8b95b-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="8b95b-143">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="8b95b-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

