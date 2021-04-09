---
title: 'IVMGuestOS SuiteMask 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中執行的客體作業系統 SuiteMask。
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- SuiteMask 屬性 Virtual PC
- SuiteMask 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，SuiteMask 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686472"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="d53c2-106">IVMGuestOS：： SuiteMask 屬性</span><span class="sxs-lookup"><span data-stu-id="d53c2-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="d53c2-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d53c2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d53c2-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d53c2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d53c2-109">抓取虛擬機器中執行的客體作業系統 SuiteMask。</span><span class="sxs-lookup"><span data-stu-id="d53c2-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="d53c2-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d53c2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d53c2-111">語法</span><span class="sxs-lookup"><span data-stu-id="d53c2-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="d53c2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d53c2-112">Property value</span></span>

<span data-ttu-id="d53c2-113">套件遮罩。</span><span class="sxs-lookup"><span data-stu-id="d53c2-113">The suite mask.</span></span> <span data-ttu-id="d53c2-114">以下是支援的字串值。</span><span class="sxs-lookup"><span data-stu-id="d53c2-114">The following string values are supported.</span></span>



| <span data-ttu-id="d53c2-115">值</span><span class="sxs-lookup"><span data-stu-id="d53c2-115">Value</span></span>                                                                                   | <span data-ttu-id="d53c2-116">意義</span><span class="sxs-lookup"><span data-stu-id="d53c2-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d53c2-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="d53c2-118">已安裝 Microsoft BackOffice 元件。</span><span class="sxs-lookup"><span data-stu-id="d53c2-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="d53c2-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="d53c2-120">已安裝 Windows Server 2003 （Web Edition）。</span><span class="sxs-lookup"><span data-stu-id="d53c2-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="d53c2-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="d53c2-122">已安裝 Windows Server 2003、Compute Cluster Edition。</span><span class="sxs-lookup"><span data-stu-id="d53c2-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="d53c2-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="d53c2-124">已安裝 windows Server 2008 R2 Datacenter、Windows Server 2008 Datacenter、Windows Server 2003、Datacenter Edition 或 Windows 2000 Datacenter Server。</span><span class="sxs-lookup"><span data-stu-id="d53c2-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="d53c2-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="d53c2-126">已安裝 windows Server 2008 R2 Enterprise、Windows Server 2008 Enterprise、Windows Server 2003、Enterprise Edition 或 Windows 2000 Advanced Server。</span><span class="sxs-lookup"><span data-stu-id="d53c2-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="d53c2-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="d53c2-128">已安裝 Windows XP Embedded。</span><span class="sxs-lookup"><span data-stu-id="d53c2-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="d53c2-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="d53c2-130">已安裝 windows Vista Home Premium、Windows Vista Home Basic 或 Windows XP Home Edition。</span><span class="sxs-lookup"><span data-stu-id="d53c2-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d53c2-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="d53c2-132">支援遠端桌面，但只支援一個互動式會話。</span><span class="sxs-lookup"><span data-stu-id="d53c2-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d53c2-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="d53c2-134">Microsoft Small Business Server 已安裝在系統上，但可能已升級至另一個版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="d53c2-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d53c2-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="d53c2-136">Microsoft Small Business Server 會以強制的嚴格用戶端授權安裝。</span><span class="sxs-lookup"><span data-stu-id="d53c2-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="d53c2-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="d53c2-138">已安裝 windows Storage Server 2003 R2 或 Windows Storage Server 2003。</span><span class="sxs-lookup"><span data-stu-id="d53c2-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d53c2-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="d53c2-140">已安裝遠端桌面服務。</span><span class="sxs-lookup"><span data-stu-id="d53c2-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="d53c2-141">一律會設定這個值。</span><span class="sxs-lookup"><span data-stu-id="d53c2-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d53c2-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="d53c2-143">已安裝 Windows Home Server。</span><span class="sxs-lookup"><span data-stu-id="d53c2-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="d53c2-144">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d53c2-144">Error codes</span></span>



| <span data-ttu-id="d53c2-145">名稱/值</span><span class="sxs-lookup"><span data-stu-id="d53c2-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d53c2-146">意義</span><span class="sxs-lookup"><span data-stu-id="d53c2-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d53c2-147"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="d53c2-148">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d53c2-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="d53c2-149"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="d53c2-150">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d53c2-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="d53c2-151"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="d53c2-152">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="d53c2-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d53c2-153"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="d53c2-154">此 VM 中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="d53c2-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d53c2-155"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="d53c2-156">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d53c2-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="d53c2-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="d53c2-157">Requirements</span></span>



| <span data-ttu-id="d53c2-158">需求</span><span class="sxs-lookup"><span data-stu-id="d53c2-158">Requirement</span></span> | <span data-ttu-id="d53c2-159">值</span><span class="sxs-lookup"><span data-stu-id="d53c2-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53c2-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d53c2-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d53c2-161">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d53c2-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d53c2-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d53c2-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d53c2-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="d53c2-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d53c2-164">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d53c2-164">End of client support</span></span><br/>    | <span data-ttu-id="d53c2-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d53c2-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d53c2-166">產品</span><span class="sxs-lookup"><span data-stu-id="d53c2-166">Product</span></span><br/>                  | <span data-ttu-id="d53c2-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d53c2-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d53c2-168">標頭</span><span class="sxs-lookup"><span data-stu-id="d53c2-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="d53c2-169"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d53c2-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d53c2-170">IID</span><span class="sxs-lookup"><span data-stu-id="d53c2-170">IID</span></span><br/>                      | <span data-ttu-id="d53c2-171">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d53c2-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d53c2-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d53c2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53c2-173">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="d53c2-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

