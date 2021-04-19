---
title: 'IVMVirtualMachine Memory 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器中的實體記憶體數量（以 mb 為單位）。
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Memory 屬性 Virtual PC
- Memory 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Memory 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991117"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="812ba-106">IVMVirtualMachine：： Memory 屬性</span><span class="sxs-lookup"><span data-stu-id="812ba-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="812ba-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="812ba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="812ba-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="812ba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="812ba-109">抓取和設定虛擬機器中的實體記憶體數量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="812ba-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="812ba-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="812ba-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="812ba-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="812ba-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="812ba-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="812ba-112">Property value</span></span>

<span data-ttu-id="812ba-113">指定實體記憶體的數量（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="812ba-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="812ba-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="812ba-114">Error codes</span></span>



| <span data-ttu-id="812ba-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="812ba-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="812ba-116">意義</span><span class="sxs-lookup"><span data-stu-id="812ba-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="812ba-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="812ba-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="812ba-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="812ba-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="812ba-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="812ba-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="812ba-121"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="812ba-122">參數無效或超出範圍。</span><span class="sxs-lookup"><span data-stu-id="812ba-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="812ba-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="812ba-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="812ba-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="812ba-125"><dt>VM \_E \_ PREF \_ \_ 找不到</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="812ba-126">找不到喜好設定。</span><span class="sxs-lookup"><span data-stu-id="812ba-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="812ba-127"><dt>VM \_E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="812ba-128">虛擬機器正在執行或已儲存。</span><span class="sxs-lookup"><span data-stu-id="812ba-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="812ba-129"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="812ba-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="812ba-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="812ba-131">備註</span><span class="sxs-lookup"><span data-stu-id="812ba-131">Remarks</span></span>

<span data-ttu-id="812ba-132">虛擬機器中的實體記憶體數量必須至少為 4 MB。</span><span class="sxs-lookup"><span data-stu-id="812ba-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="812ba-133">記憶體的上限取決於主機設定，但最多可以是 3712 MB。</span><span class="sxs-lookup"><span data-stu-id="812ba-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="812ba-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="812ba-134">Requirements</span></span>



| <span data-ttu-id="812ba-135">需求</span><span class="sxs-lookup"><span data-stu-id="812ba-135">Requirement</span></span> | <span data-ttu-id="812ba-136">值</span><span class="sxs-lookup"><span data-stu-id="812ba-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="812ba-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="812ba-137">Minimum supported client</span></span><br/> | <span data-ttu-id="812ba-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="812ba-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="812ba-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="812ba-139">Minimum supported server</span></span><br/> | <span data-ttu-id="812ba-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="812ba-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="812ba-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="812ba-141">End of client support</span></span><br/>    | <span data-ttu-id="812ba-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="812ba-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="812ba-143">產品</span><span class="sxs-lookup"><span data-stu-id="812ba-143">Product</span></span><br/>                  | <span data-ttu-id="812ba-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="812ba-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="812ba-145">標頭</span><span class="sxs-lookup"><span data-stu-id="812ba-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="812ba-146"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="812ba-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="812ba-147">IID</span><span class="sxs-lookup"><span data-stu-id="812ba-147">IID</span></span><br/>                      | <span data-ttu-id="812ba-148">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="812ba-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="812ba-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="812ba-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="812ba-150">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="812ba-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

