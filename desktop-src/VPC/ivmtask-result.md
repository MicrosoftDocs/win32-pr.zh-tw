---
title: 'IVMTask Result 屬性 (VPCCOMInterfaces .h) '
description: 捕獲工作的結果。
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- 結果屬性 Virtual PC
- 結果屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，Result 屬性
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934753"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="de591-106">IVMTask：： Result 屬性</span><span class="sxs-lookup"><span data-stu-id="de591-106">IVMTask::Result property</span></span>

<span data-ttu-id="de591-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="de591-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="de591-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="de591-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="de591-109">捕獲工作的結果。</span><span class="sxs-lookup"><span data-stu-id="de591-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="de591-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="de591-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de591-111">語法</span><span class="sxs-lookup"><span data-stu-id="de591-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="de591-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="de591-112">Property value</span></span>

<span data-ttu-id="de591-113">工作的結果。</span><span class="sxs-lookup"><span data-stu-id="de591-113">The result of the task.</span></span> <span data-ttu-id="de591-114">如需值的清單，請參閱 [**VMTaskResult**](vmtaskresult.md)。</span><span class="sxs-lookup"><span data-stu-id="de591-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="de591-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="de591-115">Error codes</span></span>



| <span data-ttu-id="de591-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="de591-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="de591-117">意義</span><span class="sxs-lookup"><span data-stu-id="de591-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="de591-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="de591-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="de591-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="de591-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="de591-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="de591-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="de591-121">參數值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="de591-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="de591-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="de591-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="de591-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="de591-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de591-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="de591-124">Requirements</span></span>



| <span data-ttu-id="de591-125">需求</span><span class="sxs-lookup"><span data-stu-id="de591-125">Requirement</span></span> | <span data-ttu-id="de591-126">值</span><span class="sxs-lookup"><span data-stu-id="de591-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de591-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de591-127">Minimum supported client</span></span><br/> | <span data-ttu-id="de591-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de591-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de591-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de591-129">Minimum supported server</span></span><br/> | <span data-ttu-id="de591-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="de591-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="de591-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="de591-131">End of client support</span></span><br/>    | <span data-ttu-id="de591-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de591-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="de591-133">產品</span><span class="sxs-lookup"><span data-stu-id="de591-133">Product</span></span><br/>                  | <span data-ttu-id="de591-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="de591-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="de591-135">標頭</span><span class="sxs-lookup"><span data-stu-id="de591-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="de591-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="de591-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="de591-137">IID</span><span class="sxs-lookup"><span data-stu-id="de591-137">IID</span></span><br/>                      | <span data-ttu-id="de591-138">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="de591-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="de591-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de591-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de591-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="de591-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

