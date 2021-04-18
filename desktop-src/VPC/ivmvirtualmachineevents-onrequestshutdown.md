---
title: 'IVMVirtualMachineEvents OnRequestShutdown 方法 (VPCCOMInterfaces .h) '
description: 接收已發出關機要求的通知。
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- OnRequestShutdown 方法 Virtual PC
- OnRequestShutdown 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnRequestShutdown 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465765"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="7a787-106">IVMVirtualMachineEvents：： OnRequestShutdown 方法</span><span class="sxs-lookup"><span data-stu-id="7a787-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="7a787-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7a787-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a787-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7a787-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a787-109">接收已發出關機要求的通知。</span><span class="sxs-lookup"><span data-stu-id="7a787-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a787-110">語法</span><span class="sxs-lookup"><span data-stu-id="7a787-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="7a787-111">參數</span><span class="sxs-lookup"><span data-stu-id="7a787-111">Parameters</span></span>

<span data-ttu-id="7a787-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7a787-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a787-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a787-113">Return value</span></span>

<span data-ttu-id="7a787-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7a787-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7a787-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7a787-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a787-116">備註</span><span class="sxs-lookup"><span data-stu-id="7a787-116">Remarks</span></span>

<span data-ttu-id="7a787-117">每當虛擬機器會話即將關閉時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7a787-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="7a787-118">用戶端程式必須執行這個介面方法，以接收來自 [**IVMVirtualMachine**](ivmvirtualmachine.md)的 **vmVirtualMachineEvent \_ RequestShutdown** 事件的通知。</span><span class="sxs-lookup"><span data-stu-id="7a787-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="7a787-119">只有當虛擬機器會話即將關閉時，才會傳送此事件通知。</span><span class="sxs-lookup"><span data-stu-id="7a787-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="7a787-120">作業系統關閉常式（例如 [**IVMGuestOS：： shutdown**](ivmguestos-shutdown.md)）不會直接引發此事件，除非它們也嘗試執行虛擬硬體的軟體電源。</span><span class="sxs-lookup"><span data-stu-id="7a787-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a787-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a787-121">Requirements</span></span>



| <span data-ttu-id="7a787-122">需求</span><span class="sxs-lookup"><span data-stu-id="7a787-122">Requirement</span></span> | <span data-ttu-id="7a787-123">值</span><span class="sxs-lookup"><span data-stu-id="7a787-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a787-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a787-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7a787-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a787-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a787-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a787-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7a787-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="7a787-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a787-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7a787-128">End of client support</span></span><br/>    | <span data-ttu-id="7a787-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a787-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a787-130">產品</span><span class="sxs-lookup"><span data-stu-id="7a787-130">Product</span></span><br/>                  | <span data-ttu-id="7a787-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a787-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a787-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7a787-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a787-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a787-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7a787-134">IID</span><span class="sxs-lookup"><span data-stu-id="7a787-134">IID</span></span><br/>                      | <span data-ttu-id="7a787-135">DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="7a787-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7a787-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a787-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a787-137">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="7a787-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

