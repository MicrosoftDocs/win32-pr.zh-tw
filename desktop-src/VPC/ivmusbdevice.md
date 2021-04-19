---
title: 'IVMUSBDevice 介面 (VPCCOMInterfaces .h) '
description: 定義連接至主機之 USB 裝置的介面。 您可以將 USB 裝置連接到虛擬機器，以在虛擬機器中使用該裝置。
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- IVMUSBDevice 介面 Virtual PC
- IVMUSBDevice 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968351"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="7f8f3-106">IVMUSBDevice 介面</span><span class="sxs-lookup"><span data-stu-id="7f8f3-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="7f8f3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f8f3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7f8f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f8f3-109">定義連接至主機之 USB 裝置的介面。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="7f8f3-110">您可以將 USB 裝置連接到虛擬機器，以在虛擬機器中使用該裝置。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="7f8f3-111">成員</span><span class="sxs-lookup"><span data-stu-id="7f8f3-111">Members</span></span>

<span data-ttu-id="7f8f3-112">**IVMUSBDevice** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7f8f3-113">**IVMUSBDevice** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f8f3-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="7f8f3-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7f8f3-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f8f3-115">屬性</span><span class="sxs-lookup"><span data-stu-id="7f8f3-115">Properties</span></span>

<span data-ttu-id="7f8f3-116">**IVMUSBDevice** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="7f8f3-117">屬性</span><span class="sxs-lookup"><span data-stu-id="7f8f3-117">Property</span></span>                                                                 | <span data-ttu-id="7f8f3-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="7f8f3-118">Access type</span></span>          | <span data-ttu-id="7f8f3-119">Description</span><span class="sxs-lookup"><span data-stu-id="7f8f3-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="7f8f3-120">**AttachedToVM**</span><span class="sxs-lookup"><span data-stu-id="7f8f3-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="7f8f3-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f8f3-121">Read-only</span></span><br/> | <span data-ttu-id="7f8f3-122">USB 裝置所連接之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="7f8f3-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="7f8f3-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="7f8f3-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f8f3-124">Read-only</span></span><br/> | <span data-ttu-id="7f8f3-125">USB 裝置的裝置類別。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="7f8f3-126">**DeviceString**</span><span class="sxs-lookup"><span data-stu-id="7f8f3-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="7f8f3-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f8f3-127">Read-only</span></span><br/> | <span data-ttu-id="7f8f3-128">USB 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="7f8f3-129">**HubID**</span><span class="sxs-lookup"><span data-stu-id="7f8f3-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="7f8f3-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f8f3-130">Read-only</span></span><br/> | <span data-ttu-id="7f8f3-131">裝置所連接之中樞的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="7f8f3-132">**ManufacturerString**</span><span class="sxs-lookup"><span data-stu-id="7f8f3-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="7f8f3-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f8f3-133">Read-only</span></span><br/> | <span data-ttu-id="7f8f3-134">USB 裝置製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="7f8f3-135">**連接埠**</span><span class="sxs-lookup"><span data-stu-id="7f8f3-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="7f8f3-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="7f8f3-136">Read-only</span></span><br/> | <span data-ttu-id="7f8f3-137">裝置所連接之埠的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f8f3-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="7f8f3-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f8f3-138">Requirements</span></span>



| <span data-ttu-id="7f8f3-139">需求</span><span class="sxs-lookup"><span data-stu-id="7f8f3-139">Requirement</span></span> | <span data-ttu-id="7f8f3-140">值</span><span class="sxs-lookup"><span data-stu-id="7f8f3-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8f3-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f8f3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8f3-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f8f3-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f8f3-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f8f3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8f3-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="7f8f3-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f8f3-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7f8f3-145">End of client support</span></span><br/>    | <span data-ttu-id="7f8f3-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f8f3-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f8f3-147">產品</span><span class="sxs-lookup"><span data-stu-id="7f8f3-147">Product</span></span><br/>                  | <span data-ttu-id="7f8f3-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f8f3-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f8f3-149">標頭</span><span class="sxs-lookup"><span data-stu-id="7f8f3-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f8f3-150"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f8f3-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f8f3-151">IID</span><span class="sxs-lookup"><span data-stu-id="7f8f3-151">IID</span></span><br/>                      | <span data-ttu-id="7f8f3-152">IID \_ IVMUSBDevice 定義為 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="7f8f3-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

