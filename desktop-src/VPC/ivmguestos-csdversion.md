---
title: 'IVMGuestOS CSDVersion 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器中執行的客體作業系統 CSDVersion。
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- CSDVersion 屬性 Virtual PC
- CSDVersion 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，CSDVersion 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d82b3939f581edf328902f7fd0a26e1916abe1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935032"
---
# <a name="ivmguestoscsdversion-property"></a><span data-ttu-id="a0829-106">IVMGuestOS：： CSDVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="a0829-106">IVMGuestOS::CSDVersion property</span></span>

<span data-ttu-id="a0829-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="a0829-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a0829-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="a0829-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a0829-109">抓取虛擬機器中執行的客體作業系統 CSDVersion。</span><span class="sxs-lookup"><span data-stu-id="a0829-109">Retrieves the CSDVersion of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="a0829-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a0829-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0829-111">語法</span><span class="sxs-lookup"><span data-stu-id="a0829-111">Syntax</span></span>


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a><span data-ttu-id="a0829-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="a0829-112">Property value</span></span>

<span data-ttu-id="a0829-113">以 null 終止的字串，例如 "Service Pack 3"，表示系統上安裝的最新 Service Pack。</span><span class="sxs-lookup"><span data-stu-id="a0829-113">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="a0829-114">如果未安裝 Service Pack，則字串是空的。</span><span class="sxs-lookup"><span data-stu-id="a0829-114">If no Service Pack has been installed, the string is empty.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0829-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a0829-115">Error codes</span></span>



| <span data-ttu-id="a0829-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="a0829-116">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a0829-117">意義</span><span class="sxs-lookup"><span data-stu-id="a0829-117">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a0829-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a0829-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="a0829-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="a0829-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="a0829-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a0829-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="a0829-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a0829-121">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="a0829-122"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="a0829-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="a0829-123">VM 未執行。</span><span class="sxs-lookup"><span data-stu-id="a0829-123">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="a0829-124"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="a0829-124"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="a0829-125">此 VM 中未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="a0829-125">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="a0829-126"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a0829-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="a0829-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0829-127">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="a0829-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0829-128">Requirements</span></span>



| <span data-ttu-id="a0829-129">需求</span><span class="sxs-lookup"><span data-stu-id="a0829-129">Requirement</span></span> | <span data-ttu-id="a0829-130">值</span><span class="sxs-lookup"><span data-stu-id="a0829-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0829-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0829-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a0829-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0829-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0829-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0829-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a0829-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="a0829-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a0829-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a0829-135">End of client support</span></span><br/>    | <span data-ttu-id="a0829-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0829-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a0829-137">產品</span><span class="sxs-lookup"><span data-stu-id="a0829-137">Product</span></span><br/>                  | <span data-ttu-id="a0829-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a0829-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a0829-139">標頭</span><span class="sxs-lookup"><span data-stu-id="a0829-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0829-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0829-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a0829-141">IID</span><span class="sxs-lookup"><span data-stu-id="a0829-141">IID</span></span><br/>                      | <span data-ttu-id="a0829-142">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="a0829-142">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a0829-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0829-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0829-144">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="a0829-144">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

