---
title: 'IVMTask ID 屬性 (VPCCOMInterfaces .h) '
description: 抓取這項工作的唯一識別碼。
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- ID 屬性 Virtual PC
- ID 屬性 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，ID 屬性
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844144"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="4ba4a-106">IVMTask：： ID 屬性</span><span class="sxs-lookup"><span data-stu-id="4ba4a-106">IVMTask::ID property</span></span>

<span data-ttu-id="4ba4a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4ba4a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="4ba4a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4ba4a-109">抓取這項工作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="4ba4a-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba4a-111">語法</span><span class="sxs-lookup"><span data-stu-id="4ba4a-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="4ba4a-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="4ba4a-112">Property value</span></span>

<span data-ttu-id="4ba4a-113">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ba4a-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4ba4a-114">Error codes</span></span>



| <span data-ttu-id="4ba4a-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="4ba4a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4ba4a-116">意義</span><span class="sxs-lookup"><span data-stu-id="4ba4a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4ba4a-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4ba4a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4ba4a-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4ba4a-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4ba4a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4ba4a-120">參數值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="4ba4a-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4ba4a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4ba4a-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ba4a-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4ba4a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ba4a-123">Requirements</span></span>



| <span data-ttu-id="4ba4a-124">需求</span><span class="sxs-lookup"><span data-stu-id="4ba4a-124">Requirement</span></span> | <span data-ttu-id="4ba4a-125">值</span><span class="sxs-lookup"><span data-stu-id="4ba4a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba4a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ba4a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba4a-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ba4a-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ba4a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ba4a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba4a-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="4ba4a-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4ba4a-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4ba4a-130">End of client support</span></span><br/>    | <span data-ttu-id="4ba4a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ba4a-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4ba4a-132">產品</span><span class="sxs-lookup"><span data-stu-id="4ba4a-132">Product</span></span><br/>                  | <span data-ttu-id="4ba4a-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4ba4a-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4ba4a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="4ba4a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ba4a-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba4a-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4ba4a-136">IID</span><span class="sxs-lookup"><span data-stu-id="4ba4a-136">IID</span></span><br/>                      | <span data-ttu-id="4ba4a-137">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="4ba4a-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="4ba4a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ba4a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba4a-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="4ba4a-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

