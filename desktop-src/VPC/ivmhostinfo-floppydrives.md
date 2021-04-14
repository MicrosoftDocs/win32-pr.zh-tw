---
title: 'IVMHostInfo FloppyDrives 屬性 (VPCCOMInterfaces .h) '
description: 抓取與主機軟碟磁碟機相關聯的磁碟機號。
ms.assetid: 9a8ab4b5-6ee8-463f-809b-b88cd28d9373
keywords:
- FloppyDrives 屬性 Virtual PC
- FloppyDrives 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，FloppyDrives 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.FloppyDrives
- IVMHostInfo.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c31e3ece942f31fc6245c9f23a2995eb7b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384857"
---
# <a name="ivmhostinfofloppydrives-property"></a><span data-ttu-id="69f13-106">IVMHostInfo：： FloppyDrives 屬性</span><span class="sxs-lookup"><span data-stu-id="69f13-106">IVMHostInfo::FloppyDrives property</span></span>

<span data-ttu-id="69f13-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="69f13-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69f13-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="69f13-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69f13-109">抓取與主機軟碟磁碟機相關聯的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="69f13-109">Retrieves the drive letters associated with host floppy drives.</span></span>

<span data-ttu-id="69f13-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="69f13-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f13-111">語法</span><span class="sxs-lookup"><span data-stu-id="69f13-111">Syntax</span></span>


```C++
HRESULT get_FloppyDrives(
  [out, retval] VARIANT *floppyDrives
);
```



## <a name="property-value"></a><span data-ttu-id="69f13-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="69f13-112">Property value</span></span>

<span data-ttu-id="69f13-113">磁碟機號的陣列。</span><span class="sxs-lookup"><span data-stu-id="69f13-113">An array of drive letters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69f13-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="69f13-114">Error codes</span></span>



| <span data-ttu-id="69f13-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="69f13-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="69f13-116">意義</span><span class="sxs-lookup"><span data-stu-id="69f13-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="69f13-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69f13-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="69f13-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="69f13-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="69f13-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="69f13-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="69f13-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="69f13-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="69f13-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="69f13-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="69f13-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="69f13-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="69f13-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="69f13-123">Requirements</span></span>



| <span data-ttu-id="69f13-124">需求</span><span class="sxs-lookup"><span data-stu-id="69f13-124">Requirement</span></span> | <span data-ttu-id="69f13-125">值</span><span class="sxs-lookup"><span data-stu-id="69f13-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f13-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69f13-126">Minimum supported client</span></span><br/> | <span data-ttu-id="69f13-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69f13-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69f13-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69f13-128">Minimum supported server</span></span><br/> | <span data-ttu-id="69f13-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="69f13-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69f13-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="69f13-130">End of client support</span></span><br/>    | <span data-ttu-id="69f13-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69f13-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69f13-132">產品</span><span class="sxs-lookup"><span data-stu-id="69f13-132">Product</span></span><br/>                  | <span data-ttu-id="69f13-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69f13-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69f13-134">標頭</span><span class="sxs-lookup"><span data-stu-id="69f13-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="69f13-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="69f13-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69f13-136">IID</span><span class="sxs-lookup"><span data-stu-id="69f13-136">IID</span></span><br/>                      | <span data-ttu-id="69f13-137">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="69f13-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="69f13-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69f13-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f13-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="69f13-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

