---
title: 'IVMVirtualMachine Startup2 方法 (VPCCOMInterfaces .h) '
description: 使用 advanced 選項，從未初始化或已儲存的狀態啟動虛擬機器。
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Startup2 方法 Virtual PC
- Startup2 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Startup2 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384741"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="96d2a-106">IVMVirtualMachine：： Startup2 方法</span><span class="sxs-lookup"><span data-stu-id="96d2a-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="96d2a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="96d2a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96d2a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="96d2a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96d2a-109">使用 advanced options 從未初始化或已儲存的狀態啟動虛擬機器 (VM) 。</span><span class="sxs-lookup"><span data-stu-id="96d2a-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="96d2a-110">即使父磁片的時間戳記已變更，此方法也會提供一種機制來啟動具有差異磁片的 VM。</span><span class="sxs-lookup"><span data-stu-id="96d2a-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d2a-111">語法</span><span class="sxs-lookup"><span data-stu-id="96d2a-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="96d2a-112">參數</span><span class="sxs-lookup"><span data-stu-id="96d2a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d2a-113">*startupOption* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96d2a-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d2a-114">Advanced 啟動選項。</span><span class="sxs-lookup"><span data-stu-id="96d2a-114">The advanced startup option.</span></span> <span data-ttu-id="96d2a-115">可能的值來自 [**VMStartupOption**](vmstartupoption.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="96d2a-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="96d2a-116">*startupTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="96d2a-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="96d2a-117">[**IVMTask**](ivmtask.md)物件，用來追蹤開始順序的完成進度。</span><span class="sxs-lookup"><span data-stu-id="96d2a-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d2a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="96d2a-118">Return value</span></span>

<span data-ttu-id="96d2a-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="96d2a-119">This method can return one of these values.</span></span>



| <span data-ttu-id="96d2a-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="96d2a-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="96d2a-121">Description</span><span class="sxs-lookup"><span data-stu-id="96d2a-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96d2a-122"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="96d2a-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="96d2a-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="96d2a-124"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="96d2a-125">*StartupOption* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="96d2a-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="96d2a-126"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="96d2a-127">*StartupTask* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="96d2a-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="96d2a-128"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="96d2a-129">呼叫端必須具有執行存取權限，才能啟動此 VM。</span><span class="sxs-lookup"><span data-stu-id="96d2a-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="96d2a-130"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="96d2a-131">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="96d2a-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="96d2a-132"><dt>**VM \_E \_ 0xA0040203 \_ \_ 資源**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="96d2a-133">沒有足夠的主機資源。</span><span class="sxs-lookup"><span data-stu-id="96d2a-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="96d2a-134"><dt>**VM \_電子 \_ 0xA0040204 太 \_ 多 \_ vm**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="96d2a-135">有太多作用中的 Vm。</span><span class="sxs-lookup"><span data-stu-id="96d2a-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="96d2a-136"><dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="96d2a-137">VM 已在執行中。</span><span class="sxs-lookup"><span data-stu-id="96d2a-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="96d2a-138"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="96d2a-139">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="96d2a-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="96d2a-140">備註</span><span class="sxs-lookup"><span data-stu-id="96d2a-140">Remarks</span></span>

<span data-ttu-id="96d2a-141">下列值可透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性來傳回。</span><span class="sxs-lookup"><span data-stu-id="96d2a-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="96d2a-142">[**錯誤碼**](ivmtask-error.md) /值</span><span class="sxs-lookup"><span data-stu-id="96d2a-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="96d2a-143">Description</span><span class="sxs-lookup"><span data-stu-id="96d2a-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="96d2a-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950) </span><span class="sxs-lookup"><span data-stu-id="96d2a-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="96d2a-145">硬體不支援虛擬化。</span><span class="sxs-lookup"><span data-stu-id="96d2a-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="96d2a-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951) </span><span class="sxs-lookup"><span data-stu-id="96d2a-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="96d2a-147">硬體虛擬化已停用。</span><span class="sxs-lookup"><span data-stu-id="96d2a-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="96d2a-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952) </span><span class="sxs-lookup"><span data-stu-id="96d2a-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="96d2a-149">Virtual PC 2007 和 Windows Virtual PC 皆已安裝。</span><span class="sxs-lookup"><span data-stu-id="96d2a-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="96d2a-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953) </span><span class="sxs-lookup"><span data-stu-id="96d2a-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="96d2a-151">已安裝其他虛擬化軟體。</span><span class="sxs-lookup"><span data-stu-id="96d2a-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="96d2a-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203) </span><span class="sxs-lookup"><span data-stu-id="96d2a-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="96d2a-153">沒有足夠的主機資源。</span><span class="sxs-lookup"><span data-stu-id="96d2a-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="96d2a-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="96d2a-154">Requirements</span></span>



| <span data-ttu-id="96d2a-155">需求</span><span class="sxs-lookup"><span data-stu-id="96d2a-155">Requirement</span></span> | <span data-ttu-id="96d2a-156">值</span><span class="sxs-lookup"><span data-stu-id="96d2a-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d2a-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96d2a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="96d2a-158">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96d2a-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96d2a-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96d2a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="96d2a-160">都不支援</span><span class="sxs-lookup"><span data-stu-id="96d2a-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96d2a-161">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="96d2a-161">End of client support</span></span><br/>    | <span data-ttu-id="96d2a-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96d2a-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96d2a-163">產品</span><span class="sxs-lookup"><span data-stu-id="96d2a-163">Product</span></span><br/>                  | <span data-ttu-id="96d2a-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96d2a-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96d2a-165">標頭</span><span class="sxs-lookup"><span data-stu-id="96d2a-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d2a-166"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="96d2a-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="96d2a-167">IID</span><span class="sxs-lookup"><span data-stu-id="96d2a-167">IID</span></span><br/>                      | <span data-ttu-id="96d2a-168">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="96d2a-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="96d2a-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96d2a-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d2a-170">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="96d2a-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

