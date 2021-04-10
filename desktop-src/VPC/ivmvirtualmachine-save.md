---
title: 'IVMVirtualMachine Save 方法 (VPCCOMInterfaces .h) '
description: 將虛擬機器 (VM) 狀態。
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- 儲存方法 Virtual PC
- 儲存方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，Save 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686253"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="fd311-106">IVMVirtualMachine：： Save 方法</span><span class="sxs-lookup"><span data-stu-id="fd311-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="fd311-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fd311-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd311-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fd311-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd311-109">將虛擬機器 (VM) 狀態。</span><span class="sxs-lookup"><span data-stu-id="fd311-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd311-110">語法</span><span class="sxs-lookup"><span data-stu-id="fd311-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="fd311-111">參數</span><span class="sxs-lookup"><span data-stu-id="fd311-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd311-112">*saveTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="fd311-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fd311-113">[**IVMTask**](ivmtask.md)物件，可用來追蹤 VM 狀態儲存順序的完成進度。</span><span class="sxs-lookup"><span data-stu-id="fd311-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd311-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd311-114">Return value</span></span>

<span data-ttu-id="fd311-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fd311-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fd311-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="fd311-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="fd311-117">Description</span><span class="sxs-lookup"><span data-stu-id="fd311-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd311-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="fd311-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="fd311-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="fd311-120"><dt>**E \_FAIL**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="fd311-121">因為復原磁片已標示為要刪除，所以無法儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="fd311-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="fd311-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="fd311-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fd311-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="fd311-124"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="fd311-125">呼叫端必須具有執行存取權限，才能儲存此 VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="fd311-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="fd311-126"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="fd311-127">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="fd311-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="fd311-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="fd311-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fd311-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="fd311-130">備註</span><span class="sxs-lookup"><span data-stu-id="fd311-130">Remarks</span></span>

<span data-ttu-id="fd311-131">當 **儲存** 工作達到完成時，VM 會關閉。</span><span class="sxs-lookup"><span data-stu-id="fd311-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="fd311-132">[**IVMVirtualMachine：： State**](ivmvirtualmachine-state.md)屬性會在儲存進行中時包含 **vmVMState \_ 儲存**，接著在儲存完成並關閉 VM 時 **\_ 儲存 vmVMState** 。</span><span class="sxs-lookup"><span data-stu-id="fd311-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd311-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd311-133">Requirements</span></span>



| <span data-ttu-id="fd311-134">需求</span><span class="sxs-lookup"><span data-stu-id="fd311-134">Requirement</span></span> | <span data-ttu-id="fd311-135">值</span><span class="sxs-lookup"><span data-stu-id="fd311-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd311-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd311-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fd311-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd311-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd311-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd311-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fd311-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd311-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd311-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fd311-140">End of client support</span></span><br/>    | <span data-ttu-id="fd311-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd311-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd311-142">產品</span><span class="sxs-lookup"><span data-stu-id="fd311-142">Product</span></span><br/>                  | <span data-ttu-id="fd311-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd311-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd311-144">標頭</span><span class="sxs-lookup"><span data-stu-id="fd311-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd311-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd311-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd311-146">IID</span><span class="sxs-lookup"><span data-stu-id="fd311-146">IID</span></span><br/>                      | <span data-ttu-id="fd311-147">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="fd311-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fd311-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd311-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd311-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fd311-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

