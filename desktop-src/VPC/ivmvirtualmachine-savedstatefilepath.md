---
title: 'IVMVirtualMachine SavedStateFilePath 屬性 (VPCCOMInterfaces .h) '
description: 抓取儲存狀態檔案的完整路徑。
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- SavedStateFilePath 屬性 Virtual PC
- SavedStateFilePath 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，SavedStateFilePath 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105341"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="f8e5c-106">IVMVirtualMachine：： SavedStateFilePath 屬性</span><span class="sxs-lookup"><span data-stu-id="f8e5c-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="f8e5c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f8e5c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f8e5c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f8e5c-109">抓取儲存狀態檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="f8e5c-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e5c-111">語法</span><span class="sxs-lookup"><span data-stu-id="f8e5c-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="f8e5c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f8e5c-112">Property value</span></span>

<span data-ttu-id="f8e5c-113">虛擬機器儲存狀態檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8e5c-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f8e5c-114">Error codes</span></span>



| <span data-ttu-id="f8e5c-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="f8e5c-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="f8e5c-116">意義</span><span class="sxs-lookup"><span data-stu-id="f8e5c-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8e5c-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8e5c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="f8e5c-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="f8e5c-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f8e5c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="f8e5c-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="f8e5c-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="f8e5c-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="f8e5c-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="f8e5c-123"><dt>VM \_E \_ VM \_ 沒有 \_ 儲存的 \_ 狀態</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="f8e5c-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="f8e5c-124">虛擬機器沒有相關聯的儲存狀態檔案。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="f8e5c-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f8e5c-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="f8e5c-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8e5c-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="f8e5c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8e5c-127">Requirements</span></span>



| <span data-ttu-id="f8e5c-128">需求</span><span class="sxs-lookup"><span data-stu-id="f8e5c-128">Requirement</span></span> | <span data-ttu-id="f8e5c-129">值</span><span class="sxs-lookup"><span data-stu-id="f8e5c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e5c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8e5c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e5c-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8e5c-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8e5c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8e5c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e5c-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="f8e5c-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f8e5c-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f8e5c-134">End of client support</span></span><br/>    | <span data-ttu-id="f8e5c-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8e5c-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f8e5c-136">產品</span><span class="sxs-lookup"><span data-stu-id="f8e5c-136">Product</span></span><br/>                  | <span data-ttu-id="f8e5c-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f8e5c-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f8e5c-138">標頭</span><span class="sxs-lookup"><span data-stu-id="f8e5c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e5c-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e5c-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f8e5c-140">IID</span><span class="sxs-lookup"><span data-stu-id="f8e5c-140">IID</span></span><br/>                      | <span data-ttu-id="f8e5c-141">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f8e5c-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f8e5c-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8e5c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e5c-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f8e5c-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

