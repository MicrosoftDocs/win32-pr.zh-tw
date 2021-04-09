---
title: 'IVMAccountant DiskBytesWritten 屬性 (VPCCOMInterfaces .h) '
description: 此虛擬機器的所有儲存控制器所寫入的位元組總數。
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- DiskBytesWritten 屬性 Virtual PC
- DiskBytesWritten 屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面 Virtual PC，DiskBytesWritten 屬性
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9ad27acf538af25daec676289df5e7664b169
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844275"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a><span data-ttu-id="b7836-106">IVMAccountant：:D iskBytesWritten 屬性</span><span class="sxs-lookup"><span data-stu-id="b7836-106">IVMAccountant::DiskBytesWritten property</span></span>

<span data-ttu-id="b7836-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b7836-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7836-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b7836-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7836-109">抓取此虛擬機器的所有儲存控制器寫入的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="b7836-109">Retrieves the total number of bytes written by all storage controllers for this virtual machine.</span></span>

<span data-ttu-id="b7836-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b7836-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7836-111">語法</span><span class="sxs-lookup"><span data-stu-id="b7836-111">Syntax</span></span>


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a><span data-ttu-id="b7836-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="b7836-112">Property value</span></span>

<span data-ttu-id="b7836-113">位元組總數。</span><span class="sxs-lookup"><span data-stu-id="b7836-113">The total number of bytes.</span></span> <span data-ttu-id="b7836-114">這項資料會以 **VT \_ DECIMAL** 類型的 **變數** 傳回。</span><span class="sxs-lookup"><span data-stu-id="b7836-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7836-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b7836-115">Error codes</span></span>



| <span data-ttu-id="b7836-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="b7836-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b7836-117">意義</span><span class="sxs-lookup"><span data-stu-id="b7836-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b7836-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7836-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b7836-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b7836-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="b7836-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b7836-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b7836-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b7836-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="b7836-122"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b7836-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="b7836-123">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="b7836-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="b7836-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b7836-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b7836-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7836-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="b7836-126">備註</span><span class="sxs-lookup"><span data-stu-id="b7836-126">Remarks</span></span>

<span data-ttu-id="b7836-127">請注意，當虛擬機器從儲存狀態開機、重設或還原時，磁片 i/o 統計資料會重設為零。</span><span class="sxs-lookup"><span data-stu-id="b7836-127">Note that disk I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7836-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7836-128">Requirements</span></span>



| <span data-ttu-id="b7836-129">需求</span><span class="sxs-lookup"><span data-stu-id="b7836-129">Requirement</span></span> | <span data-ttu-id="b7836-130">值</span><span class="sxs-lookup"><span data-stu-id="b7836-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7836-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7836-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b7836-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7836-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7836-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7836-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b7836-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="b7836-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7836-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b7836-135">End of client support</span></span><br/>    | <span data-ttu-id="b7836-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7836-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7836-137">產品</span><span class="sxs-lookup"><span data-stu-id="b7836-137">Product</span></span><br/>                  | <span data-ttu-id="b7836-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7836-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7836-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b7836-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7836-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7836-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b7836-141">IID</span><span class="sxs-lookup"><span data-stu-id="b7836-141">IID</span></span><br/>                      | <span data-ttu-id="b7836-142">IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="b7836-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="b7836-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7836-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7836-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="b7836-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

