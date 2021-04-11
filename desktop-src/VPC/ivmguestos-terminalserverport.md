---
title: IVMGuestOS TerminalServerPort 屬性
description: 客體作業系統中遠端桌面服務所使用的埠。
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort 屬性 Virtual PC
- TerminalServerPort 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，TerminalServerPort 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105816"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="be7a8-106">IVMGuestOS：： TerminalServerPort 屬性</span><span class="sxs-lookup"><span data-stu-id="be7a8-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="be7a8-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="be7a8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="be7a8-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="be7a8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="be7a8-109">遠端桌面服務的埠 (之前稱為「終端機服務」，可在客體作業系統中) 。</span><span class="sxs-lookup"><span data-stu-id="be7a8-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="be7a8-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="be7a8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7a8-111">語法</span><span class="sxs-lookup"><span data-stu-id="be7a8-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="be7a8-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="be7a8-112">Property value</span></span>

<span data-ttu-id="be7a8-113">傳回客體作業系統中遠端桌面服務所使用的埠。</span><span class="sxs-lookup"><span data-stu-id="be7a8-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="be7a8-114">值</span><span class="sxs-lookup"><span data-stu-id="be7a8-114">Value</span></span>                                                                              | <span data-ttu-id="be7a8-115">意義</span><span class="sxs-lookup"><span data-stu-id="be7a8-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="be7a8-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="be7a8-117">預設值</span><span class="sxs-lookup"><span data-stu-id="be7a8-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="be7a8-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="be7a8-119">有效範圍</span><span class="sxs-lookup"><span data-stu-id="be7a8-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="be7a8-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="be7a8-121">無法使用有效的埠值。</span><span class="sxs-lookup"><span data-stu-id="be7a8-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="be7a8-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="be7a8-122">Error codes</span></span>



| <span data-ttu-id="be7a8-123">名稱/值</span><span class="sxs-lookup"><span data-stu-id="be7a8-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="be7a8-124">意義</span><span class="sxs-lookup"><span data-stu-id="be7a8-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be7a8-125"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="be7a8-126">作業成功。</span><span class="sxs-lookup"><span data-stu-id="be7a8-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="be7a8-127"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="be7a8-128">遠端桌面服務尚未在客體作業系統中初始化。</span><span class="sxs-lookup"><span data-stu-id="be7a8-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="be7a8-129"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="be7a8-130">*TsPort* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="be7a8-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="be7a8-131"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="be7a8-132">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="be7a8-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="be7a8-133"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="be7a8-134">此虛擬機器中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="be7a8-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="be7a8-135"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="be7a8-136">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="be7a8-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="be7a8-137">備註</span><span class="sxs-lookup"><span data-stu-id="be7a8-137">Remarks</span></span>

<span data-ttu-id="be7a8-138">除非 [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) 屬性為 **VARIANT \_ TRUE**，否則這個屬性的值無效。</span><span class="sxs-lookup"><span data-stu-id="be7a8-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="be7a8-139">如果 [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) 屬性由於埠上的連接錯誤而成為 **VARIANT \_ FALSE** ，則 **TerminalServerPort** 屬性所傳回的值會包含錯誤值。</span><span class="sxs-lookup"><span data-stu-id="be7a8-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7a8-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="be7a8-140">Requirements</span></span>



| <span data-ttu-id="be7a8-141">需求</span><span class="sxs-lookup"><span data-stu-id="be7a8-141">Requirement</span></span> | <span data-ttu-id="be7a8-142">值</span><span class="sxs-lookup"><span data-stu-id="be7a8-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7a8-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be7a8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="be7a8-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be7a8-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be7a8-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be7a8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="be7a8-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="be7a8-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="be7a8-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="be7a8-147">End of client support</span></span><br/>    | <span data-ttu-id="be7a8-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="be7a8-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="be7a8-149">Idl</span><span class="sxs-lookup"><span data-stu-id="be7a8-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be7a8-150"><dt>IVMGuestOS .idl</dt></span><span class="sxs-lookup"><span data-stu-id="be7a8-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="be7a8-151">IID</span><span class="sxs-lookup"><span data-stu-id="be7a8-151">IID</span></span><br/>                      | <span data-ttu-id="be7a8-152">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="be7a8-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="be7a8-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be7a8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7a8-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="be7a8-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

