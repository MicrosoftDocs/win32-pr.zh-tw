---
title: 'IVMTaskCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 捕獲此集合中的工作數目。
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMTaskCollection 介面
- IVMTaskCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843948"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="95bfb-106">IVMTaskCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="95bfb-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="95bfb-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="95bfb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="95bfb-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="95bfb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="95bfb-109">捕獲此集合中的工作數目。</span><span class="sxs-lookup"><span data-stu-id="95bfb-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="95bfb-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="95bfb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95bfb-111">語法</span><span class="sxs-lookup"><span data-stu-id="95bfb-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="95bfb-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="95bfb-112">Property value</span></span>

<span data-ttu-id="95bfb-113">工作的數目。</span><span class="sxs-lookup"><span data-stu-id="95bfb-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="95bfb-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="95bfb-114">Error codes</span></span>



| <span data-ttu-id="95bfb-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="95bfb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="95bfb-116">意義</span><span class="sxs-lookup"><span data-stu-id="95bfb-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="95bfb-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="95bfb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="95bfb-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="95bfb-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="95bfb-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="95bfb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="95bfb-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="95bfb-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="95bfb-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="95bfb-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="95bfb-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95bfb-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="95bfb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="95bfb-123">Requirements</span></span>



| <span data-ttu-id="95bfb-124">需求</span><span class="sxs-lookup"><span data-stu-id="95bfb-124">Requirement</span></span> | <span data-ttu-id="95bfb-125">值</span><span class="sxs-lookup"><span data-stu-id="95bfb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95bfb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95bfb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="95bfb-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95bfb-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95bfb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95bfb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="95bfb-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="95bfb-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="95bfb-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="95bfb-130">End of client support</span></span><br/>    | <span data-ttu-id="95bfb-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95bfb-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="95bfb-132">產品</span><span class="sxs-lookup"><span data-stu-id="95bfb-132">Product</span></span><br/>                  | <span data-ttu-id="95bfb-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="95bfb-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="95bfb-134">標頭</span><span class="sxs-lookup"><span data-stu-id="95bfb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="95bfb-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="95bfb-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="95bfb-136">IID</span><span class="sxs-lookup"><span data-stu-id="95bfb-136">IID</span></span><br/>                      | <span data-ttu-id="95bfb-137">IID \_ IVMTaskCollection 定義為5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="95bfb-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="95bfb-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95bfb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95bfb-139">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="95bfb-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

