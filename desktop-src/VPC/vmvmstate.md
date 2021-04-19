---
title: 'VMVMState 列舉 (VPCCOMInterfaces) '
description: 指定虛擬機器的狀態。
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- VMVMState 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967757"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="bbd98-104">VMVMState 列舉</span><span class="sxs-lookup"><span data-stu-id="bbd98-104">VMVMState enumeration</span></span>

<span data-ttu-id="bbd98-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="bbd98-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bbd98-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="bbd98-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bbd98-107">指定虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="bbd98-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd98-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbd98-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a><span data-ttu-id="bbd98-109">常數</span><span class="sxs-lookup"><span data-stu-id="bbd98-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bbd98-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="bbd98-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-111">如果虛擬機器存在) ，則不應發生的狀態 (無效。</span><span class="sxs-lookup"><span data-stu-id="bbd98-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState \_ TurnedOff**</span><span class="sxs-lookup"><span data-stu-id="bbd98-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-113">關閉且不儲存。</span><span class="sxs-lookup"><span data-stu-id="bbd98-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ 已儲存**</span><span class="sxs-lookup"><span data-stu-id="bbd98-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-115">Off，但會儲存來賓。</span><span class="sxs-lookup"><span data-stu-id="bbd98-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState \_ TurningOn**</span><span class="sxs-lookup"><span data-stu-id="bbd98-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-117">開啟的進程。</span><span class="sxs-lookup"><span data-stu-id="bbd98-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState \_ 還原**</span><span class="sxs-lookup"><span data-stu-id="bbd98-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-119">正在還原狀態。</span><span class="sxs-lookup"><span data-stu-id="bbd98-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState \_ 正在執行**</span><span class="sxs-lookup"><span data-stu-id="bbd98-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-121">正在執行且未暫停。</span><span class="sxs-lookup"><span data-stu-id="bbd98-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState 已 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="bbd98-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-123">正在執行和暫停。</span><span class="sxs-lookup"><span data-stu-id="bbd98-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState \_ 儲存**</span><span class="sxs-lookup"><span data-stu-id="bbd98-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-125">正在儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="bbd98-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState \_ TurningOff**</span><span class="sxs-lookup"><span data-stu-id="bbd98-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-127">關閉的進程。</span><span class="sxs-lookup"><span data-stu-id="bbd98-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState \_ MergingDrives**</span><span class="sxs-lookup"><span data-stu-id="bbd98-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-129">在合併復原磁片磁碟機的過程中。</span><span class="sxs-lookup"><span data-stu-id="bbd98-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="bbd98-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState \_ DeleteMachine**</span><span class="sxs-lookup"><span data-stu-id="bbd98-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="bbd98-131">正在刪除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bbd98-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbd98-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbd98-132">Requirements</span></span>



| <span data-ttu-id="bbd98-133">需求</span><span class="sxs-lookup"><span data-stu-id="bbd98-133">Requirement</span></span> | <span data-ttu-id="bbd98-134">值</span><span class="sxs-lookup"><span data-stu-id="bbd98-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd98-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbd98-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd98-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bbd98-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbd98-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbd98-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd98-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="bbd98-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bbd98-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bbd98-139">End of client support</span></span><br/>    | <span data-ttu-id="bbd98-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbd98-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bbd98-141">產品</span><span class="sxs-lookup"><span data-stu-id="bbd98-141">Product</span></span><br/>                  | <span data-ttu-id="bbd98-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bbd98-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bbd98-143">標頭</span><span class="sxs-lookup"><span data-stu-id="bbd98-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbd98-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd98-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd98-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbd98-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd98-146">**IVMVirtualMachine：： State**</span><span class="sxs-lookup"><span data-stu-id="bbd98-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="bbd98-147">**IVMVirtualMachineEvents：： OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="bbd98-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="bbd98-148">**IVMVirtualPCEvents::OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="bbd98-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

