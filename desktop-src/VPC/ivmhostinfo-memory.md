---
title: 'IVMHostInfo Memory 屬性 (VPCCOMInterfaces .h) '
description: 抓取主機電腦中的實體記憶體總數量（以 mb 為單位）。
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Memory 屬性 Virtual PC
- Memory 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，Memory 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f634bfe3bf81dcb13c9f09d8f19a5a82aa6902
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968377"
---
# <a name="ivmhostinfomemory-property"></a><span data-ttu-id="395d1-106">IVMHostInfo：： Memory 屬性</span><span class="sxs-lookup"><span data-stu-id="395d1-106">IVMHostInfo::Memory property</span></span>

<span data-ttu-id="395d1-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="395d1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="395d1-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="395d1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="395d1-109">抓取主機電腦中的實體記憶體總數量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="395d1-109">Retrieves the total amount of physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="395d1-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="395d1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="395d1-111">語法</span><span class="sxs-lookup"><span data-stu-id="395d1-111">Syntax</span></span>


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="395d1-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="395d1-112">Property value</span></span>

<span data-ttu-id="395d1-113">實體記憶體的總容量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="395d1-113">The total amount of physical memory, in megabytes.</span></span> <span data-ttu-id="395d1-114">此值為 VT  DECIMAL 類型的變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="395d1-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="395d1-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="395d1-115">Error codes</span></span>



| <span data-ttu-id="395d1-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="395d1-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="395d1-117">意義</span><span class="sxs-lookup"><span data-stu-id="395d1-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="395d1-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="395d1-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="395d1-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="395d1-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="395d1-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="395d1-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="395d1-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="395d1-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="395d1-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="395d1-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="395d1-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="395d1-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="395d1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="395d1-124">Requirements</span></span>



| <span data-ttu-id="395d1-125">需求</span><span class="sxs-lookup"><span data-stu-id="395d1-125">Requirement</span></span> | <span data-ttu-id="395d1-126">值</span><span class="sxs-lookup"><span data-stu-id="395d1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="395d1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="395d1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="395d1-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="395d1-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="395d1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="395d1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="395d1-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="395d1-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="395d1-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="395d1-131">End of client support</span></span><br/>    | <span data-ttu-id="395d1-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="395d1-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="395d1-133">產品</span><span class="sxs-lookup"><span data-stu-id="395d1-133">Product</span></span><br/>                  | <span data-ttu-id="395d1-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="395d1-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="395d1-135">標頭</span><span class="sxs-lookup"><span data-stu-id="395d1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="395d1-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="395d1-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="395d1-137">IID</span><span class="sxs-lookup"><span data-stu-id="395d1-137">IID</span></span><br/>                      | <span data-ttu-id="395d1-138">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="395d1-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="395d1-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="395d1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395d1-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="395d1-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

