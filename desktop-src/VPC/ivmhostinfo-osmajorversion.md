---
title: 'IVMHostInfo OSMajorVersion 屬性 (VPCCOMInterfaces .h) '
description: 抓取主機電腦上執行之作業系統的主要版本。
ms.assetid: d0b62d2d-532f-45c7-8622-67176b9b4a8f
keywords:
- OSMajorVersion 屬性 Virtual PC
- OSMajorVersion 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，OSMajorVersion 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMajorVersion
- IVMHostInfo.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf064744d90ede010a7e48e0e23e6a62a19eb4af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383814"
---
# <a name="ivmhostinfoosmajorversion-property"></a><span data-ttu-id="f808f-106">IVMHostInfo：： OSMajorVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="f808f-106">IVMHostInfo::OSMajorVersion property</span></span>

<span data-ttu-id="f808f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f808f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f808f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f808f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f808f-109">抓取主機電腦上執行之作業系統的主要版本。</span><span class="sxs-lookup"><span data-stu-id="f808f-109">Retrieves the major version of the operating system running on the host machine.</span></span>

<span data-ttu-id="f808f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f808f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f808f-111">語法</span><span class="sxs-lookup"><span data-stu-id="f808f-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] long *osMajorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="f808f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f808f-112">Property value</span></span>

<span data-ttu-id="f808f-113">主要版本。</span><span class="sxs-lookup"><span data-stu-id="f808f-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f808f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f808f-114">Error codes</span></span>



| <span data-ttu-id="f808f-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="f808f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f808f-116">意義</span><span class="sxs-lookup"><span data-stu-id="f808f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f808f-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f808f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f808f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f808f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f808f-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f808f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f808f-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f808f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f808f-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f808f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f808f-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f808f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f808f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f808f-123">Requirements</span></span>



| <span data-ttu-id="f808f-124">需求</span><span class="sxs-lookup"><span data-stu-id="f808f-124">Requirement</span></span> | <span data-ttu-id="f808f-125">值</span><span class="sxs-lookup"><span data-stu-id="f808f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f808f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f808f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f808f-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f808f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f808f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f808f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f808f-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="f808f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f808f-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f808f-130">End of client support</span></span><br/>    | <span data-ttu-id="f808f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f808f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f808f-132">產品</span><span class="sxs-lookup"><span data-stu-id="f808f-132">Product</span></span><br/>                  | <span data-ttu-id="f808f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f808f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f808f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f808f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f808f-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f808f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f808f-136">IID</span><span class="sxs-lookup"><span data-stu-id="f808f-136">IID</span></span><br/>                      | <span data-ttu-id="f808f-137">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="f808f-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f808f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f808f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f808f-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="f808f-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

