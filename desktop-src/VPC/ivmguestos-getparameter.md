---
title: 'IVMGuestOS GetParameter 方法 (VPCCOMInterfaces .h) '
description: 抓取客體作業系統內的具名引數。
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter 方法 Virtual PC
- GetParameter 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，GetParameter 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509255"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="b85bc-106">IVMGuestOS：： GetParameter 方法</span><span class="sxs-lookup"><span data-stu-id="b85bc-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="b85bc-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b85bc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b85bc-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b85bc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b85bc-109">抓取客體作業系統內的具名引數。</span><span class="sxs-lookup"><span data-stu-id="b85bc-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b85bc-110">語法</span><span class="sxs-lookup"><span data-stu-id="b85bc-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="b85bc-111">參數</span><span class="sxs-lookup"><span data-stu-id="b85bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b85bc-112">*inParameterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b85bc-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b85bc-113">參數名稱。</span><span class="sxs-lookup"><span data-stu-id="b85bc-113">The parameter name.</span></span> <span data-ttu-id="b85bc-114">長度必須介於1到255個字元之間，且不能包含反斜線 (\) 字元。</span><span class="sxs-lookup"><span data-stu-id="b85bc-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="b85bc-115">*outParameterValue* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="b85bc-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b85bc-116">參數值。</span><span class="sxs-lookup"><span data-stu-id="b85bc-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b85bc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b85bc-117">Return value</span></span>

<span data-ttu-id="b85bc-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b85bc-118">This method can return one of these values.</span></span>



| <span data-ttu-id="b85bc-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b85bc-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="b85bc-120">Description</span><span class="sxs-lookup"><span data-stu-id="b85bc-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b85bc-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="b85bc-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b85bc-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b85bc-123"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="b85bc-124">參數無效或未指定。</span><span class="sxs-lookup"><span data-stu-id="b85bc-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="b85bc-125"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="b85bc-126">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b85bc-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b85bc-127"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="b85bc-128">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="b85bc-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="b85bc-129"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="b85bc-130">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="b85bc-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="b85bc-131"><dt>**VM \_E \_ VM 已 \_ 暫停**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="b85bc-132">虛擬機器已暫停。</span><span class="sxs-lookup"><span data-stu-id="b85bc-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b85bc-133"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="b85bc-134">此虛擬機器中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="b85bc-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="b85bc-135"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="b85bc-136">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b85bc-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="b85bc-137">備註</span><span class="sxs-lookup"><span data-stu-id="b85bc-137">Remarks</span></span>

<span data-ttu-id="b85bc-138">虛擬機器必須在執行中，而且當叫用此方法時，必須安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="b85bc-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="b85bc-139">只有以 Windows 為基礎的客體作業系統支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b85bc-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="b85bc-140">安裝整合元件後，系統會自動將下列金鑰新增至客體作業系統的登錄：</span><span class="sxs-lookup"><span data-stu-id="b85bc-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="b85bc-141">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 虛擬機器 \\ 來賓 \\ 參數**</span><span class="sxs-lookup"><span data-stu-id="b85bc-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="b85bc-142">當客體作業系統啟動時，會在 **參數** 索引鍵中填入下列登錄字串值：</span><span class="sxs-lookup"><span data-stu-id="b85bc-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="b85bc-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="b85bc-143">**HostName**</span></span>
-   <span data-ttu-id="b85bc-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="b85bc-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="b85bc-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="b85bc-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="b85bc-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="b85bc-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="b85bc-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="b85bc-147">Requirements</span></span>



| <span data-ttu-id="b85bc-148">需求</span><span class="sxs-lookup"><span data-stu-id="b85bc-148">Requirement</span></span> | <span data-ttu-id="b85bc-149">值</span><span class="sxs-lookup"><span data-stu-id="b85bc-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b85bc-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b85bc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b85bc-151">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b85bc-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b85bc-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b85bc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b85bc-153">都不支援</span><span class="sxs-lookup"><span data-stu-id="b85bc-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b85bc-154">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b85bc-154">End of client support</span></span><br/>    | <span data-ttu-id="b85bc-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b85bc-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b85bc-156">產品</span><span class="sxs-lookup"><span data-stu-id="b85bc-156">Product</span></span><br/>                  | <span data-ttu-id="b85bc-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b85bc-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b85bc-158">標頭</span><span class="sxs-lookup"><span data-stu-id="b85bc-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="b85bc-159"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b85bc-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b85bc-160">IID</span><span class="sxs-lookup"><span data-stu-id="b85bc-160">IID</span></span><br/>                      | <span data-ttu-id="b85bc-161">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="b85bc-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b85bc-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b85bc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b85bc-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="b85bc-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

