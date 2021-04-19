---
title: 'VMShutdownAction 列舉 (VPCCOMInterfaces) '
description: 指定當主機關機或 vpc.exe 進程結束時，如何關閉虛擬機器。
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- VMShutdownAction 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969587"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="23c78-104">VMShutdownAction 列舉</span><span class="sxs-lookup"><span data-stu-id="23c78-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="23c78-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="23c78-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="23c78-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="23c78-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="23c78-107">指定當主機關機或 vpc.exe 進程結束時，如何關閉虛擬機器 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="23c78-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c78-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="23c78-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="23c78-109">常數</span><span class="sxs-lookup"><span data-stu-id="23c78-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23c78-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ 儲存**</span><span class="sxs-lookup"><span data-stu-id="23c78-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="23c78-111">儲存 VM 狀態。</span><span class="sxs-lookup"><span data-stu-id="23c78-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="23c78-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ TurnOff**</span><span class="sxs-lookup"><span data-stu-id="23c78-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="23c78-113">在不復原磁片磁碟機的情況下關閉 VM。</span><span class="sxs-lookup"><span data-stu-id="23c78-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="23c78-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction \_ 關機**</span><span class="sxs-lookup"><span data-stu-id="23c78-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="23c78-115">如果有整合元件可供使用，請關閉 VM 上的客體作業系統而不復原磁片磁碟機，否則會儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="23c78-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23c78-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="23c78-116">Requirements</span></span>



| <span data-ttu-id="23c78-117">需求</span><span class="sxs-lookup"><span data-stu-id="23c78-117">Requirement</span></span> | <span data-ttu-id="23c78-118">值</span><span class="sxs-lookup"><span data-stu-id="23c78-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c78-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23c78-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23c78-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23c78-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23c78-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23c78-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23c78-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="23c78-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="23c78-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="23c78-123">End of client support</span></span><br/>    | <span data-ttu-id="23c78-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23c78-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="23c78-125">產品</span><span class="sxs-lookup"><span data-stu-id="23c78-125">Product</span></span><br/>                  | <span data-ttu-id="23c78-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="23c78-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="23c78-127">標頭</span><span class="sxs-lookup"><span data-stu-id="23c78-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c78-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="23c78-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c78-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23c78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c78-130">Windows Virtual PC 列舉</span><span class="sxs-lookup"><span data-stu-id="23c78-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="23c78-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="23c78-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

