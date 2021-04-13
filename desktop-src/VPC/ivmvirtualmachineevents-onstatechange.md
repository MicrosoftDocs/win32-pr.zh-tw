---
title: 'IVMVirtualMachineEvents OnStateChange 方法 (VPCCOMInterfaces .h) '
description: '收到虛擬機器的狀態已變更的通知。 |IVMVirtualMachineEvents OnStateChange 方法 (VPCCOMInterfaces .h) '
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- OnStateChange 方法 Virtual PC
- OnStateChange 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnStateChange 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322504"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="0010b-107">IVMVirtualMachineEvents：： OnStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="0010b-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="0010b-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0010b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0010b-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0010b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0010b-110">收到虛擬機器的狀態已變更的通知。</span><span class="sxs-lookup"><span data-stu-id="0010b-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0010b-111">語法</span><span class="sxs-lookup"><span data-stu-id="0010b-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="0010b-112">參數</span><span class="sxs-lookup"><span data-stu-id="0010b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0010b-113">*virtualMachineState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0010b-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0010b-114">虛擬機器的新狀態。</span><span class="sxs-lookup"><span data-stu-id="0010b-114">The new state of the virtual machine.</span></span> <span data-ttu-id="0010b-115">如需值的清單，請參閱 [**VMVMState**](vmvmstate.md)。</span><span class="sxs-lookup"><span data-stu-id="0010b-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0010b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0010b-116">Return value</span></span>

<span data-ttu-id="0010b-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0010b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0010b-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0010b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0010b-119">備註</span><span class="sxs-lookup"><span data-stu-id="0010b-119">Remarks</span></span>

<span data-ttu-id="0010b-120">當此虛擬機器的狀態變更時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0010b-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="0010b-121">用戶端程式必須執行這個介面方法，以接收來自 IVMVirtualMachine 的 vmVirtualMachineEvent \_ StateChanged 事件的[](ivmvirtualmachine.md)通知。</span><span class="sxs-lookup"><span data-stu-id="0010b-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0010b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0010b-122">Requirements</span></span>



| <span data-ttu-id="0010b-123">需求</span><span class="sxs-lookup"><span data-stu-id="0010b-123">Requirement</span></span> | <span data-ttu-id="0010b-124">值</span><span class="sxs-lookup"><span data-stu-id="0010b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0010b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0010b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0010b-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0010b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0010b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0010b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0010b-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="0010b-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0010b-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0010b-129">End of client support</span></span><br/>    | <span data-ttu-id="0010b-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0010b-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0010b-131">產品</span><span class="sxs-lookup"><span data-stu-id="0010b-131">Product</span></span><br/>                  | <span data-ttu-id="0010b-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0010b-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0010b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="0010b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0010b-134"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0010b-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0010b-135">IID</span><span class="sxs-lookup"><span data-stu-id="0010b-135">IID</span></span><br/>                      | <span data-ttu-id="0010b-136">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="0010b-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0010b-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0010b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0010b-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="0010b-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

