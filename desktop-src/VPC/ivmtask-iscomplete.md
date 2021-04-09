---
title: 'IVMTask C.iscomplete 屬性 (VPCCOMInterfaces .h) '
description: 判斷工作是否已完成。
ms.assetid: 181fa220-4de2-4ab3-950b-fffc4fe4de64
keywords:
- C.iscomplete 屬性 Virtual PC
- C.iscomplete 屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，C.iscomplete 屬性
topic_type:
- apiref
api_name:
- IVMTask.IsComplete
- IVMTask.get_IsComplete
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbf046b4a16ef4e907f1fec0126d08815ca2955
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934500"
---
# <a name="ivmtaskiscomplete-property"></a><span data-ttu-id="d77f4-106">IVMTask：： C.iscomplete 屬性</span><span class="sxs-lookup"><span data-stu-id="d77f4-106">IVMTask::IsComplete property</span></span>

<span data-ttu-id="d77f4-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d77f4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d77f4-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d77f4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d77f4-109">判斷工作是否已完成。</span><span class="sxs-lookup"><span data-stu-id="d77f4-109">Determines whether the task has completed.</span></span>

<span data-ttu-id="d77f4-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d77f4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d77f4-111">語法</span><span class="sxs-lookup"><span data-stu-id="d77f4-111">Syntax</span></span>


```C++
HRESULT get_IsComplete(
  [out, retval] VARIANT_BOOL *isComplete
);
```



## <a name="property-value"></a><span data-ttu-id="d77f4-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d77f4-112">Property value</span></span>

<span data-ttu-id="d77f4-113">如果工作已完成，則 **為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d77f4-113">**TRUE** if the task has completed and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d77f4-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d77f4-114">Error codes</span></span>



| <span data-ttu-id="d77f4-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="d77f4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d77f4-116">意義</span><span class="sxs-lookup"><span data-stu-id="d77f4-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d77f4-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d77f4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d77f4-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d77f4-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d77f4-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d77f4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d77f4-120">參數值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d77f4-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="d77f4-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d77f4-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d77f4-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d77f4-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d77f4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d77f4-123">Requirements</span></span>



| <span data-ttu-id="d77f4-124">需求</span><span class="sxs-lookup"><span data-stu-id="d77f4-124">Requirement</span></span> | <span data-ttu-id="d77f4-125">值</span><span class="sxs-lookup"><span data-stu-id="d77f4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d77f4-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d77f4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d77f4-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d77f4-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d77f4-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d77f4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d77f4-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="d77f4-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d77f4-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d77f4-130">End of client support</span></span><br/>    | <span data-ttu-id="d77f4-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d77f4-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d77f4-132">產品</span><span class="sxs-lookup"><span data-stu-id="d77f4-132">Product</span></span><br/>                  | <span data-ttu-id="d77f4-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d77f4-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d77f4-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d77f4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d77f4-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d77f4-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d77f4-136">IID</span><span class="sxs-lookup"><span data-stu-id="d77f4-136">IID</span></span><br/>                      | <span data-ttu-id="d77f4-137">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="d77f4-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="d77f4-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d77f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77f4-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="d77f4-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

