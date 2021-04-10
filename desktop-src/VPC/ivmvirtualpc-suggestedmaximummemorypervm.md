---
title: 'IVMVirtualPC SuggestedMaximumMemoryPerVM 屬性 (VPCCOMInterfaces .h) '
description: 抓取每部虛擬機器的建議最大實體記憶體數量（以 mb 為單位），以避免主機上的記憶體不足狀況。
ms.assetid: 533cca40-f41d-4717-87ae-d8072414a637
keywords:
- SuggestedMaximumMemoryPerVM 屬性 Virtual PC
- SuggestedMaximumMemoryPerVM 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，SuggestedMaximumMemoryPerVM 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.SuggestedMaximumMemoryPerVM
- IVMVirtualPC.get_SuggestedMaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142c4ade861116876342d598fbf10b5925fa100e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025487"
---
# <a name="ivmvirtualpcsuggestedmaximummemorypervm-property"></a><span data-ttu-id="e8743-106">IVMVirtualPC：： SuggestedMaximumMemoryPerVM 屬性</span><span class="sxs-lookup"><span data-stu-id="e8743-106">IVMVirtualPC::SuggestedMaximumMemoryPerVM property</span></span>

<span data-ttu-id="e8743-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e8743-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8743-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e8743-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8743-109">抓取每部虛擬機器的建議最大實體記憶體數量（以 mb 為單位），以避免主機上的記憶體不足狀況。</span><span class="sxs-lookup"><span data-stu-id="e8743-109">Retrieves the suggested maximum allowable quantity of physical memory per virtual machine, in megabytes, to avoid low memory conditions on the host.</span></span>

<span data-ttu-id="e8743-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e8743-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8743-111">語法</span><span class="sxs-lookup"><span data-stu-id="e8743-111">Syntax</span></span>


```C++
HRESULT get_SuggestedMaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="e8743-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e8743-112">Property value</span></span>

<span data-ttu-id="e8743-113">每一虛擬機器的最大允許數量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="e8743-113">The suggested maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8743-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e8743-114">Error codes</span></span>



| <span data-ttu-id="e8743-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="e8743-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="e8743-116">意義</span><span class="sxs-lookup"><span data-stu-id="e8743-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8743-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8743-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e8743-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e8743-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e8743-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e8743-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e8743-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e8743-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="e8743-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e8743-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e8743-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8743-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e8743-123"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e8743-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e8743-124">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e8743-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e8743-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8743-125">Requirements</span></span>



| <span data-ttu-id="e8743-126">需求</span><span class="sxs-lookup"><span data-stu-id="e8743-126">Requirement</span></span> | <span data-ttu-id="e8743-127">值</span><span class="sxs-lookup"><span data-stu-id="e8743-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8743-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8743-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8743-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8743-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8743-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8743-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8743-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="e8743-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8743-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e8743-132">End of client support</span></span><br/>    | <span data-ttu-id="e8743-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8743-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8743-134">產品</span><span class="sxs-lookup"><span data-stu-id="e8743-134">Product</span></span><br/>                  | <span data-ttu-id="e8743-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8743-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8743-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e8743-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8743-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8743-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8743-138">IID</span><span class="sxs-lookup"><span data-stu-id="e8743-138">IID</span></span><br/>                      | <span data-ttu-id="e8743-139">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e8743-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e8743-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8743-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8743-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e8743-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

