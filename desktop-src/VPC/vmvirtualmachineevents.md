---
title: 'VMVirtualMachineEvents 列舉 (VPCCOMInterfaces) '
description: 指定 VM 事件。
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- VMVirtualMachineEvents 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025394"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="e1044-104">VMVirtualMachineEvents 列舉</span><span class="sxs-lookup"><span data-stu-id="e1044-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="e1044-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e1044-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e1044-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e1044-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e1044-107">指定虛擬機器 (VM) 事件。</span><span class="sxs-lookup"><span data-stu-id="e1044-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1044-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1044-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="e1044-109">常數</span><span class="sxs-lookup"><span data-stu-id="e1044-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e1044-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent \_ StateChanged**</span><span class="sxs-lookup"><span data-stu-id="e1044-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-111">VM 的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="e1044-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ RequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="e1044-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-113">已要求關機。</span><span class="sxs-lookup"><span data-stu-id="e1044-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent \_ 重設**</span><span class="sxs-lookup"><span data-stu-id="e1044-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-115">VM 已重設。</span><span class="sxs-lookup"><span data-stu-id="e1044-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent \_ TripleFault**</span><span class="sxs-lookup"><span data-stu-id="e1044-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-117">VM 發生三個錯誤。</span><span class="sxs-lookup"><span data-stu-id="e1044-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent \_ HeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="e1044-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-119">已停止 VM 的信號。</span><span class="sxs-lookup"><span data-stu-id="e1044-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="e1044-120">這通常表示客體作業系統已損毀。</span><span class="sxs-lookup"><span data-stu-id="e1044-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent \_ ConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="e1044-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-122">此 VM 設定中的值已變更</span><span class="sxs-lookup"><span data-stu-id="e1044-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="e1044-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent \_ EnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="e1044-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-124">VM 的影片模式已變更。</span><span class="sxs-lookup"><span data-stu-id="e1044-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent \_ AdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="e1044-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-126">已從 VM 卸載整合元件。</span><span class="sxs-lookup"><span data-stu-id="e1044-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent \_ AdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="e1044-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-128">客體作業系統中提供整合功能。</span><span class="sxs-lookup"><span data-stu-id="e1044-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ GuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="e1044-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-130">客體作業系統正在關機。</span><span class="sxs-lookup"><span data-stu-id="e1044-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent \_ GuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="e1044-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-132">從客體作業系統登出的使用者。</span><span class="sxs-lookup"><span data-stu-id="e1044-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="e1044-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent \_ DiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="e1044-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="e1044-134">VM 所需的磁碟空間不足。</span><span class="sxs-lookup"><span data-stu-id="e1044-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1044-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1044-135">Requirements</span></span>



| <span data-ttu-id="e1044-136">需求</span><span class="sxs-lookup"><span data-stu-id="e1044-136">Requirement</span></span> | <span data-ttu-id="e1044-137">值</span><span class="sxs-lookup"><span data-stu-id="e1044-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1044-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1044-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e1044-139">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1044-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1044-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1044-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e1044-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="e1044-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e1044-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e1044-142">End of client support</span></span><br/>    | <span data-ttu-id="e1044-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1044-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e1044-144">產品</span><span class="sxs-lookup"><span data-stu-id="e1044-144">Product</span></span><br/>                  | <span data-ttu-id="e1044-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e1044-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e1044-146">標頭</span><span class="sxs-lookup"><span data-stu-id="e1044-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1044-147"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1044-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1044-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1044-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1044-149">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="e1044-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

