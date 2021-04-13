---
title: IMsRdpDeviceCollection 介面
description: 代表裝置物件的集合。
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceCollection 介面遠端桌面服務
- IMsRdpDeviceCollection 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383882"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="898d0-105">IMsRdpDeviceCollection 介面</span><span class="sxs-lookup"><span data-stu-id="898d0-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="898d0-106">代表裝置物件的集合。</span><span class="sxs-lookup"><span data-stu-id="898d0-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="898d0-107">成員</span><span class="sxs-lookup"><span data-stu-id="898d0-107">Members</span></span>

<span data-ttu-id="898d0-108">**IMsRdpDeviceCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="898d0-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="898d0-109">**IMsRdpDeviceCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="898d0-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="898d0-110">方法</span><span class="sxs-lookup"><span data-stu-id="898d0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="898d0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="898d0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="898d0-112">方法</span><span class="sxs-lookup"><span data-stu-id="898d0-112">Methods</span></span>

<span data-ttu-id="898d0-113">**IMsRdpDeviceCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="898d0-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="898d0-114">方法</span><span class="sxs-lookup"><span data-stu-id="898d0-114">Method</span></span>                                                        | <span data-ttu-id="898d0-115">描述</span><span class="sxs-lookup"><span data-stu-id="898d0-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="898d0-116">**RescanDevices**</span><span class="sxs-lookup"><span data-stu-id="898d0-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="898d0-117">重新整理集合中的物件清單。</span><span class="sxs-lookup"><span data-stu-id="898d0-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="898d0-118">屬性</span><span class="sxs-lookup"><span data-stu-id="898d0-118">Properties</span></span>

<span data-ttu-id="898d0-119">**IMsRdpDeviceCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="898d0-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="898d0-120">屬性</span><span class="sxs-lookup"><span data-stu-id="898d0-120">Property</span></span>                                                                 | <span data-ttu-id="898d0-121">存取類型</span><span class="sxs-lookup"><span data-stu-id="898d0-121">Access type</span></span>          | <span data-ttu-id="898d0-122">Description</span><span class="sxs-lookup"><span data-stu-id="898d0-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="898d0-123">**DeviceById**</span><span class="sxs-lookup"><span data-stu-id="898d0-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="898d0-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="898d0-124">Read-only</span></span><br/> | <span data-ttu-id="898d0-125">使用指定的識別碼抓取裝置。</span><span class="sxs-lookup"><span data-stu-id="898d0-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="898d0-126">**DeviceByIndex**</span><span class="sxs-lookup"><span data-stu-id="898d0-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="898d0-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="898d0-127">Read-only</span></span><br/> | <span data-ttu-id="898d0-128">在指定的索引處抓取裝置。</span><span class="sxs-lookup"><span data-stu-id="898d0-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="898d0-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="898d0-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="898d0-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="898d0-130">Read-only</span></span><br/> | <span data-ttu-id="898d0-131">抓取集合中的物件計數。</span><span class="sxs-lookup"><span data-stu-id="898d0-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="898d0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="898d0-132">Requirements</span></span>



| <span data-ttu-id="898d0-133">需求</span><span class="sxs-lookup"><span data-stu-id="898d0-133">Requirement</span></span> | <span data-ttu-id="898d0-134">值</span><span class="sxs-lookup"><span data-stu-id="898d0-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="898d0-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="898d0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="898d0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="898d0-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="898d0-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="898d0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="898d0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="898d0-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="898d0-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="898d0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="898d0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="898d0-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="898d0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="898d0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="898d0-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="898d0-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="898d0-143">IID</span><span class="sxs-lookup"><span data-stu-id="898d0-143">IID</span></span><br/>                      | <span data-ttu-id="898d0-144">IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="898d0-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="898d0-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="898d0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="898d0-146">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="898d0-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="898d0-147">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="898d0-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

