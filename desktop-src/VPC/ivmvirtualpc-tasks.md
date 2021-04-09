---
title: 'IVMVirtualPC Tasks 屬性 (VPCCOMInterfaces .h) '
description: 捕獲工作的集合。
ms.assetid: bba9c4b4-c933-43c8-9fbc-f2beb59867cf
keywords:
- 工作屬性 Virtual PC
- Tasks 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC interface Virtual PC，Tasks 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.Tasks
- IVMVirtualPC.get_Tasks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83eb27a48654a52a5724768da4ecf38584ea1231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844020"
---
# <a name="ivmvirtualpctasks-property"></a><span data-ttu-id="3224a-106">IVMVirtualPC：： Tasks 屬性</span><span class="sxs-lookup"><span data-stu-id="3224a-106">IVMVirtualPC::Tasks property</span></span>

<span data-ttu-id="3224a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3224a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3224a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3224a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3224a-109">捕獲工作的集合。</span><span class="sxs-lookup"><span data-stu-id="3224a-109">Retrieves a collection of tasks.</span></span>

<span data-ttu-id="3224a-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3224a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3224a-111">語法</span><span class="sxs-lookup"><span data-stu-id="3224a-111">Syntax</span></span>


```C++
HRESULT get_Tasks(
  [out, retval] IVMTaskCollection **taskCollection
);
```



## <a name="property-value"></a><span data-ttu-id="3224a-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3224a-112">Property value</span></span>

<span data-ttu-id="3224a-113">[**IVMTask**](ivmtask.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="3224a-113">A collection of [**IVMTask**](ivmtask.md) objects.</span></span> <span data-ttu-id="3224a-114">請參閱 [**IVMTaskCollection**](ivmtaskcollection.md)。</span><span class="sxs-lookup"><span data-stu-id="3224a-114">See [**IVMTaskCollection**](ivmtaskcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="3224a-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3224a-115">Error codes</span></span>



| <span data-ttu-id="3224a-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="3224a-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="3224a-117">意義</span><span class="sxs-lookup"><span data-stu-id="3224a-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3224a-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3224a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="3224a-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3224a-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3224a-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3224a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="3224a-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3224a-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="3224a-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3224a-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="3224a-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3224a-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3224a-124"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3224a-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="3224a-125">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3224a-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3224a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3224a-126">Requirements</span></span>



| <span data-ttu-id="3224a-127">需求</span><span class="sxs-lookup"><span data-stu-id="3224a-127">Requirement</span></span> | <span data-ttu-id="3224a-128">值</span><span class="sxs-lookup"><span data-stu-id="3224a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3224a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3224a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3224a-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3224a-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3224a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3224a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3224a-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="3224a-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3224a-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3224a-133">End of client support</span></span><br/>    | <span data-ttu-id="3224a-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3224a-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3224a-135">產品</span><span class="sxs-lookup"><span data-stu-id="3224a-135">Product</span></span><br/>                  | <span data-ttu-id="3224a-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3224a-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3224a-137">標頭</span><span class="sxs-lookup"><span data-stu-id="3224a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3224a-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3224a-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3224a-139">IID</span><span class="sxs-lookup"><span data-stu-id="3224a-139">IID</span></span><br/>                      | <span data-ttu-id="3224a-140">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="3224a-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3224a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3224a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3224a-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="3224a-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

