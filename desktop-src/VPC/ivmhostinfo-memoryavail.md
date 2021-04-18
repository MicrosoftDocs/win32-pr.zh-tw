---
title: 'IVMHostInfo MemoryAvail 屬性 (VPCCOMInterfaces .h) '
description: 抓取主機電腦中可用的實體記憶體數量（以 mb 為單位）。
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- MemoryAvail 屬性 Virtual PC
- MemoryAvail 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，MemoryAvail 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df6be8bf62595720d01372ee891184952a0dd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965752"
---
# <a name="ivmhostinfomemoryavail-property"></a><span data-ttu-id="25fc1-106">IVMHostInfo：： MemoryAvail 屬性</span><span class="sxs-lookup"><span data-stu-id="25fc1-106">IVMHostInfo::MemoryAvail property</span></span>

<span data-ttu-id="25fc1-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="25fc1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="25fc1-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="25fc1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="25fc1-109">抓取主機電腦中可用的實體記憶體數量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="25fc1-109">Retrieves the amount of available physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="25fc1-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="25fc1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fc1-111">語法</span><span class="sxs-lookup"><span data-stu-id="25fc1-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="25fc1-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="25fc1-112">Property value</span></span>

<span data-ttu-id="25fc1-113">可用的實體記憶體（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="25fc1-113">The available physical memory, in megabytes.</span></span> <span data-ttu-id="25fc1-114">此值為 VT  DECIMAL 類型的變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25fc1-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25fc1-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="25fc1-115">Error codes</span></span>



| <span data-ttu-id="25fc1-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="25fc1-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="25fc1-117">意義</span><span class="sxs-lookup"><span data-stu-id="25fc1-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="25fc1-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25fc1-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="25fc1-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="25fc1-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="25fc1-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="25fc1-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="25fc1-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="25fc1-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="25fc1-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="25fc1-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="25fc1-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="25fc1-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="25fc1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="25fc1-124">Requirements</span></span>



| <span data-ttu-id="25fc1-125">需求</span><span class="sxs-lookup"><span data-stu-id="25fc1-125">Requirement</span></span> | <span data-ttu-id="25fc1-126">值</span><span class="sxs-lookup"><span data-stu-id="25fc1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fc1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25fc1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="25fc1-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25fc1-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25fc1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25fc1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="25fc1-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="25fc1-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="25fc1-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="25fc1-131">End of client support</span></span><br/>    | <span data-ttu-id="25fc1-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25fc1-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="25fc1-133">產品</span><span class="sxs-lookup"><span data-stu-id="25fc1-133">Product</span></span><br/>                  | <span data-ttu-id="25fc1-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="25fc1-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="25fc1-135">標頭</span><span class="sxs-lookup"><span data-stu-id="25fc1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="25fc1-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="25fc1-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="25fc1-137">IID</span><span class="sxs-lookup"><span data-stu-id="25fc1-137">IID</span></span><br/>                      | <span data-ttu-id="25fc1-138">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="25fc1-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="25fc1-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25fc1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fc1-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="25fc1-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

