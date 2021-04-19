---
title: 'IVMUSBDeviceCollection 介面 (VPCCOMInterfaces .h) '
description: 定義連接至主機系統的 USB 裝置集合。 若要取得 IVMUSBDeviceCollection 物件，請使用 IVMVirtualPC USBDeviceCollection 屬性。
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- IVMUSBDeviceCollection 介面 Virtual PC
- IVMUSBDeviceCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967535"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="ceb29-106">IVMUSBDeviceCollection 介面</span><span class="sxs-lookup"><span data-stu-id="ceb29-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="ceb29-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ceb29-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ceb29-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ceb29-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ceb29-109">定義連接至主機系統的 USB 裝置集合。</span><span class="sxs-lookup"><span data-stu-id="ceb29-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="ceb29-110">若要取得 **IVMUSBDeviceCollection** 物件，請使用 [**IVMVirtualPC：： USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ceb29-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="ceb29-111">成員</span><span class="sxs-lookup"><span data-stu-id="ceb29-111">Members</span></span>

<span data-ttu-id="ceb29-112">**IVMUSBDeviceCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="ceb29-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ceb29-113">**IVMUSBDeviceCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ceb29-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="ceb29-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ceb29-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ceb29-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ceb29-115">Properties</span></span>

<span data-ttu-id="ceb29-116">**IVMUSBDeviceCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ceb29-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="ceb29-117">屬性</span><span class="sxs-lookup"><span data-stu-id="ceb29-117">Property</span></span>                                                        | <span data-ttu-id="ceb29-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="ceb29-118">Access type</span></span>          | <span data-ttu-id="ceb29-119">Description</span><span class="sxs-lookup"><span data-stu-id="ceb29-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb29-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="ceb29-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="ceb29-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb29-121">Read-only</span></span><br/> | <span data-ttu-id="ceb29-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="ceb29-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="ceb29-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="ceb29-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="ceb29-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb29-124">Read-only</span></span><br/> | <span data-ttu-id="ceb29-125">此集合中的 USB 裝置數目。</span><span class="sxs-lookup"><span data-stu-id="ceb29-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="ceb29-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="ceb29-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="ceb29-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="ceb29-127">Read-only</span></span><br/> | <span data-ttu-id="ceb29-128">對應至指定索引 (1) 的 USB 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="ceb29-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ceb29-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ceb29-129">Requirements</span></span>



| <span data-ttu-id="ceb29-130">需求</span><span class="sxs-lookup"><span data-stu-id="ceb29-130">Requirement</span></span> | <span data-ttu-id="ceb29-131">值</span><span class="sxs-lookup"><span data-stu-id="ceb29-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb29-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ceb29-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb29-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ceb29-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ceb29-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ceb29-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb29-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="ceb29-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ceb29-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ceb29-136">End of client support</span></span><br/>    | <span data-ttu-id="ceb29-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ceb29-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ceb29-138">產品</span><span class="sxs-lookup"><span data-stu-id="ceb29-138">Product</span></span><br/>                  | <span data-ttu-id="ceb29-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ceb29-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ceb29-140">標頭</span><span class="sxs-lookup"><span data-stu-id="ceb29-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceb29-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ceb29-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ceb29-142">IID</span><span class="sxs-lookup"><span data-stu-id="ceb29-142">IID</span></span><br/>                      | <span data-ttu-id="ceb29-143">IID \_ IVMUSBDeviceCollection 定義為4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="ceb29-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="ceb29-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ceb29-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb29-145">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="ceb29-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="ceb29-146">**IVMVirtualPC::USBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="ceb29-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

