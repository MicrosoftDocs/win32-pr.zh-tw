---
title: 'IVMVirtualMachine MergeUndoDisks 方法 (VPCCOMInterfaces .h) '
description: 合併虛擬復原磁片。
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- MergeUndoDisks 方法 Virtual PC
- MergeUndoDisks 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，MergeUndoDisks 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317403"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="aef6f-106">IVMVirtualMachine：： MergeUndoDisks 方法</span><span class="sxs-lookup"><span data-stu-id="aef6f-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="aef6f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="aef6f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aef6f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="aef6f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aef6f-109">合併虛擬復原磁片。</span><span class="sxs-lookup"><span data-stu-id="aef6f-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef6f-110">語法</span><span class="sxs-lookup"><span data-stu-id="aef6f-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="aef6f-111">參數</span><span class="sxs-lookup"><span data-stu-id="aef6f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef6f-112">*undoMergeTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="aef6f-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="aef6f-113">用來追蹤影像建立的 [**IVMTask**](ivmtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="aef6f-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef6f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="aef6f-114">Return value</span></span>

<span data-ttu-id="aef6f-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="aef6f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="aef6f-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="aef6f-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="aef6f-117">Description</span><span class="sxs-lookup"><span data-stu-id="aef6f-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aef6f-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="aef6f-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="aef6f-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="aef6f-120"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="aef6f-121">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aef6f-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="aef6f-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="aef6f-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="aef6f-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="aef6f-124"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="aef6f-125">系統找不到 *convertedDiskImagePath* 參數所指定的路徑，或其中一個父磁片無效。</span><span class="sxs-lookup"><span data-stu-id="aef6f-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="aef6f-126"><dt>**E \_ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="aef6f-127">目前的使用者沒有足夠的父系檔案存取權。</span><span class="sxs-lookup"><span data-stu-id="aef6f-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="aef6f-128"><dt>**E \_處理**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="aef6f-129">其中一個父磁片正在使用中。</span><span class="sxs-lookup"><span data-stu-id="aef6f-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="aef6f-130"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="aef6f-131">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="aef6f-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="aef6f-132"><dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="aef6f-133">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="aef6f-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="aef6f-134"><dt>**VM \_E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="aef6f-135">虛擬復原磁片的父系會標示為唯讀。</span><span class="sxs-lookup"><span data-stu-id="aef6f-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="aef6f-136"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="aef6f-137">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aef6f-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="aef6f-138">備註</span><span class="sxs-lookup"><span data-stu-id="aef6f-138">Remarks</span></span>

<span data-ttu-id="aef6f-139">當虛擬機器仍在執行時，無法呼叫 **MergeUndoDisks** 。</span><span class="sxs-lookup"><span data-stu-id="aef6f-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="aef6f-140">使用 [**IVMVirtualMachine：： save**](ivmvirtualmachine-save.md) 可先儲存虛擬機器的狀態，然後再呼叫 **MergeUndoDisks**，或 [**IVMVirtualMachine：： TurnOff**](ivmvirtualmachine-turnoff.md) 以關閉虛擬機器，而不需事先儲存其目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="aef6f-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef6f-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="aef6f-141">Requirements</span></span>



| <span data-ttu-id="aef6f-142">需求</span><span class="sxs-lookup"><span data-stu-id="aef6f-142">Requirement</span></span> | <span data-ttu-id="aef6f-143">值</span><span class="sxs-lookup"><span data-stu-id="aef6f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef6f-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aef6f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="aef6f-145">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aef6f-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aef6f-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aef6f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="aef6f-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="aef6f-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aef6f-148">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="aef6f-148">End of client support</span></span><br/>    | <span data-ttu-id="aef6f-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aef6f-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aef6f-150">產品</span><span class="sxs-lookup"><span data-stu-id="aef6f-150">Product</span></span><br/>                  | <span data-ttu-id="aef6f-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aef6f-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aef6f-152">標頭</span><span class="sxs-lookup"><span data-stu-id="aef6f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="aef6f-153"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="aef6f-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aef6f-154">IID</span><span class="sxs-lookup"><span data-stu-id="aef6f-154">IID</span></span><br/>                      | <span data-ttu-id="aef6f-155">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="aef6f-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="aef6f-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aef6f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef6f-157">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="aef6f-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

