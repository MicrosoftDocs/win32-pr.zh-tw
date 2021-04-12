---
title: 'IVMGuestOS SetParameter 方法 (VPCCOMInterfaces .h) '
description: 設定客體作業系統內的具名引數。
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- SetParameter 方法 Virtual PC
- SetParameter 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，SetParameter 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508655"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="8b25a-106">IVMGuestOS：： SetParameter 方法</span><span class="sxs-lookup"><span data-stu-id="8b25a-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="8b25a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8b25a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8b25a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8b25a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8b25a-109">設定客體作業系統內的具名引數。</span><span class="sxs-lookup"><span data-stu-id="8b25a-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b25a-110">語法</span><span class="sxs-lookup"><span data-stu-id="8b25a-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="8b25a-111">參數</span><span class="sxs-lookup"><span data-stu-id="8b25a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b25a-112">*inParameterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b25a-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b25a-113">參數名稱。</span><span class="sxs-lookup"><span data-stu-id="8b25a-113">The parameter name.</span></span> <span data-ttu-id="8b25a-114">長度必須介於1到255個字元之間，且不能包含反斜線 (\) 字元。</span><span class="sxs-lookup"><span data-stu-id="8b25a-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="8b25a-115">*inParameterValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b25a-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b25a-116">參數值。</span><span class="sxs-lookup"><span data-stu-id="8b25a-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b25a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b25a-117">Return value</span></span>

<span data-ttu-id="8b25a-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8b25a-118">This method can return one of these values.</span></span>



| <span data-ttu-id="8b25a-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="8b25a-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="8b25a-120">Description</span><span class="sxs-lookup"><span data-stu-id="8b25a-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8b25a-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8b25a-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="8b25a-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="8b25a-123"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="8b25a-124">參數無效或未指定。</span><span class="sxs-lookup"><span data-stu-id="8b25a-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="8b25a-125"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="8b25a-126">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="8b25a-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="8b25a-127"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8b25a-128">虛擬機器 (VM) 未執行。</span><span class="sxs-lookup"><span data-stu-id="8b25a-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="8b25a-129"><dt>**VM \_E \_ VM 已 \_ 暫停**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="8b25a-130">VM 已暫停。</span><span class="sxs-lookup"><span data-stu-id="8b25a-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8b25a-131"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8b25a-132">此 VM 中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="8b25a-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="8b25a-133"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8b25a-134">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8b25a-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8b25a-135">備註</span><span class="sxs-lookup"><span data-stu-id="8b25a-135">Remarks</span></span>

<span data-ttu-id="8b25a-136">虛擬機器必須正在執行，而且必須在叫用此方法時安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="8b25a-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="8b25a-137">只有以 Windows 為基礎的客體作業系統支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="8b25a-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="8b25a-138">安裝整合元件後，系統會自動將下列金鑰新增至客體作業系統的登錄：</span><span class="sxs-lookup"><span data-stu-id="8b25a-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="8b25a-139">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 虛擬機器 \\ 來賓 \\ 參數**</span><span class="sxs-lookup"><span data-stu-id="8b25a-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="8b25a-140">當客體作業系統啟動時，會在 **參數** 索引鍵中填入下列登錄字串值：</span><span class="sxs-lookup"><span data-stu-id="8b25a-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="8b25a-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="8b25a-141">**HostName**</span></span>
-   <span data-ttu-id="8b25a-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="8b25a-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="8b25a-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="8b25a-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="8b25a-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="8b25a-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="8b25a-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b25a-145">Requirements</span></span>



| <span data-ttu-id="8b25a-146">需求</span><span class="sxs-lookup"><span data-stu-id="8b25a-146">Requirement</span></span> | <span data-ttu-id="8b25a-147">值</span><span class="sxs-lookup"><span data-stu-id="8b25a-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b25a-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b25a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8b25a-149">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b25a-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b25a-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b25a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8b25a-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="8b25a-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8b25a-152">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8b25a-152">End of client support</span></span><br/>    | <span data-ttu-id="8b25a-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b25a-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8b25a-154">產品</span><span class="sxs-lookup"><span data-stu-id="8b25a-154">Product</span></span><br/>                  | <span data-ttu-id="8b25a-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8b25a-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8b25a-156">標頭</span><span class="sxs-lookup"><span data-stu-id="8b25a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b25a-157"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b25a-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8b25a-158">IID</span><span class="sxs-lookup"><span data-stu-id="8b25a-158">IID</span></span><br/>                      | <span data-ttu-id="8b25a-159">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8b25a-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8b25a-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b25a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b25a-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8b25a-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

