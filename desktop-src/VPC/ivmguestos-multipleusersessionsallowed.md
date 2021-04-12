---
title: IVMGuestOS MultipleUserSessionsAllowed 屬性
description: 判斷客體作業系統中是否允許多個並行使用者會話。
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed 屬性 Virtual PC
- MultipleUserSessionsAllowed 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，MultipleUserSessionsAllowed 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103968"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="896be-106">IVMGuestOS：： MultipleUserSessionsAllowed 屬性</span><span class="sxs-lookup"><span data-stu-id="896be-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="896be-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="896be-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="896be-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="896be-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="896be-109">判斷客體作業系統中是否允許多個並行使用者會話。</span><span class="sxs-lookup"><span data-stu-id="896be-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="896be-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="896be-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="896be-111">語法</span><span class="sxs-lookup"><span data-stu-id="896be-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="896be-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="896be-112">Property value</span></span>

<span data-ttu-id="896be-113">**變異 \_** 如果客體作業系統允許多個並行使用者會話，則為 TRUE，**否則 \_ 為 VARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="896be-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="896be-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="896be-114">Error codes</span></span>



| <span data-ttu-id="896be-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="896be-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="896be-116">意義</span><span class="sxs-lookup"><span data-stu-id="896be-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="896be-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="896be-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="896be-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="896be-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="896be-119"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="896be-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="896be-120">先前稱為終端機服務) 的遠端桌面服務 (尚未在客體作業系統中初始化。</span><span class="sxs-lookup"><span data-stu-id="896be-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="896be-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="896be-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="896be-122">*SessionStatus* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="896be-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="896be-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="896be-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="896be-124">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="896be-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="896be-125"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="896be-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="896be-126">此虛擬機器中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="896be-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="896be-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="896be-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="896be-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="896be-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="896be-129">備註</span><span class="sxs-lookup"><span data-stu-id="896be-129">Remarks</span></span>

<span data-ttu-id="896be-130">除非 [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) 屬性為 **VARIANT \_ TRUE**，否則這個屬性的值無效。</span><span class="sxs-lookup"><span data-stu-id="896be-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="896be-131">針對 Windows 用戶端作業系統，如果支援快速使用者切換，則 **MultipleUserSessionsAllowed** 是 **變異 \_** 。</span><span class="sxs-lookup"><span data-stu-id="896be-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="896be-132">若是 Windows Server 作業系統，如果已安裝並啟用遠端桌面服務 (之前稱為「終端機) 服務」，則 **MultipleUserSessionsAllowed** 是 **VARIANT \_** 。</span><span class="sxs-lookup"><span data-stu-id="896be-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="896be-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="896be-133">Requirements</span></span>



| <span data-ttu-id="896be-134">需求</span><span class="sxs-lookup"><span data-stu-id="896be-134">Requirement</span></span> | <span data-ttu-id="896be-135">值</span><span class="sxs-lookup"><span data-stu-id="896be-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="896be-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="896be-136">Minimum supported client</span></span><br/> | <span data-ttu-id="896be-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="896be-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="896be-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="896be-138">Minimum supported server</span></span><br/> | <span data-ttu-id="896be-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="896be-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="896be-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="896be-140">End of client support</span></span><br/>    | <span data-ttu-id="896be-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="896be-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="896be-142">Idl</span><span class="sxs-lookup"><span data-stu-id="896be-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="896be-143"><dt>IVMGuestOS .idl</dt></span><span class="sxs-lookup"><span data-stu-id="896be-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="896be-144">IID</span><span class="sxs-lookup"><span data-stu-id="896be-144">IID</span></span><br/>                      | <span data-ttu-id="896be-145">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="896be-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="896be-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="896be-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896be-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="896be-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

