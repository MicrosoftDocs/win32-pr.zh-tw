---
title: 'IVMHardDisk 介面 (VPCCOMInterfaces .h) '
description: 提供硬碟影像的存取。 您可以透過 IVMHardDiskConnection 硬碟屬性或 IVMVirtualPC GetHardDisk 方法來存取它。
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- IVMHardDisk 介面 Virtual PC
- IVMHardDisk 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464189"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="ed557-106">IVMHardDisk 介面</span><span class="sxs-lookup"><span data-stu-id="ed557-106">IVMHardDisk interface</span></span>

<span data-ttu-id="ed557-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ed557-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ed557-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ed557-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ed557-109">提供硬碟影像的存取。</span><span class="sxs-lookup"><span data-stu-id="ed557-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="ed557-110">您可以透過 [**IVMHardDiskConnection：：硬碟**](ivmharddiskconnection-harddisk.md) 屬性或 [**IVMVirtualPC：： GetHardDisk**](ivmvirtualpc-getharddisk.md) 方法來存取它。</span><span class="sxs-lookup"><span data-stu-id="ed557-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="ed557-111">成員</span><span class="sxs-lookup"><span data-stu-id="ed557-111">Members</span></span>

<span data-ttu-id="ed557-112">**IVMHardDisk** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="ed557-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ed557-113">**IVMHardDisk** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ed557-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="ed557-114">方法</span><span class="sxs-lookup"><span data-stu-id="ed557-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ed557-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ed557-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ed557-116">方法</span><span class="sxs-lookup"><span data-stu-id="ed557-116">Methods</span></span>

<span data-ttu-id="ed557-117">**IVMHardDisk** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ed557-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="ed557-118">方法</span><span class="sxs-lookup"><span data-stu-id="ed557-118">Method</span></span>                                 | <span data-ttu-id="ed557-119">描述</span><span class="sxs-lookup"><span data-stu-id="ed557-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed557-120">**精簡**</span><span class="sxs-lookup"><span data-stu-id="ed557-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="ed557-121">壓縮動態擴充的虛擬硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="ed557-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="ed557-122">**轉換**</span><span class="sxs-lookup"><span data-stu-id="ed557-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="ed557-123">將任何虛擬硬碟轉換成動態擴充的虛擬硬碟或固定大小的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="ed557-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="ed557-124">**合併**</span><span class="sxs-lookup"><span data-stu-id="ed557-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="ed557-125">合併差異虛擬硬碟與其父磁片映射。</span><span class="sxs-lookup"><span data-stu-id="ed557-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="ed557-126">**MergeTo**</span><span class="sxs-lookup"><span data-stu-id="ed557-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="ed557-127">將差異虛擬硬碟與其所有父系合併 (（包括根父系虛擬硬碟) ）至新的硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="ed557-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ed557-128">屬性</span><span class="sxs-lookup"><span data-stu-id="ed557-128">Properties</span></span>

<span data-ttu-id="ed557-129">**IVMHardDisk** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ed557-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="ed557-130">屬性</span><span class="sxs-lookup"><span data-stu-id="ed557-130">Property</span></span>                                                              | <span data-ttu-id="ed557-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="ed557-131">Access type</span></span>           | <span data-ttu-id="ed557-132">Description</span><span class="sxs-lookup"><span data-stu-id="ed557-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed557-133">**檔案**</span><span class="sxs-lookup"><span data-stu-id="ed557-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="ed557-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="ed557-134">Read-only</span></span><br/>  | <span data-ttu-id="ed557-135">虛擬硬碟檔案的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="ed557-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="ed557-136">**HostFreeDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="ed557-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="ed557-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="ed557-137">Read-only</span></span><br/>  | <span data-ttu-id="ed557-138">虛擬硬碟的主機上可用的剩餘磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="ed557-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="ed557-139">**父代**</span><span class="sxs-lookup"><span data-stu-id="ed557-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="ed557-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed557-140">Read/write</span></span><br/> | <span data-ttu-id="ed557-141">差異虛擬硬碟的父系。</span><span class="sxs-lookup"><span data-stu-id="ed557-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="ed557-142">**SizeInGuest**</span><span class="sxs-lookup"><span data-stu-id="ed557-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="ed557-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="ed557-143">Read-only</span></span><br/>  | <span data-ttu-id="ed557-144">客體作業系統中的虛擬硬碟大小。</span><span class="sxs-lookup"><span data-stu-id="ed557-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="ed557-145">**SizeOnHost**</span><span class="sxs-lookup"><span data-stu-id="ed557-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="ed557-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="ed557-146">Read-only</span></span><br/>  | <span data-ttu-id="ed557-147">主機電腦上虛擬硬碟檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="ed557-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="ed557-148">**類型**</span><span class="sxs-lookup"><span data-stu-id="ed557-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="ed557-149">唯讀</span><span class="sxs-lookup"><span data-stu-id="ed557-149">Read-only</span></span><br/>  | <span data-ttu-id="ed557-150">虛擬硬碟的類型。</span><span class="sxs-lookup"><span data-stu-id="ed557-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="ed557-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed557-151">Requirements</span></span>



| <span data-ttu-id="ed557-152">需求</span><span class="sxs-lookup"><span data-stu-id="ed557-152">Requirement</span></span> | <span data-ttu-id="ed557-153">值</span><span class="sxs-lookup"><span data-stu-id="ed557-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed557-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed557-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ed557-155">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed557-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed557-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed557-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ed557-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="ed557-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ed557-158">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ed557-158">End of client support</span></span><br/>    | <span data-ttu-id="ed557-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed557-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ed557-160">產品</span><span class="sxs-lookup"><span data-stu-id="ed557-160">Product</span></span><br/>                  | <span data-ttu-id="ed557-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ed557-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ed557-162">標頭</span><span class="sxs-lookup"><span data-stu-id="ed557-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed557-163"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed557-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ed557-164">IID</span><span class="sxs-lookup"><span data-stu-id="ed557-164">IID</span></span><br/>                      | <span data-ttu-id="ed557-165">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="ed557-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

