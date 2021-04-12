---
title: 'IVMGuestOS 登出方法 (VPCCOMInterfaces .h) '
description: 登出客體作業系統中的所有使用者。
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- 登出方法虛擬電腦
- 登出方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，登出方法
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025455"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="7846a-106">IVMGuestOS：：登出方法</span><span class="sxs-lookup"><span data-stu-id="7846a-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="7846a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7846a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7846a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7846a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7846a-109">登出客體作業系統中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="7846a-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7846a-110">語法</span><span class="sxs-lookup"><span data-stu-id="7846a-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="7846a-111">參數</span><span class="sxs-lookup"><span data-stu-id="7846a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7846a-112">*outLogoffTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="7846a-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7846a-113">[**IVMTask**](ivmtask.md)物件，用來追蹤登出順序的完成進度。</span><span class="sxs-lookup"><span data-stu-id="7846a-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7846a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7846a-114">Return value</span></span>

<span data-ttu-id="7846a-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7846a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="7846a-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7846a-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="7846a-117">Description</span><span class="sxs-lookup"><span data-stu-id="7846a-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7846a-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="7846a-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="7846a-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="7846a-120"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="7846a-121">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7846a-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="7846a-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="7846a-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7846a-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="7846a-124"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="7846a-125">呼叫端必須具有此 VM 的「執行」存取權限。</span><span class="sxs-lookup"><span data-stu-id="7846a-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="7846a-126"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7846a-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="7846a-127">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="7846a-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="7846a-128"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="7846a-129">此虛擬機器未安裝整合元件功能。</span><span class="sxs-lookup"><span data-stu-id="7846a-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="7846a-130"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="7846a-131">虛擬機器 (VM) 必須針對此操作執行。</span><span class="sxs-lookup"><span data-stu-id="7846a-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="7846a-132"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="7846a-133">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="7846a-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="7846a-134">備註</span><span class="sxs-lookup"><span data-stu-id="7846a-134">Remarks</span></span>

<span data-ttu-id="7846a-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (的 0x80070520) 會透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性傳回，而客體作業系統中沒有任何登入會話。</span><span class="sxs-lookup"><span data-stu-id="7846a-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="7846a-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="7846a-136">Requirements</span></span>



| <span data-ttu-id="7846a-137">需求</span><span class="sxs-lookup"><span data-stu-id="7846a-137">Requirement</span></span> | <span data-ttu-id="7846a-138">值</span><span class="sxs-lookup"><span data-stu-id="7846a-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7846a-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7846a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7846a-140">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7846a-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7846a-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7846a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7846a-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="7846a-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7846a-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7846a-143">End of client support</span></span><br/>    | <span data-ttu-id="7846a-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7846a-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7846a-145">產品</span><span class="sxs-lookup"><span data-stu-id="7846a-145">Product</span></span><br/>                  | <span data-ttu-id="7846a-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7846a-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7846a-147">標頭</span><span class="sxs-lookup"><span data-stu-id="7846a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7846a-148"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7846a-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7846a-149">IID</span><span class="sxs-lookup"><span data-stu-id="7846a-149">IID</span></span><br/>                      | <span data-ttu-id="7846a-150">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="7846a-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7846a-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7846a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7846a-152">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="7846a-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

