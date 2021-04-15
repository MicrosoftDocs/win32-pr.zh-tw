---
title: 'IVMVirtualMachineEvents 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMVirtualMachine 介面的外寄事件介面。
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- IVMVirtualMachineEvents 介面 Virtual PC
- IVMVirtualMachineEvents 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466609"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="9c374-105">IVMVirtualMachineEvents 介面</span><span class="sxs-lookup"><span data-stu-id="9c374-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="9c374-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="9c374-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9c374-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="9c374-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9c374-108">定義 [**IVMVirtualMachine**](ivmvirtualmachine.md) 介面的外寄事件介面。</span><span class="sxs-lookup"><span data-stu-id="9c374-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="9c374-109">用戶端會執行這些方法來接收從 [**IVMVirtualMachine**](ivmvirtualmachine.md)傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="9c374-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="9c374-110">成員</span><span class="sxs-lookup"><span data-stu-id="9c374-110">Members</span></span>

<span data-ttu-id="9c374-111">**IVMVirtualMachineEvents** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="9c374-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9c374-112">**IVMVirtualMachineEvents** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9c374-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="9c374-113">方法</span><span class="sxs-lookup"><span data-stu-id="9c374-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9c374-114">方法</span><span class="sxs-lookup"><span data-stu-id="9c374-114">Methods</span></span>

<span data-ttu-id="9c374-115">**IVMVirtualMachineEvents** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9c374-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="9c374-116">方法</span><span class="sxs-lookup"><span data-stu-id="9c374-116">Method</span></span>                                                                                   | <span data-ttu-id="9c374-117">描述</span><span class="sxs-lookup"><span data-stu-id="9c374-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c374-118">**OnAdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="9c374-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="9c374-119">接收可在虛擬機器中使用整合元件的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="9c374-120">**OnAdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="9c374-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="9c374-121">接收在虛擬機器中卸載整合元件的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="9c374-122">**OnConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="9c374-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="9c374-123">接收此虛擬機器設定中的值已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="9c374-124">**OnDiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="9c374-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="9c374-125">收到通知，表示虛擬機器所需的磁碟空間不足，且虛擬機器無法執行。</span><span class="sxs-lookup"><span data-stu-id="9c374-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="9c374-126">**OnEnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="9c374-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="9c374-127">收到虛擬機器的增強型影片模式支援已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="9c374-128">**OnGuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="9c374-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="9c374-129">接收使用者已從客體作業系統登出的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="9c374-130">**OnGuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="9c374-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="9c374-131">收到客體作業系統已關機的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="9c374-132">**OnHeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="9c374-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="9c374-133">收到虛擬機器的信號已停止的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="9c374-134">這通常表示客體作業系統已損毀。</span><span class="sxs-lookup"><span data-stu-id="9c374-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="9c374-135">**OnRequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="9c374-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="9c374-136">接收已發出關機要求的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="9c374-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="9c374-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="9c374-138">接收已重設虛擬機器的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="9c374-139">**OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="9c374-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="9c374-140">收到虛擬機器的狀態已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="9c374-141">**OnTripleFault**</span><span class="sxs-lookup"><span data-stu-id="9c374-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="9c374-142">收到虛擬機器有三個錯誤的通知。</span><span class="sxs-lookup"><span data-stu-id="9c374-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="9c374-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c374-143">Requirements</span></span>



| <span data-ttu-id="9c374-144">需求</span><span class="sxs-lookup"><span data-stu-id="9c374-144">Requirement</span></span> | <span data-ttu-id="9c374-145">值</span><span class="sxs-lookup"><span data-stu-id="9c374-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c374-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c374-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9c374-147">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c374-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c374-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c374-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9c374-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="9c374-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9c374-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9c374-150">End of client support</span></span><br/>    | <span data-ttu-id="9c374-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c374-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9c374-152">產品</span><span class="sxs-lookup"><span data-stu-id="9c374-152">Product</span></span><br/>                  | <span data-ttu-id="9c374-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9c374-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9c374-154">標頭</span><span class="sxs-lookup"><span data-stu-id="9c374-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c374-155"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c374-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9c374-156">IID</span><span class="sxs-lookup"><span data-stu-id="9c374-156">IID</span></span><br/>                      | <span data-ttu-id="9c374-157">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="9c374-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

