---
title: 'IVMVirtualMachineEvents OnTripleFault 方法 (VPCCOMInterfaces .h) '
description: 收到虛擬機器有三個錯誤的通知。
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- OnTripleFault 方法 Virtual PC
- OnTripleFault 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnTripleFault 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509099"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a><span data-ttu-id="e54eb-106">IVMVirtualMachineEvents：： OnTripleFault 方法</span><span class="sxs-lookup"><span data-stu-id="e54eb-106">IVMVirtualMachineEvents::OnTripleFault method</span></span>

<span data-ttu-id="e54eb-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e54eb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e54eb-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e54eb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e54eb-109">收到虛擬機器有三個錯誤的通知。</span><span class="sxs-lookup"><span data-stu-id="e54eb-109">Receives notification that a virtual machine has triple-faulted.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54eb-110">語法</span><span class="sxs-lookup"><span data-stu-id="e54eb-110">Syntax</span></span>


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a><span data-ttu-id="e54eb-111">參數</span><span class="sxs-lookup"><span data-stu-id="e54eb-111">Parameters</span></span>

<span data-ttu-id="e54eb-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e54eb-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e54eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e54eb-113">Return value</span></span>

<span data-ttu-id="e54eb-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e54eb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e54eb-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e54eb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e54eb-116">備註</span><span class="sxs-lookup"><span data-stu-id="e54eb-116">Remarks</span></span>

<span data-ttu-id="e54eb-117">當虛擬機器有三個錯誤時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e54eb-117">This method is called when a virtual machine has triple-faulted.</span></span> <span data-ttu-id="e54eb-118">用戶端程式必須執行這個介面方法，以接收來自 IVMVirtualMachine 的 vmVirtualMachineEvent \_ TripleFault 事件的[](ivmvirtualmachine.md)通知。</span><span class="sxs-lookup"><span data-stu-id="e54eb-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_TripleFault event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e54eb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e54eb-119">Requirements</span></span>



| <span data-ttu-id="e54eb-120">需求</span><span class="sxs-lookup"><span data-stu-id="e54eb-120">Requirement</span></span> | <span data-ttu-id="e54eb-121">值</span><span class="sxs-lookup"><span data-stu-id="e54eb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e54eb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e54eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e54eb-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54eb-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e54eb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e54eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e54eb-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="e54eb-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e54eb-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e54eb-126">End of client support</span></span><br/>    | <span data-ttu-id="e54eb-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e54eb-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e54eb-128">產品</span><span class="sxs-lookup"><span data-stu-id="e54eb-128">Product</span></span><br/>                  | <span data-ttu-id="e54eb-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e54eb-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e54eb-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e54eb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e54eb-131"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e54eb-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e54eb-132">IID</span><span class="sxs-lookup"><span data-stu-id="e54eb-132">IID</span></span><br/>                      | <span data-ttu-id="e54eb-133">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="e54eb-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="e54eb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e54eb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54eb-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="e54eb-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

