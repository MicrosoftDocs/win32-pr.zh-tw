---
title: 'IVMGuestOS TerminalServicesInitialized 屬性 (VPCCOMInterfaces .h) '
description: 客體作業系統中遠端桌面服務的狀態。
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- TerminalServicesInitialized 屬性 Virtual PC
- TerminalServicesInitialized 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，TerminalServicesInitialized 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509335"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="8c19b-106">IVMGuestOS：： TerminalServicesInitialized 屬性</span><span class="sxs-lookup"><span data-stu-id="8c19b-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="8c19b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8c19b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c19b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8c19b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c19b-109">抓取客體作業系統中先前稱為終端機服務) 的遠端桌面服務 (狀態。</span><span class="sxs-lookup"><span data-stu-id="8c19b-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="8c19b-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8c19b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c19b-111">語法</span><span class="sxs-lookup"><span data-stu-id="8c19b-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="8c19b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="8c19b-112">Property value</span></span>

<span data-ttu-id="8c19b-113">初始化狀態。</span><span class="sxs-lookup"><span data-stu-id="8c19b-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8c19b-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8c19b-114">Error codes</span></span>



| <span data-ttu-id="8c19b-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="8c19b-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="8c19b-116">意義</span><span class="sxs-lookup"><span data-stu-id="8c19b-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c19b-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="8c19b-118">作業成功且遠端桌面服務已初始化。</span><span class="sxs-lookup"><span data-stu-id="8c19b-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="8c19b-119">傳回的屬性值會指出是否可在客體作業系統中使用遠端桌面服務。</span><span class="sxs-lookup"><span data-stu-id="8c19b-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="8c19b-120"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="8c19b-121">整合元件功能正在執行，但遠端桌面服務尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="8c19b-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8c19b-122"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="8c19b-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8c19b-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="8c19b-124"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="8c19b-125">虛擬機器 (VM) 必須針對此操作執行。</span><span class="sxs-lookup"><span data-stu-id="8c19b-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="8c19b-126"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="8c19b-127">「整合元件」功能未在客體作業系統中執行。</span><span class="sxs-lookup"><span data-stu-id="8c19b-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="8c19b-128"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="8c19b-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c19b-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="8c19b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c19b-130">Requirements</span></span>



| <span data-ttu-id="8c19b-131">需求</span><span class="sxs-lookup"><span data-stu-id="8c19b-131">Requirement</span></span> | <span data-ttu-id="8c19b-132">值</span><span class="sxs-lookup"><span data-stu-id="8c19b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c19b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c19b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8c19b-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c19b-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c19b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c19b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8c19b-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="8c19b-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c19b-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8c19b-137">End of client support</span></span><br/>    | <span data-ttu-id="8c19b-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c19b-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c19b-139">產品</span><span class="sxs-lookup"><span data-stu-id="8c19b-139">Product</span></span><br/>                  | <span data-ttu-id="8c19b-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c19b-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c19b-141">標頭</span><span class="sxs-lookup"><span data-stu-id="8c19b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c19b-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c19b-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8c19b-143">IID</span><span class="sxs-lookup"><span data-stu-id="8c19b-143">IID</span></span><br/>                      | <span data-ttu-id="8c19b-144">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8c19b-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8c19b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c19b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c19b-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8c19b-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

