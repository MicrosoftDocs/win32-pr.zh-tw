---
title: 'IVMAccountant CPUUtilization 屬性 (VPCCOMInterfaces .h) '
description: 抓取此虛擬機器目前的 CPU 使用率百分比。
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- CPUUtilization 屬性 Virtual PC
- CPUUtilization 屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面 Virtual PC，CPUUtilization 屬性
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935035"
---
# <a name="ivmaccountantcpuutilization-property"></a><span data-ttu-id="6e067-106">IVMAccountant：： CPUUtilization 屬性</span><span class="sxs-lookup"><span data-stu-id="6e067-106">IVMAccountant::CPUUtilization property</span></span>

<span data-ttu-id="6e067-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="6e067-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6e067-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="6e067-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6e067-109">抓取此虛擬機器目前的 CPU 使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="6e067-109">Retrieves the percentage of current CPU utilization for this virtual machine.</span></span>

<span data-ttu-id="6e067-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6e067-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e067-111">語法</span><span class="sxs-lookup"><span data-stu-id="6e067-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="6e067-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6e067-112">Property value</span></span>

<span data-ttu-id="6e067-113">目前的 CPU 使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="6e067-113">The percentage of current CPU utilization.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e067-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6e067-114">Error codes</span></span>



| <span data-ttu-id="6e067-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="6e067-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6e067-116">意義</span><span class="sxs-lookup"><span data-stu-id="6e067-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6e067-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e067-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6e067-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="6e067-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="6e067-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6e067-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6e067-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6e067-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="6e067-121"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6e067-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="6e067-122">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="6e067-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="6e067-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6e067-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6e067-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6e067-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="6e067-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e067-125">Requirements</span></span>



| <span data-ttu-id="6e067-126">需求</span><span class="sxs-lookup"><span data-stu-id="6e067-126">Requirement</span></span> | <span data-ttu-id="6e067-127">值</span><span class="sxs-lookup"><span data-stu-id="6e067-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e067-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e067-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6e067-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e067-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e067-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e067-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6e067-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="6e067-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6e067-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6e067-132">End of client support</span></span><br/>    | <span data-ttu-id="6e067-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e067-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6e067-134">產品</span><span class="sxs-lookup"><span data-stu-id="6e067-134">Product</span></span><br/>                  | <span data-ttu-id="6e067-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6e067-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6e067-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6e067-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e067-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e067-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6e067-138">IID</span><span class="sxs-lookup"><span data-stu-id="6e067-138">IID</span></span><br/>                      | <span data-ttu-id="6e067-139">IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="6e067-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="6e067-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e067-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e067-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="6e067-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

