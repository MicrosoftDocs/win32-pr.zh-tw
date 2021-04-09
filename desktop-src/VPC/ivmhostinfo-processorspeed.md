---
title: 'IVMHostInfo >processorspeed 屬性 (VPCCOMInterfaces .h) '
description: 主機處理器的速度，以兆赫 (MHz)  (或 ghz) 。
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- '>processorspeed 屬性 Virtual PC'
- '>processorspeed 屬性 Virtual PC，IVMHostInfo 介面'
- IVMHostInfo 介面 Virtual PC，>processorspeed 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc890392db5f61a7819fa1d4b4a11d2b3de312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024541"
---
# <a name="ivmhostinfoprocessorspeed-property"></a><span data-ttu-id="62ab0-106">IVMHostInfo：:P rocessorSpeed 屬性</span><span class="sxs-lookup"><span data-stu-id="62ab0-106">IVMHostInfo::ProcessorSpeed property</span></span>

<span data-ttu-id="62ab0-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="62ab0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62ab0-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="62ab0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="62ab0-109">抓取主機處理器的速度，以 mhz (MHz)  (或 ghz) 。</span><span class="sxs-lookup"><span data-stu-id="62ab0-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="62ab0-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="62ab0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ab0-111">語法</span><span class="sxs-lookup"><span data-stu-id="62ab0-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="62ab0-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="62ab0-112">Property value</span></span>

<span data-ttu-id="62ab0-113">處理器速度（mhz 或 ghz）。</span><span class="sxs-lookup"><span data-stu-id="62ab0-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62ab0-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="62ab0-114">Error codes</span></span>



| <span data-ttu-id="62ab0-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="62ab0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="62ab0-116">意義</span><span class="sxs-lookup"><span data-stu-id="62ab0-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="62ab0-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62ab0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="62ab0-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="62ab0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="62ab0-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="62ab0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="62ab0-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="62ab0-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="62ab0-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="62ab0-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="62ab0-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="62ab0-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="62ab0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="62ab0-123">Requirements</span></span>



| <span data-ttu-id="62ab0-124">需求</span><span class="sxs-lookup"><span data-stu-id="62ab0-124">Requirement</span></span> | <span data-ttu-id="62ab0-125">值</span><span class="sxs-lookup"><span data-stu-id="62ab0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ab0-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62ab0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="62ab0-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62ab0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62ab0-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62ab0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="62ab0-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="62ab0-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="62ab0-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="62ab0-130">End of client support</span></span><br/>    | <span data-ttu-id="62ab0-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62ab0-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="62ab0-132">產品</span><span class="sxs-lookup"><span data-stu-id="62ab0-132">Product</span></span><br/>                  | <span data-ttu-id="62ab0-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="62ab0-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="62ab0-134">標頭</span><span class="sxs-lookup"><span data-stu-id="62ab0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ab0-135"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="62ab0-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="62ab0-136">IID</span><span class="sxs-lookup"><span data-stu-id="62ab0-136">IID</span></span><br/>                      | <span data-ttu-id="62ab0-137">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="62ab0-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="62ab0-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62ab0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ab0-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="62ab0-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

