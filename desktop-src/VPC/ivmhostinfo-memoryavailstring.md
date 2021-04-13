---
title: 'IVMHostInfo MemoryAvailString 屬性 (VPCCOMInterfaces .h) '
description: 以字串形式抓取主機電腦中可用的實體記憶體數量（以 mb 為單位）。
ms.assetid: a0f17dda-2042-4aec-9968-6662d32684cf
keywords:
- MemoryAvailString 屬性 Virtual PC
- MemoryAvailString 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，MemoryAvailString 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvailString
- IVMHostInfo.get_MemoryAvailString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea003b94d0d4604dfba3daf545a51b9d69b6708c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465773"
---
# <a name="ivmhostinfomemoryavailstring-property"></a><span data-ttu-id="7356f-106">IVMHostInfo：： MemoryAvailString 屬性</span><span class="sxs-lookup"><span data-stu-id="7356f-106">IVMHostInfo::MemoryAvailString property</span></span>

<span data-ttu-id="7356f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7356f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7356f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7356f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7356f-109">以字串形式抓取主機電腦中可用的實體記憶體數量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7356f-109">Retrieves the amount of available physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="7356f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7356f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7356f-111">語法</span><span class="sxs-lookup"><span data-stu-id="7356f-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvailString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="7356f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="7356f-112">Property value</span></span>

<span data-ttu-id="7356f-113">可用的實體記憶體（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="7356f-113">The available physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7356f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7356f-114">Error codes</span></span>



| <span data-ttu-id="7356f-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="7356f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7356f-116">意義</span><span class="sxs-lookup"><span data-stu-id="7356f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7356f-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7356f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7356f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="7356f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7356f-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7356f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7356f-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7356f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7356f-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7356f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7356f-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7356f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7356f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7356f-123">Requirements</span></span>



| <span data-ttu-id="7356f-124">需求</span><span class="sxs-lookup"><span data-stu-id="7356f-124">Requirement</span></span> | <span data-ttu-id="7356f-125">值</span><span class="sxs-lookup"><span data-stu-id="7356f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7356f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7356f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7356f-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7356f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7356f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7356f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7356f-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="7356f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7356f-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7356f-130">End of client support</span></span><br/>    | <span data-ttu-id="7356f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7356f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7356f-132">產品</span><span class="sxs-lookup"><span data-stu-id="7356f-132">Product</span></span><br/>                  | <span data-ttu-id="7356f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7356f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7356f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7356f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7356f-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7356f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7356f-136">IID</span><span class="sxs-lookup"><span data-stu-id="7356f-136">IID</span></span><br/>                      | <span data-ttu-id="7356f-137">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="7356f-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7356f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7356f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7356f-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="7356f-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

