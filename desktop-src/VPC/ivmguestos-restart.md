---
title: 'IVMGuestOS Restart 方法 (VPCCOMInterfaces .h) '
description: 重新開機客體作業系統。
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- 重新開機方法虛擬電腦
- 重新開機方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，Restart 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384753"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="c376c-106">IVMGuestOS：： Restart 方法</span><span class="sxs-lookup"><span data-stu-id="c376c-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="c376c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="c376c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c376c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="c376c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c376c-109">重新開機客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="c376c-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c376c-110">語法</span><span class="sxs-lookup"><span data-stu-id="c376c-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="c376c-111">參數</span><span class="sxs-lookup"><span data-stu-id="c376c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c376c-112">*inForced* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c376c-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c376c-113">**變異 \_** 如果需要強制重新開機，則為 TRUE，否則為 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c376c-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="c376c-114">*outRestartTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="c376c-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c376c-115">[**IVMTask**](ivmtask.md)物件，用來追蹤重新開機順序的完成進度。</span><span class="sxs-lookup"><span data-stu-id="c376c-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c376c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c376c-116">Return value</span></span>

<span data-ttu-id="c376c-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c376c-117">This method can return one of these values.</span></span>



| <span data-ttu-id="c376c-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c376c-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="c376c-119">Description</span><span class="sxs-lookup"><span data-stu-id="c376c-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c376c-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="c376c-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c376c-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c376c-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="c376c-123">*OutRestartTask* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c376c-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="c376c-124"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="c376c-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c376c-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="c376c-126"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c376c-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="c376c-127">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="c376c-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="c376c-128"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="c376c-129">虛擬機器 (VM) 必須針對此操作執行。</span><span class="sxs-lookup"><span data-stu-id="c376c-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="c376c-130"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="c376c-131">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="c376c-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c376c-132"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="c376c-133">此 VM 中未安裝整合元件功能。</span><span class="sxs-lookup"><span data-stu-id="c376c-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c376c-134">備註</span><span class="sxs-lookup"><span data-stu-id="c376c-134">Remarks</span></span>

<span data-ttu-id="c376c-135">下列值可透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性來傳回。</span><span class="sxs-lookup"><span data-stu-id="c376c-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="c376c-136">[**錯誤碼**](ivmtask-error.md) /值</span><span class="sxs-lookup"><span data-stu-id="c376c-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="c376c-137">Description</span><span class="sxs-lookup"><span data-stu-id="c376c-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c376c-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005) </span><span class="sxs-lookup"><span data-stu-id="c376c-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="c376c-139">呼叫端必須具有此 VM 的「執行」存取權限。</span><span class="sxs-lookup"><span data-stu-id="c376c-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="c376c-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7) </span><span class="sxs-lookup"><span data-stu-id="c376c-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="c376c-141">電腦已鎖定，無法在沒有強制選項的情況下關閉。</span><span class="sxs-lookup"><span data-stu-id="c376c-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="c376c-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015) </span><span class="sxs-lookup"><span data-stu-id="c376c-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="c376c-143">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c376c-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="c376c-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b) </span><span class="sxs-lookup"><span data-stu-id="c376c-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="c376c-145">系統關機正在進行中。</span><span class="sxs-lookup"><span data-stu-id="c376c-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="c376c-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="c376c-146">Requirements</span></span>



| <span data-ttu-id="c376c-147">需求</span><span class="sxs-lookup"><span data-stu-id="c376c-147">Requirement</span></span> | <span data-ttu-id="c376c-148">值</span><span class="sxs-lookup"><span data-stu-id="c376c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c376c-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c376c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c376c-150">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c376c-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c376c-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c376c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c376c-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="c376c-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c376c-153">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c376c-153">End of client support</span></span><br/>    | <span data-ttu-id="c376c-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c376c-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c376c-155">產品</span><span class="sxs-lookup"><span data-stu-id="c376c-155">Product</span></span><br/>                  | <span data-ttu-id="c376c-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c376c-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c376c-157">標頭</span><span class="sxs-lookup"><span data-stu-id="c376c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c376c-158"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="c376c-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c376c-159">IID</span><span class="sxs-lookup"><span data-stu-id="c376c-159">IID</span></span><br/>                      | <span data-ttu-id="c376c-160">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="c376c-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c376c-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c376c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c376c-162">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="c376c-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

