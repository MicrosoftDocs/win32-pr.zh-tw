---
title: 'IVMGuestOS OSMajorVersion 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器中執行之客體作業系統的主要版本。
ms.assetid: c9be8b4e-15fe-402d-8396-30be6b065b73
keywords:
- OSMajorVersion 屬性 Virtual PC
- OSMajorVersion 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，OSMajorVersion 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMajorVersion
- IVMGuestOS.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f76e3105c4917141c8a5304082d55f383ee947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465201"
---
# <a name="ivmguestososmajorversion-property"></a><span data-ttu-id="15695-106">IVMGuestOS：： OSMajorVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="15695-106">IVMGuestOS::OSMajorVersion property</span></span>

<span data-ttu-id="15695-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="15695-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="15695-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="15695-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="15695-109">抓取虛擬機器中執行之客體作業系統的主要版本。</span><span class="sxs-lookup"><span data-stu-id="15695-109">Retrieves the major version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="15695-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="15695-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="15695-111">語法</span><span class="sxs-lookup"><span data-stu-id="15695-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] BSTR *majorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="15695-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="15695-112">Property value</span></span>

<span data-ttu-id="15695-113">主要版本。</span><span class="sxs-lookup"><span data-stu-id="15695-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="15695-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="15695-114">Error codes</span></span>



| <span data-ttu-id="15695-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="15695-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="15695-116">意義</span><span class="sxs-lookup"><span data-stu-id="15695-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="15695-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="15695-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="15695-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="15695-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="15695-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="15695-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="15695-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15695-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="15695-121"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="15695-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="15695-122">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="15695-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="15695-123"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="15695-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="15695-124">此 VM 中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="15695-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="15695-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="15695-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="15695-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="15695-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="15695-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="15695-127">Requirements</span></span>



| <span data-ttu-id="15695-128">需求</span><span class="sxs-lookup"><span data-stu-id="15695-128">Requirement</span></span> | <span data-ttu-id="15695-129">值</span><span class="sxs-lookup"><span data-stu-id="15695-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15695-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15695-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15695-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15695-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15695-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15695-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15695-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="15695-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="15695-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="15695-134">End of client support</span></span><br/>    | <span data-ttu-id="15695-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15695-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="15695-136">產品</span><span class="sxs-lookup"><span data-stu-id="15695-136">Product</span></span><br/>                  | <span data-ttu-id="15695-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="15695-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="15695-138">標頭</span><span class="sxs-lookup"><span data-stu-id="15695-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="15695-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="15695-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="15695-140">IID</span><span class="sxs-lookup"><span data-stu-id="15695-140">IID</span></span><br/>                      | <span data-ttu-id="15695-141">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="15695-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="15695-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15695-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15695-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="15695-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

