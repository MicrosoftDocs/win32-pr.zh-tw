---
title: 'IVMHardDiskConnection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內硬碟的連接。
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- IVMHardDiskConnection 介面 Virtual PC
- IVMHardDiskConnection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983313"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="73d6a-105">IVMHardDiskConnection 介面</span><span class="sxs-lookup"><span data-stu-id="73d6a-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="73d6a-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="73d6a-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73d6a-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="73d6a-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73d6a-108">定義虛擬機器內硬碟的連接。</span><span class="sxs-lookup"><span data-stu-id="73d6a-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="73d6a-109">從 [**IVMVirtualMachine：： AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)方法傳回的 **IVMHardDiskConnection** 物件。</span><span class="sxs-lookup"><span data-stu-id="73d6a-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="73d6a-110">您也可以從 [**IVMVirtualMachine：： HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)屬性傳回的 [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)物件中取出 **IVMHardDiskConnection** 物件。</span><span class="sxs-lookup"><span data-stu-id="73d6a-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="73d6a-111">成員</span><span class="sxs-lookup"><span data-stu-id="73d6a-111">Members</span></span>

<span data-ttu-id="73d6a-112">**IVMHardDiskConnection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="73d6a-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="73d6a-113">**IVMHardDiskConnection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="73d6a-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="73d6a-114">方法</span><span class="sxs-lookup"><span data-stu-id="73d6a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="73d6a-115">屬性</span><span class="sxs-lookup"><span data-stu-id="73d6a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73d6a-116">方法</span><span class="sxs-lookup"><span data-stu-id="73d6a-116">Methods</span></span>

<span data-ttu-id="73d6a-117">**IVMHardDiskConnection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="73d6a-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="73d6a-118">方法</span><span class="sxs-lookup"><span data-stu-id="73d6a-118">Method</span></span>                                                         | <span data-ttu-id="73d6a-119">描述</span><span class="sxs-lookup"><span data-stu-id="73d6a-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="73d6a-120">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="73d6a-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="73d6a-121">設定此硬碟所連接的匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="73d6a-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="73d6a-122">屬性</span><span class="sxs-lookup"><span data-stu-id="73d6a-122">Properties</span></span>

<span data-ttu-id="73d6a-123">**IVMHardDiskConnection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="73d6a-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="73d6a-124">屬性</span><span class="sxs-lookup"><span data-stu-id="73d6a-124">Property</span></span>                                                              | <span data-ttu-id="73d6a-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="73d6a-125">Access type</span></span>          | <span data-ttu-id="73d6a-126">Description</span><span class="sxs-lookup"><span data-stu-id="73d6a-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="73d6a-127">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="73d6a-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="73d6a-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="73d6a-128">Read-only</span></span><br/> | <span data-ttu-id="73d6a-129">磁片磁碟機映射所連接的匯流排編號。</span><span class="sxs-lookup"><span data-stu-id="73d6a-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="73d6a-130">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="73d6a-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="73d6a-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="73d6a-131">Read-only</span></span><br/> | <span data-ttu-id="73d6a-132">磁片磁碟機映射所連接的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="73d6a-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="73d6a-133">**硬碟**</span><span class="sxs-lookup"><span data-stu-id="73d6a-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="73d6a-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="73d6a-134">Read-only</span></span><br/> | <span data-ttu-id="73d6a-135">對應至此連接的硬碟物件。</span><span class="sxs-lookup"><span data-stu-id="73d6a-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="73d6a-136">**UndoHardDisk**</span><span class="sxs-lookup"><span data-stu-id="73d6a-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="73d6a-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="73d6a-137">Read-only</span></span><br/> | <span data-ttu-id="73d6a-138">與此連線的復原磁片映射對應的硬碟物件。</span><span class="sxs-lookup"><span data-stu-id="73d6a-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="73d6a-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="73d6a-139">Requirements</span></span>



| <span data-ttu-id="73d6a-140">需求</span><span class="sxs-lookup"><span data-stu-id="73d6a-140">Requirement</span></span> | <span data-ttu-id="73d6a-141">值</span><span class="sxs-lookup"><span data-stu-id="73d6a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73d6a-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73d6a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="73d6a-143">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73d6a-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73d6a-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73d6a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="73d6a-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="73d6a-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73d6a-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="73d6a-146">End of client support</span></span><br/>    | <span data-ttu-id="73d6a-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73d6a-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73d6a-148">產品</span><span class="sxs-lookup"><span data-stu-id="73d6a-148">Product</span></span><br/>                  | <span data-ttu-id="73d6a-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73d6a-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73d6a-150">標頭</span><span class="sxs-lookup"><span data-stu-id="73d6a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="73d6a-151"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="73d6a-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73d6a-152">IID</span><span class="sxs-lookup"><span data-stu-id="73d6a-152">IID</span></span><br/>                      | <span data-ttu-id="73d6a-153">IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="73d6a-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

