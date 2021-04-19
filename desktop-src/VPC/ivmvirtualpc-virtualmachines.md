---
title: 'IVMVirtualPC VirtualMachines 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器的可列舉集合。
ms.assetid: 9e8dcd65-7cf8-4cdd-a412-62cbb96eb8ec
keywords:
- VirtualMachines 屬性 Virtual PC
- VirtualMachines 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，VirtualMachines 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualMachines
- IVMVirtualPC.get_VirtualMachines
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e141208994fa3d759074e7cbb294e1e2158917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968386"
---
# <a name="ivmvirtualpcvirtualmachines-property"></a><span data-ttu-id="40c8f-106">IVMVirtualPC：： VirtualMachines 屬性</span><span class="sxs-lookup"><span data-stu-id="40c8f-106">IVMVirtualPC::VirtualMachines property</span></span>

<span data-ttu-id="40c8f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="40c8f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40c8f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="40c8f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40c8f-109">抓取虛擬機器的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="40c8f-109">Retrieves an enumerable collection of virtual machines.</span></span>

<span data-ttu-id="40c8f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="40c8f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c8f-111">語法</span><span class="sxs-lookup"><span data-stu-id="40c8f-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachines(
  [out, retval] IVMVirtualMachineCollection **virtualMachineCollection
);
```



## <a name="property-value"></a><span data-ttu-id="40c8f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="40c8f-112">Property value</span></span>

<span data-ttu-id="40c8f-113">[**IVMVirtualMachine**](ivmvirtualmachine.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="40c8f-113">A collection of [**IVMVirtualMachine**](ivmvirtualmachine.md) objects.</span></span> <span data-ttu-id="40c8f-114">請參閱 [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)。</span><span class="sxs-lookup"><span data-stu-id="40c8f-114">See [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="40c8f-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="40c8f-115">Error codes</span></span>



| <span data-ttu-id="40c8f-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="40c8f-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="40c8f-117">意義</span><span class="sxs-lookup"><span data-stu-id="40c8f-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40c8f-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40c8f-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="40c8f-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="40c8f-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="40c8f-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="40c8f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="40c8f-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="40c8f-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="40c8f-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="40c8f-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="40c8f-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="40c8f-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="40c8f-124"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="40c8f-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="40c8f-125">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="40c8f-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="40c8f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="40c8f-126">Requirements</span></span>



| <span data-ttu-id="40c8f-127">需求</span><span class="sxs-lookup"><span data-stu-id="40c8f-127">Requirement</span></span> | <span data-ttu-id="40c8f-128">值</span><span class="sxs-lookup"><span data-stu-id="40c8f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c8f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40c8f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40c8f-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40c8f-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40c8f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40c8f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40c8f-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="40c8f-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40c8f-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="40c8f-133">End of client support</span></span><br/>    | <span data-ttu-id="40c8f-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40c8f-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40c8f-135">產品</span><span class="sxs-lookup"><span data-stu-id="40c8f-135">Product</span></span><br/>                  | <span data-ttu-id="40c8f-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40c8f-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40c8f-137">標頭</span><span class="sxs-lookup"><span data-stu-id="40c8f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c8f-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="40c8f-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40c8f-139">IID</span><span class="sxs-lookup"><span data-stu-id="40c8f-139">IID</span></span><br/>                      | <span data-ttu-id="40c8f-140">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="40c8f-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="40c8f-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40c8f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c8f-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="40c8f-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

