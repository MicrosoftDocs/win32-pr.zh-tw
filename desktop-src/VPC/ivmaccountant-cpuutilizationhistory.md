---
title: 'IVMAccountant CPUUtilizationHistory 屬性 (VPCCOMInterfaces .h) '
description: 將此虛擬機器的最新 CPU 使用率， (為百分比值陣列) 。
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- CPUUtilizationHistory 屬性 Virtual PC
- CPUUtilizationHistory 屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面 Virtual PC，CPUUtilizationHistory 屬性
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466844"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="82f5c-106">IVMAccountant：： CPUUtilizationHistory 屬性</span><span class="sxs-lookup"><span data-stu-id="82f5c-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="82f5c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="82f5c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="82f5c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="82f5c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="82f5c-109">將此虛擬機器的最新 CPU 使用率， (為百分比值陣列) 。</span><span class="sxs-lookup"><span data-stu-id="82f5c-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="82f5c-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="82f5c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f5c-111">語法</span><span class="sxs-lookup"><span data-stu-id="82f5c-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="82f5c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="82f5c-112">Property value</span></span>

<span data-ttu-id="82f5c-113">此虛擬機器的最近 CPU 使用方式。</span><span class="sxs-lookup"><span data-stu-id="82f5c-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="82f5c-114">這項資料會以60個元素的陣列傳回，表示過去一分鐘內每秒的 CPU 使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="82f5c-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="82f5c-115">Variant 類型是 VT \_ 陣列 \| vt \_ UI1。</span><span class="sxs-lookup"><span data-stu-id="82f5c-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="82f5c-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="82f5c-116">Error codes</span></span>



| <span data-ttu-id="82f5c-117">名稱/值</span><span class="sxs-lookup"><span data-stu-id="82f5c-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="82f5c-118">意義</span><span class="sxs-lookup"><span data-stu-id="82f5c-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82f5c-119"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="82f5c-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="82f5c-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="82f5c-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="82f5c-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="82f5c-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="82f5c-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="82f5c-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="82f5c-123"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="82f5c-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="82f5c-124">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="82f5c-124">The virtual machine is not running.</span></span> <span data-ttu-id="82f5c-125">所有60陣列元素都會設定為0。</span><span class="sxs-lookup"><span data-stu-id="82f5c-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="82f5c-126"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="82f5c-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="82f5c-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="82f5c-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="82f5c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f5c-128">Requirements</span></span>



| <span data-ttu-id="82f5c-129">需求</span><span class="sxs-lookup"><span data-stu-id="82f5c-129">Requirement</span></span> | <span data-ttu-id="82f5c-130">值</span><span class="sxs-lookup"><span data-stu-id="82f5c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="82f5c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82f5c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="82f5c-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82f5c-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82f5c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82f5c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="82f5c-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="82f5c-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="82f5c-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="82f5c-135">End of client support</span></span><br/>    | <span data-ttu-id="82f5c-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="82f5c-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="82f5c-137">產品</span><span class="sxs-lookup"><span data-stu-id="82f5c-137">Product</span></span><br/>                  | <span data-ttu-id="82f5c-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="82f5c-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="82f5c-139">標頭</span><span class="sxs-lookup"><span data-stu-id="82f5c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="82f5c-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="82f5c-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="82f5c-141">IID</span><span class="sxs-lookup"><span data-stu-id="82f5c-141">IID</span></span><br/>                      | <span data-ttu-id="82f5c-142">IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="82f5c-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="82f5c-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82f5c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f5c-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="82f5c-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

