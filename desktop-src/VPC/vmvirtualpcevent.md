---
title: 'VMVirtualPCEvent 列舉 (VPCCOMInterfaces) '
description: 指定 Windows Virtual PC 事件。
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- VMVirtualPCEvent 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025484"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="0232d-104">VMVirtualPCEvent 列舉</span><span class="sxs-lookup"><span data-stu-id="0232d-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="0232d-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0232d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0232d-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0232d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0232d-107">指定 Windows Virtual PC 事件。</span><span class="sxs-lookup"><span data-stu-id="0232d-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="0232d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0232d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="0232d-109">常數</span><span class="sxs-lookup"><span data-stu-id="0232d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0232d-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent \_ VMStateChange**</span><span class="sxs-lookup"><span data-stu-id="0232d-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="0232d-111">虛擬機器的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="0232d-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0232d-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent \_ EventLogged**</span><span class="sxs-lookup"><span data-stu-id="0232d-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="0232d-113">Virtual PC 已記錄事件。</span><span class="sxs-lookup"><span data-stu-id="0232d-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0232d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0232d-114">Requirements</span></span>



| <span data-ttu-id="0232d-115">需求</span><span class="sxs-lookup"><span data-stu-id="0232d-115">Requirement</span></span> | <span data-ttu-id="0232d-116">值</span><span class="sxs-lookup"><span data-stu-id="0232d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0232d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0232d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0232d-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0232d-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0232d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0232d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0232d-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="0232d-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0232d-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0232d-121">End of client support</span></span><br/>    | <span data-ttu-id="0232d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0232d-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0232d-123">產品</span><span class="sxs-lookup"><span data-stu-id="0232d-123">Product</span></span><br/>                  | <span data-ttu-id="0232d-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0232d-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0232d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0232d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0232d-126"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0232d-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0232d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0232d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0232d-128">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="0232d-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

