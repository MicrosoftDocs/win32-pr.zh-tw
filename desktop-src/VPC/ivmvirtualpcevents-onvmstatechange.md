---
title: 'IVMVirtualPCEvents OnVMStateChange 方法 (VPCCOMInterfaces .h) '
description: '收到虛擬機器的狀態已變更的通知。 |IVMVirtualPCEvents OnVMStateChange 方法 (VPCCOMInterfaces .h) '
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- OnVMStateChange 方法 Virtual PC
- OnVMStateChange 方法 Virtual PC，IVMVirtualPCEvents 介面
- IVMVirtualPCEvents 介面 Virtual PC，OnVMStateChange 方法
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991957"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="f24e5-107">IVMVirtualPCEvents：： OnVMStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="f24e5-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="f24e5-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f24e5-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f24e5-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f24e5-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f24e5-110">收到虛擬機器的狀態已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="f24e5-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24e5-111">語法</span><span class="sxs-lookup"><span data-stu-id="f24e5-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="f24e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="f24e5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f24e5-113">*virtualMachineConfig* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f24e5-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24e5-114">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f24e5-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f24e5-115">*virtualMachineState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f24e5-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24e5-116">虛擬機器的新狀態。</span><span class="sxs-lookup"><span data-stu-id="f24e5-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f24e5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f24e5-117">Return value</span></span>

<span data-ttu-id="f24e5-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f24e5-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f24e5-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f24e5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f24e5-120">備註</span><span class="sxs-lookup"><span data-stu-id="f24e5-120">Remarks</span></span>

<span data-ttu-id="f24e5-121">用戶端程式必須執行這個介面方法，以接收來自 [**IVMVirtualPC**](ivmvirtualpc.md)的 **vmVirtualPCEvent \_ VMStateChanged** 事件的通知。</span><span class="sxs-lookup"><span data-stu-id="f24e5-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="f24e5-122">若要監視特定的虛擬機器，請使用 [**IVMVirtualMachineEvents：： OnStateChange**](ivmvirtualmachineevents-onstatechange.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f24e5-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f24e5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f24e5-123">Requirements</span></span>



| <span data-ttu-id="f24e5-124">需求</span><span class="sxs-lookup"><span data-stu-id="f24e5-124">Requirement</span></span> | <span data-ttu-id="f24e5-125">值</span><span class="sxs-lookup"><span data-stu-id="f24e5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f24e5-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f24e5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f24e5-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f24e5-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f24e5-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f24e5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f24e5-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="f24e5-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f24e5-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f24e5-130">End of client support</span></span><br/>    | <span data-ttu-id="f24e5-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f24e5-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f24e5-132">產品</span><span class="sxs-lookup"><span data-stu-id="f24e5-132">Product</span></span><br/>                  | <span data-ttu-id="f24e5-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f24e5-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f24e5-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f24e5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f24e5-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f24e5-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f24e5-136">IID</span><span class="sxs-lookup"><span data-stu-id="f24e5-136">IID</span></span><br/>                      | <span data-ttu-id="f24e5-137">DIID \_ IVMVirtualPCEvents 定義為 efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="f24e5-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f24e5-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f24e5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24e5-139">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="f24e5-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

