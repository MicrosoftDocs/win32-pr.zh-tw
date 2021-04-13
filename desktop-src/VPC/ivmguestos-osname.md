---
title: 'IVMGuestOS OSName 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器中執行的客體作業系統名稱。
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- OSName 屬性 Virtual PC
- OSName 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，OSName 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465200"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="e0b03-106">IVMGuestOS：： OSName 屬性</span><span class="sxs-lookup"><span data-stu-id="e0b03-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="e0b03-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e0b03-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e0b03-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e0b03-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e0b03-109">抓取虛擬機器中執行的客體作業系統 (VM) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0b03-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="e0b03-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e0b03-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b03-111">語法</span><span class="sxs-lookup"><span data-stu-id="e0b03-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="e0b03-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e0b03-112">Property value</span></span>

<span data-ttu-id="e0b03-113">完整名稱 (包括客體作業系統的套件名稱) 。</span><span class="sxs-lookup"><span data-stu-id="e0b03-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0b03-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e0b03-114">Error codes</span></span>



| <span data-ttu-id="e0b03-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="e0b03-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="e0b03-116">意義</span><span class="sxs-lookup"><span data-stu-id="e0b03-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e0b03-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="e0b03-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e0b03-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="e0b03-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="e0b03-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e0b03-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="e0b03-121"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="e0b03-122">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="e0b03-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="e0b03-123"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="e0b03-124">此 VM 中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="e0b03-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="e0b03-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="e0b03-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e0b03-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="e0b03-127">備註</span><span class="sxs-lookup"><span data-stu-id="e0b03-127">Remarks</span></span>

<span data-ttu-id="e0b03-128">VM 必須執行 (也就是，完全開機且未關閉) 而且在叫用此方法時，必須安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="e0b03-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b03-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0b03-129">Requirements</span></span>



| <span data-ttu-id="e0b03-130">需求</span><span class="sxs-lookup"><span data-stu-id="e0b03-130">Requirement</span></span> | <span data-ttu-id="e0b03-131">值</span><span class="sxs-lookup"><span data-stu-id="e0b03-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b03-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0b03-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b03-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0b03-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0b03-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0b03-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b03-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="e0b03-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e0b03-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e0b03-136">End of client support</span></span><br/>    | <span data-ttu-id="e0b03-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0b03-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e0b03-138">產品</span><span class="sxs-lookup"><span data-stu-id="e0b03-138">Product</span></span><br/>                  | <span data-ttu-id="e0b03-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e0b03-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e0b03-140">標頭</span><span class="sxs-lookup"><span data-stu-id="e0b03-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0b03-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b03-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e0b03-142">IID</span><span class="sxs-lookup"><span data-stu-id="e0b03-142">IID</span></span><br/>                      | <span data-ttu-id="e0b03-143">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="e0b03-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e0b03-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0b03-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b03-145">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="e0b03-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

