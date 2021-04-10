---
title: 'IVMVirtualMachine 啟動方法 (VPCCOMInterfaces .h) '
description: 從未初始化或已儲存的狀態啟動虛擬機器。
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- 啟動方法虛擬電腦
- Startup 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC、Startup 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934863"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="14b1c-106">IVMVirtualMachine：： Startup 方法</span><span class="sxs-lookup"><span data-stu-id="14b1c-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="14b1c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="14b1c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="14b1c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="14b1c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="14b1c-109">從未初始化或已儲存的狀態啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b1c-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b1c-110">語法</span><span class="sxs-lookup"><span data-stu-id="14b1c-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="14b1c-111">參數</span><span class="sxs-lookup"><span data-stu-id="14b1c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b1c-112">*startupTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="14b1c-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="14b1c-113">[**IVMTask**](ivmtask.md)物件，可用來追蹤虛擬機器啟動順序的完成進度。</span><span class="sxs-lookup"><span data-stu-id="14b1c-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b1c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="14b1c-114">Return value</span></span>

<span data-ttu-id="14b1c-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="14b1c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="14b1c-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="14b1c-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="14b1c-117">Description</span><span class="sxs-lookup"><span data-stu-id="14b1c-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14b1c-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="14b1c-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="14b1c-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="14b1c-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="14b1c-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14b1c-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="14b1c-122"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="14b1c-123">呼叫端必須具有執行存取權限，才能啟動此虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b1c-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="14b1c-124"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="14b1c-125">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="14b1c-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="14b1c-126"><dt>**VM \_E \_ 0xA0040203 \_ \_ 資源**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="14b1c-127">沒有足夠的主機資源。</span><span class="sxs-lookup"><span data-stu-id="14b1c-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="14b1c-128"><dt>**VM \_電子 \_ 0xA0040204 太 \_ 多 \_ vm**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="14b1c-129">有太多作用中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b1c-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="14b1c-130"><dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="14b1c-131">虛擬機器已在執行中。</span><span class="sxs-lookup"><span data-stu-id="14b1c-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="14b1c-132"><dt>**VM \_E \_ 父 \_ 修改過**</dt>的 <dt>0xA00400687</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="14b1c-133">因為已修改父 VHD，所以無法啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b1c-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="14b1c-134"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="14b1c-135">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="14b1c-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="14b1c-136">備註</span><span class="sxs-lookup"><span data-stu-id="14b1c-136">Remarks</span></span>

<span data-ttu-id="14b1c-137">如果虛擬機器已儲存，則會從儲存的狀態還原。</span><span class="sxs-lookup"><span data-stu-id="14b1c-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="14b1c-138">下列值可透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性來傳回。</span><span class="sxs-lookup"><span data-stu-id="14b1c-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="14b1c-139">[**錯誤碼**](ivmtask-error.md) /值</span><span class="sxs-lookup"><span data-stu-id="14b1c-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="14b1c-140">Description</span><span class="sxs-lookup"><span data-stu-id="14b1c-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="14b1c-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950) </span><span class="sxs-lookup"><span data-stu-id="14b1c-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="14b1c-142">硬體不支援虛擬化。</span><span class="sxs-lookup"><span data-stu-id="14b1c-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="14b1c-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951) </span><span class="sxs-lookup"><span data-stu-id="14b1c-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="14b1c-144">硬體虛擬化已停用。</span><span class="sxs-lookup"><span data-stu-id="14b1c-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="14b1c-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952) </span><span class="sxs-lookup"><span data-stu-id="14b1c-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="14b1c-146">Virtual PC 2007 和 Windows Virtual PC 皆已安裝。</span><span class="sxs-lookup"><span data-stu-id="14b1c-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="14b1c-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953) </span><span class="sxs-lookup"><span data-stu-id="14b1c-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="14b1c-148">已安裝其他虛擬化軟體。</span><span class="sxs-lookup"><span data-stu-id="14b1c-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="14b1c-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203) </span><span class="sxs-lookup"><span data-stu-id="14b1c-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="14b1c-150">沒有足夠的主機資源。</span><span class="sxs-lookup"><span data-stu-id="14b1c-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="14b1c-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="14b1c-151">Requirements</span></span>



| <span data-ttu-id="14b1c-152">需求</span><span class="sxs-lookup"><span data-stu-id="14b1c-152">Requirement</span></span> | <span data-ttu-id="14b1c-153">值</span><span class="sxs-lookup"><span data-stu-id="14b1c-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b1c-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14b1c-154">Minimum supported client</span></span><br/> | <span data-ttu-id="14b1c-155">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14b1c-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14b1c-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14b1c-156">Minimum supported server</span></span><br/> | <span data-ttu-id="14b1c-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="14b1c-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="14b1c-158">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="14b1c-158">End of client support</span></span><br/>    | <span data-ttu-id="14b1c-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="14b1c-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="14b1c-160">產品</span><span class="sxs-lookup"><span data-stu-id="14b1c-160">Product</span></span><br/>                  | <span data-ttu-id="14b1c-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="14b1c-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="14b1c-162">標頭</span><span class="sxs-lookup"><span data-stu-id="14b1c-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b1c-163"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="14b1c-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="14b1c-164">IID</span><span class="sxs-lookup"><span data-stu-id="14b1c-164">IID</span></span><br/>                      | <span data-ttu-id="14b1c-165">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="14b1c-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="14b1c-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14b1c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b1c-167">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="14b1c-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

