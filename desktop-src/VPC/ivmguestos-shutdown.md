---
title: 'IVMGuestOS Shutdown 方法 (VPCCOMInterfaces .h) '
description: 關閉 VM 中的客體作業系統。
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Shutdown 方法 Virtual PC
- Shutdown 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，Shutdown 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686048"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="43d77-106">IVMGuestOS：： Shutdown 方法</span><span class="sxs-lookup"><span data-stu-id="43d77-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="43d77-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="43d77-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43d77-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="43d77-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43d77-109">將虛擬機器中的客體作業系統 (VM) 關閉。</span><span class="sxs-lookup"><span data-stu-id="43d77-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="43d77-110">語法</span><span class="sxs-lookup"><span data-stu-id="43d77-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="43d77-111">參數</span><span class="sxs-lookup"><span data-stu-id="43d77-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d77-112">*isForced* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43d77-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d77-113">**變異 \_** 如果要強制關機，則為 TRUE，**否則 \_ 為 VARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="43d77-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="43d77-114">*outShutdownTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="43d77-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="43d77-115">用來追蹤關閉程式完成的 [**IVMTask**](ivmtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="43d77-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d77-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="43d77-116">Return value</span></span>

<span data-ttu-id="43d77-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="43d77-117">This method can return one of these values.</span></span>



| <span data-ttu-id="43d77-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="43d77-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="43d77-119">Description</span><span class="sxs-lookup"><span data-stu-id="43d77-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43d77-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="43d77-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="43d77-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="43d77-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="43d77-123">*OutShutdownTask* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="43d77-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="43d77-124"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="43d77-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="43d77-125">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="43d77-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="43d77-126"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="43d77-127">找不到 VM。</span><span class="sxs-lookup"><span data-stu-id="43d77-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="43d77-128"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="43d77-129">此作業必須執行 VM。</span><span class="sxs-lookup"><span data-stu-id="43d77-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="43d77-130"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="43d77-131">呼叫端必須具有此 VM 的「執行」存取權限。</span><span class="sxs-lookup"><span data-stu-id="43d77-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="43d77-132"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="43d77-133">此 VM 中未安裝整合元件功能。</span><span class="sxs-lookup"><span data-stu-id="43d77-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="43d77-134"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="43d77-135">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="43d77-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="43d77-136">備註</span><span class="sxs-lookup"><span data-stu-id="43d77-136">Remarks</span></span>

<span data-ttu-id="43d77-137">當叫用此方法時，VM 必須正在執行，而且必須安裝整合元件功能。</span><span class="sxs-lookup"><span data-stu-id="43d77-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="43d77-138">只有以 Windows 為基礎的客體作業系統支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="43d77-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="43d77-139">下列值可透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性來傳回。</span><span class="sxs-lookup"><span data-stu-id="43d77-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="43d77-140">[**錯誤碼**](ivmtask-error.md) /值</span><span class="sxs-lookup"><span data-stu-id="43d77-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="43d77-141">Description</span><span class="sxs-lookup"><span data-stu-id="43d77-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43d77-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005) </span><span class="sxs-lookup"><span data-stu-id="43d77-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="43d77-143">呼叫端必須具有此 VM 的「執行」存取權限。</span><span class="sxs-lookup"><span data-stu-id="43d77-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="43d77-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7) </span><span class="sxs-lookup"><span data-stu-id="43d77-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="43d77-145">電腦已鎖定，無法在沒有強制選項的情況下關閉。</span><span class="sxs-lookup"><span data-stu-id="43d77-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="43d77-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015) </span><span class="sxs-lookup"><span data-stu-id="43d77-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="43d77-147">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="43d77-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="43d77-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b) </span><span class="sxs-lookup"><span data-stu-id="43d77-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="43d77-149">系統關機正在進行中。</span><span class="sxs-lookup"><span data-stu-id="43d77-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="43d77-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="43d77-150">Requirements</span></span>



| <span data-ttu-id="43d77-151">需求</span><span class="sxs-lookup"><span data-stu-id="43d77-151">Requirement</span></span> | <span data-ttu-id="43d77-152">值</span><span class="sxs-lookup"><span data-stu-id="43d77-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d77-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43d77-153">Minimum supported client</span></span><br/> | <span data-ttu-id="43d77-154">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43d77-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43d77-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43d77-155">Minimum supported server</span></span><br/> | <span data-ttu-id="43d77-156">都不支援</span><span class="sxs-lookup"><span data-stu-id="43d77-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43d77-157">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="43d77-157">End of client support</span></span><br/>    | <span data-ttu-id="43d77-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43d77-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43d77-159">產品</span><span class="sxs-lookup"><span data-stu-id="43d77-159">Product</span></span><br/>                  | <span data-ttu-id="43d77-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43d77-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43d77-161">標頭</span><span class="sxs-lookup"><span data-stu-id="43d77-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d77-162"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="43d77-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="43d77-163">IID</span><span class="sxs-lookup"><span data-stu-id="43d77-163">IID</span></span><br/>                      | <span data-ttu-id="43d77-164">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="43d77-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="43d77-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43d77-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d77-166">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="43d77-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

