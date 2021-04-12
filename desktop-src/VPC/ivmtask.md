---
title: 'IVMTask 介面 (VPCCOMInterfaces .h) '
description: 您可以使用 IVMTask 介面來監視和控制各種 COM 方法的非同步工作。
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- IVMTask 介面 Virtual PC
- IVMTask 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508979"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="fd655-105">IVMTask 介面</span><span class="sxs-lookup"><span data-stu-id="fd655-105">IVMTask interface</span></span>

<span data-ttu-id="fd655-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fd655-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd655-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fd655-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd655-108">您可以使用 **IVMTask** 介面來監視和控制各種 COM 方法的非同步工作。</span><span class="sxs-lookup"><span data-stu-id="fd655-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="fd655-109">成員</span><span class="sxs-lookup"><span data-stu-id="fd655-109">Members</span></span>

<span data-ttu-id="fd655-110">**IVMTask** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="fd655-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fd655-111">**IVMTask** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd655-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="fd655-112">方法</span><span class="sxs-lookup"><span data-stu-id="fd655-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fd655-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fd655-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fd655-114">方法</span><span class="sxs-lookup"><span data-stu-id="fd655-114">Methods</span></span>

<span data-ttu-id="fd655-115">**IVMTask** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fd655-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="fd655-116">方法</span><span class="sxs-lookup"><span data-stu-id="fd655-116">Method</span></span>                                                 | <span data-ttu-id="fd655-117">描述</span><span class="sxs-lookup"><span data-stu-id="fd655-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd655-118">**取消**</span><span class="sxs-lookup"><span data-stu-id="fd655-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="fd655-119">取消工作。</span><span class="sxs-lookup"><span data-stu-id="fd655-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="fd655-120">**WaitForCompletion**</span><span class="sxs-lookup"><span data-stu-id="fd655-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="fd655-121">等候工作完成或指定的逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="fd655-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fd655-122">屬性</span><span class="sxs-lookup"><span data-stu-id="fd655-122">Properties</span></span>

<span data-ttu-id="fd655-123">**IVMTask** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fd655-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="fd655-124">屬性</span><span class="sxs-lookup"><span data-stu-id="fd655-124">Property</span></span>                                                        | <span data-ttu-id="fd655-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="fd655-125">Access type</span></span>          | <span data-ttu-id="fd655-126">Description</span><span class="sxs-lookup"><span data-stu-id="fd655-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="fd655-127">**描述**</span><span class="sxs-lookup"><span data-stu-id="fd655-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="fd655-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-128">Read-only</span></span><br/> | <span data-ttu-id="fd655-129">工作的描述。</span><span class="sxs-lookup"><span data-stu-id="fd655-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="fd655-130">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="fd655-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="fd655-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-131">Read-only</span></span><br/> | <span data-ttu-id="fd655-132">此工作所記錄的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fd655-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="fd655-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fd655-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="fd655-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-134">Read-only</span></span><br/> | <span data-ttu-id="fd655-135">針對這項工作記錄的當地語系化錯誤描述。</span><span class="sxs-lookup"><span data-stu-id="fd655-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="fd655-136">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="fd655-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="fd655-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-137">Read-only</span></span><br/> | <span data-ttu-id="fd655-138">這項工作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd655-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="fd655-139">**屬性**</span><span class="sxs-lookup"><span data-stu-id="fd655-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="fd655-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-140">Read-only</span></span><br/> | <span data-ttu-id="fd655-141">指出是否可以取消工作。</span><span class="sxs-lookup"><span data-stu-id="fd655-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="fd655-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="fd655-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="fd655-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-143">Read-only</span></span><br/> | <span data-ttu-id="fd655-144">指出工作是否已完成。</span><span class="sxs-lookup"><span data-stu-id="fd655-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="fd655-145">**PercentCompleted**</span><span class="sxs-lookup"><span data-stu-id="fd655-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="fd655-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-146">Read-only</span></span><br/> | <span data-ttu-id="fd655-147">工作的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="fd655-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="fd655-148">**結果**</span><span class="sxs-lookup"><span data-stu-id="fd655-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="fd655-149">唯讀</span><span class="sxs-lookup"><span data-stu-id="fd655-149">Read-only</span></span><br/> | <span data-ttu-id="fd655-150">工作的結果。</span><span class="sxs-lookup"><span data-stu-id="fd655-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="fd655-151">備註</span><span class="sxs-lookup"><span data-stu-id="fd655-151">Remarks</span></span>

<span data-ttu-id="fd655-152">可能需要相當長的時間才能完成的方法會傳回 **IVMTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="fd655-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="fd655-153">這可讓應用程式監視所需作業的進度，而不需要強制它在等候作業完成時封鎖進一步的執行作業。</span><span class="sxs-lookup"><span data-stu-id="fd655-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="fd655-154">下列方法會傳回可用來追蹤進度的 **IVMTask** 物件：</span><span class="sxs-lookup"><span data-stu-id="fd655-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="fd655-155">**IVMGuestOS：：登出**</span><span class="sxs-lookup"><span data-stu-id="fd655-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="fd655-156">**IVMGuestOS：： Restart**</span><span class="sxs-lookup"><span data-stu-id="fd655-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="fd655-157">**IVMGuestOS：： Shutdown**</span><span class="sxs-lookup"><span data-stu-id="fd655-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="fd655-158">**IVMHardDisk：： Compact**</span><span class="sxs-lookup"><span data-stu-id="fd655-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="fd655-159">**IVMHardDisk：： Convert**</span><span class="sxs-lookup"><span data-stu-id="fd655-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="fd655-160">**IVMHardDisk：： Merge**</span><span class="sxs-lookup"><span data-stu-id="fd655-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="fd655-161">**IVMHardDisk::MergeTo**</span><span class="sxs-lookup"><span data-stu-id="fd655-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="fd655-162">**IVMVirtualMachine::MergeUndoDisks**</span><span class="sxs-lookup"><span data-stu-id="fd655-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="fd655-163">**IVMVirtualMachine：： Reset**</span><span class="sxs-lookup"><span data-stu-id="fd655-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="fd655-164">**IVMVirtualMachine：： Save**</span><span class="sxs-lookup"><span data-stu-id="fd655-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="fd655-165">**IVMVirtualMachine：： Startup**</span><span class="sxs-lookup"><span data-stu-id="fd655-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="fd655-166">**IVMVirtualMachine::Startup2**</span><span class="sxs-lookup"><span data-stu-id="fd655-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="fd655-167">**IVMVirtualMachine：： TurnOff**</span><span class="sxs-lookup"><span data-stu-id="fd655-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="fd655-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="fd655-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="fd655-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="fd655-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="fd655-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="fd655-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="fd655-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd655-171">Requirements</span></span>



| <span data-ttu-id="fd655-172">需求</span><span class="sxs-lookup"><span data-stu-id="fd655-172">Requirement</span></span> | <span data-ttu-id="fd655-173">值</span><span class="sxs-lookup"><span data-stu-id="fd655-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd655-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd655-174">Minimum supported client</span></span><br/> | <span data-ttu-id="fd655-175">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd655-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd655-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd655-176">Minimum supported server</span></span><br/> | <span data-ttu-id="fd655-177">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd655-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd655-178">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fd655-178">End of client support</span></span><br/>    | <span data-ttu-id="fd655-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd655-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd655-180">產品</span><span class="sxs-lookup"><span data-stu-id="fd655-180">Product</span></span><br/>                  | <span data-ttu-id="fd655-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd655-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd655-182">標頭</span><span class="sxs-lookup"><span data-stu-id="fd655-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd655-183"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd655-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd655-184">IID</span><span class="sxs-lookup"><span data-stu-id="fd655-184">IID</span></span><br/>                      | <span data-ttu-id="fd655-185">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="fd655-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

