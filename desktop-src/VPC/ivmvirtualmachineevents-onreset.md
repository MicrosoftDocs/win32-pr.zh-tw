---
title: 'IVMVirtualMachineEvents OnReset 方法 (VPCCOMInterfaces .h) '
description: 接收已重設虛擬機器的通知。
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- OnReset 方法 Virtual PC
- OnReset 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnReset 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933875"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="ce6be-106">IVMVirtualMachineEvents：： OnReset 方法</span><span class="sxs-lookup"><span data-stu-id="ce6be-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="ce6be-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ce6be-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce6be-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ce6be-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce6be-109">接收已重設虛擬機器的通知。</span><span class="sxs-lookup"><span data-stu-id="ce6be-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6be-110">語法</span><span class="sxs-lookup"><span data-stu-id="ce6be-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="ce6be-111">參數</span><span class="sxs-lookup"><span data-stu-id="ce6be-111">Parameters</span></span>

<span data-ttu-id="ce6be-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ce6be-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce6be-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce6be-113">Return value</span></span>

<span data-ttu-id="ce6be-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ce6be-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce6be-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce6be-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6be-116">備註</span><span class="sxs-lookup"><span data-stu-id="ce6be-116">Remarks</span></span>

<span data-ttu-id="ce6be-117">當虛擬機器已重設時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="ce6be-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="ce6be-118">用戶端程式必須執行此介面方法，以接收來自 IVMVirtualMachine 的 vmVirtualMachineEvent \_ 重設事件[](ivmvirtualmachine.md)的通知。</span><span class="sxs-lookup"><span data-stu-id="ce6be-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6be-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce6be-119">Requirements</span></span>



| <span data-ttu-id="ce6be-120">需求</span><span class="sxs-lookup"><span data-stu-id="ce6be-120">Requirement</span></span> | <span data-ttu-id="ce6be-121">值</span><span class="sxs-lookup"><span data-stu-id="ce6be-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6be-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce6be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6be-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce6be-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce6be-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce6be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6be-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="ce6be-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce6be-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ce6be-126">End of client support</span></span><br/>    | <span data-ttu-id="ce6be-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce6be-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce6be-128">產品</span><span class="sxs-lookup"><span data-stu-id="ce6be-128">Product</span></span><br/>                  | <span data-ttu-id="ce6be-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce6be-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce6be-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ce6be-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6be-131"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6be-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ce6be-132">IID</span><span class="sxs-lookup"><span data-stu-id="ce6be-132">IID</span></span><br/>                      | <span data-ttu-id="ce6be-133">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="ce6be-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ce6be-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce6be-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6be-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="ce6be-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

