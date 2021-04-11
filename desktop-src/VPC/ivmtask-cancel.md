---
title: 'IVMTask Cancel 方法 (VPCCOMInterfaces) '
description: 取消工作。
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Cancel 方法 Virtual PC
- Cancel 方法 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，Cancel 方法
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931b7229f3c81166f4610e873c23eca979c8897b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317471"
---
# <a name="ivmtaskcancel-method"></a><span data-ttu-id="e014b-106">IVMTask：： Cancel 方法</span><span class="sxs-lookup"><span data-stu-id="e014b-106">IVMTask::Cancel method</span></span>

<span data-ttu-id="e014b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e014b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e014b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e014b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e014b-109">取消工作。</span><span class="sxs-lookup"><span data-stu-id="e014b-109">Cancels the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="e014b-110">語法</span><span class="sxs-lookup"><span data-stu-id="e014b-110">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="e014b-111">參數</span><span class="sxs-lookup"><span data-stu-id="e014b-111">Parameters</span></span>

<span data-ttu-id="e014b-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e014b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e014b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e014b-113">Return value</span></span>

<span data-ttu-id="e014b-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e014b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e014b-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e014b-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="e014b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e014b-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e014b-117"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e014b-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e014b-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e014b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e014b-119"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="e014b-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="e014b-120">無法取消工作。</span><span class="sxs-lookup"><span data-stu-id="e014b-120">The task cannot be canceled.</span></span><br/>      |
| <dl> <span data-ttu-id="e014b-121"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e014b-121"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e014b-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e014b-122">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e014b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e014b-123">Requirements</span></span>



| <span data-ttu-id="e014b-124">需求</span><span class="sxs-lookup"><span data-stu-id="e014b-124">Requirement</span></span> | <span data-ttu-id="e014b-125">值</span><span class="sxs-lookup"><span data-stu-id="e014b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e014b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e014b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e014b-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e014b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e014b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e014b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e014b-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="e014b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e014b-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e014b-130">End of client support</span></span><br/>    | <span data-ttu-id="e014b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e014b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e014b-132">產品</span><span class="sxs-lookup"><span data-stu-id="e014b-132">Product</span></span><br/>                  | <span data-ttu-id="e014b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e014b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e014b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e014b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e014b-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e014b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e014b-136">IID</span><span class="sxs-lookup"><span data-stu-id="e014b-136">IID</span></span><br/>                      | <span data-ttu-id="e014b-137">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="e014b-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="e014b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e014b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e014b-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="e014b-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

