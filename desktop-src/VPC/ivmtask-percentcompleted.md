---
title: 'IVMTask PercentCompleted 屬性 (VPCCOMInterfaces .h) '
description: 捕獲工作的完成百分比。
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- PercentCompleted 屬性 Virtual PC
- PercentCompleted 屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，PercentCompleted 屬性
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686306"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="c1a56-106">IVMTask：:P ercentCompleted 屬性</span><span class="sxs-lookup"><span data-stu-id="c1a56-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="c1a56-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="c1a56-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c1a56-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="c1a56-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c1a56-109">捕獲工作的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="c1a56-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="c1a56-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c1a56-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a56-111">語法</span><span class="sxs-lookup"><span data-stu-id="c1a56-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="c1a56-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="c1a56-112">Property value</span></span>

<span data-ttu-id="c1a56-113">目前的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="c1a56-113">The current completion percentage.</span></span> <span data-ttu-id="c1a56-114">值是介於0和100之間的數位。</span><span class="sxs-lookup"><span data-stu-id="c1a56-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c1a56-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1a56-115">Error codes</span></span>



| <span data-ttu-id="c1a56-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="c1a56-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c1a56-117">意義</span><span class="sxs-lookup"><span data-stu-id="c1a56-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c1a56-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c1a56-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c1a56-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c1a56-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c1a56-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c1a56-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c1a56-121">參數值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c1a56-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="c1a56-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c1a56-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c1a56-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1a56-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c1a56-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1a56-124">Requirements</span></span>



| <span data-ttu-id="c1a56-125">需求</span><span class="sxs-lookup"><span data-stu-id="c1a56-125">Requirement</span></span> | <span data-ttu-id="c1a56-126">值</span><span class="sxs-lookup"><span data-stu-id="c1a56-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a56-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1a56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a56-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1a56-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1a56-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1a56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a56-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="c1a56-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c1a56-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c1a56-131">End of client support</span></span><br/>    | <span data-ttu-id="c1a56-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1a56-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c1a56-133">產品</span><span class="sxs-lookup"><span data-stu-id="c1a56-133">Product</span></span><br/>                  | <span data-ttu-id="c1a56-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c1a56-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c1a56-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c1a56-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1a56-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a56-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c1a56-137">IID</span><span class="sxs-lookup"><span data-stu-id="c1a56-137">IID</span></span><br/>                      | <span data-ttu-id="c1a56-138">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="c1a56-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="c1a56-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1a56-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a56-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="c1a56-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

