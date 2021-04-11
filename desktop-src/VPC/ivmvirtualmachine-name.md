---
title: 'IVMVirtualMachine Name 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器設定的名稱。
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Name 屬性 Virtual PC
- Name 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Name 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104100"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="0d11c-106">IVMVirtualMachine：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="0d11c-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="0d11c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="0d11c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d11c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="0d11c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d11c-109">抓取和設定虛擬機器設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d11c-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="0d11c-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0d11c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d11c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d11c-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="0d11c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="0d11c-112">Property value</span></span>

<span data-ttu-id="0d11c-113">指定虛擬機器設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d11c-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="0d11c-114">名稱的長度不能超過80個字元，且包含虛擬機器名稱設定檔的完整路徑總長度不能超過 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="0d11c-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d11c-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0d11c-115">Error codes</span></span>



| <span data-ttu-id="0d11c-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="0d11c-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="0d11c-117">意義</span><span class="sxs-lookup"><span data-stu-id="0d11c-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d11c-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="0d11c-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0d11c-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0d11c-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="0d11c-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0d11c-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="0d11c-122"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="0d11c-123">參數無效或為空字串。</span><span class="sxs-lookup"><span data-stu-id="0d11c-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d11c-124"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="0d11c-125">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="0d11c-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0d11c-126"><dt>VM \_E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="0d11c-127">虛擬機器正在執行或已儲存。</span><span class="sxs-lookup"><span data-stu-id="0d11c-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="0d11c-128"><dt>VM \_E \_ 設定 \_ 沒有 \_ 名稱</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="0d11c-129">*VirtualMachineName* 參數是空的。</span><span class="sxs-lookup"><span data-stu-id="0d11c-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="0d11c-130"><dt>VM \_E \_ CONFIG \_ NAME \_ 太 \_ 長</dt> <dt>0xA00400401</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="0d11c-131">參數包含太多字元。</span><span class="sxs-lookup"><span data-stu-id="0d11c-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="0d11c-132"><dt>VM \_E \_ CONFIG \_ NAME \_ 不正確 \_ CHAR</dt> <dt>0xA0040402</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="0d11c-133">參數包含下列其中一個無效字元 " \* ？： <>/ \| \\ " "。</span><span class="sxs-lookup"><span data-stu-id="0d11c-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="0d11c-134"><dt>VM \_E \_ 設定 \_ 重複 \_ 名稱</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="0d11c-135">指定的名稱已存在，作為另一部虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d11c-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="0d11c-136"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="0d11c-137">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0d11c-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="0d11c-138">備註</span><span class="sxs-lookup"><span data-stu-id="0d11c-138">Remarks</span></span>

<span data-ttu-id="0d11c-139">虛擬機器名稱不區分大小寫，例如 "MyVM" 和 "MyVM" 指的是相同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d11c-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="0d11c-140">這是 [**IVMVirtualMachine**](ivmvirtualmachine.md)的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="0d11c-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="0d11c-141">如果 VPC.exe 正在執行，且 VM 已儲存，則設定 [ **名稱** ] 屬性將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0d11c-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="0d11c-142">如果 VPC.exe 未執行且儲存了 VM，則下次啟動 VPC.exe 時，設定 **Name** 屬性會成功。</span><span class="sxs-lookup"><span data-stu-id="0d11c-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d11c-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d11c-143">Requirements</span></span>



| <span data-ttu-id="0d11c-144">需求</span><span class="sxs-lookup"><span data-stu-id="0d11c-144">Requirement</span></span> | <span data-ttu-id="0d11c-145">值</span><span class="sxs-lookup"><span data-stu-id="0d11c-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d11c-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d11c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0d11c-147">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d11c-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d11c-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d11c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0d11c-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="0d11c-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0d11c-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0d11c-150">End of client support</span></span><br/>    | <span data-ttu-id="0d11c-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d11c-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0d11c-152">產品</span><span class="sxs-lookup"><span data-stu-id="0d11c-152">Product</span></span><br/>                  | <span data-ttu-id="0d11c-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0d11c-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0d11c-154">標頭</span><span class="sxs-lookup"><span data-stu-id="0d11c-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d11c-155"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d11c-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0d11c-156">IID</span><span class="sxs-lookup"><span data-stu-id="0d11c-156">IID</span></span><br/>                      | <span data-ttu-id="0d11c-157">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0d11c-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0d11c-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d11c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d11c-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="0d11c-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

