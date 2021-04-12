---
title: 'VMLogoffType 列舉 (VPCCOMInterfaces) '
description: 指定如何關閉虛擬機器。
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- VMLogoffType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025052"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="b7bdb-104">VMLogoffType 列舉</span><span class="sxs-lookup"><span data-stu-id="b7bdb-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="b7bdb-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b7bdb-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7bdb-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b7bdb-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7bdb-107">指定如何關閉 (VM) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b7bdb-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7bdb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7bdb-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="b7bdb-109">常數</span><span class="sxs-lookup"><span data-stu-id="b7bdb-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b7bdb-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="b7bdb-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="b7bdb-111">來賓 VM 中的登出是正常的。</span><span class="sxs-lookup"><span data-stu-id="b7bdb-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="b7bdb-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ 強制**</span><span class="sxs-lookup"><span data-stu-id="b7bdb-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="b7bdb-113">來賓 VM 中的登出是強制的。</span><span class="sxs-lookup"><span data-stu-id="b7bdb-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="b7bdb-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ 外部**</span><span class="sxs-lookup"><span data-stu-id="b7bdb-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="b7bdb-115">來賓 VM 中的登出是使用 [**IVMGuestOS：：登出**](ivmguestos-logoff.md) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="b7bdb-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7bdb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7bdb-116">Requirements</span></span>



| <span data-ttu-id="b7bdb-117">需求</span><span class="sxs-lookup"><span data-stu-id="b7bdb-117">Requirement</span></span> | <span data-ttu-id="b7bdb-118">值</span><span class="sxs-lookup"><span data-stu-id="b7bdb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bdb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7bdb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7bdb-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7bdb-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7bdb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7bdb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7bdb-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="b7bdb-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7bdb-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b7bdb-123">End of client support</span></span><br/>    | <span data-ttu-id="b7bdb-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7bdb-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7bdb-125">產品</span><span class="sxs-lookup"><span data-stu-id="b7bdb-125">Product</span></span><br/>                  | <span data-ttu-id="b7bdb-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7bdb-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7bdb-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b7bdb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7bdb-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7bdb-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7bdb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7bdb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bdb-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="b7bdb-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

