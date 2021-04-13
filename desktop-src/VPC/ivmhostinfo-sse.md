---
title: 'IVMHostInfo SSE 屬性 (VPCCOMInterfaces .h) '
description: '判斷處理器是否支援 SSE 指令集。 |IVMHostInfo SSE 屬性 (VPCCOMInterfaces .h) '
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- SSE 屬性 Virtual PC
- SSE 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，SSE 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322368"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="97e86-107">IVMHostInfo：： SSE 屬性</span><span class="sxs-lookup"><span data-stu-id="97e86-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="97e86-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="97e86-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="97e86-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="97e86-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="97e86-110">判斷處理器是否支援 SSE 指令集。</span><span class="sxs-lookup"><span data-stu-id="97e86-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="97e86-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="97e86-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e86-112">語法</span><span class="sxs-lookup"><span data-stu-id="97e86-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="97e86-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="97e86-113">Property value</span></span>

<span data-ttu-id="97e86-114">如果主機處理器支援 SSE 指令，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="97e86-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="97e86-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="97e86-115">Error codes</span></span>



| <span data-ttu-id="97e86-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="97e86-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="97e86-117">意義</span><span class="sxs-lookup"><span data-stu-id="97e86-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="97e86-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="97e86-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="97e86-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="97e86-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="97e86-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="97e86-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="97e86-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="97e86-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="97e86-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="97e86-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="97e86-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="97e86-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="97e86-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="97e86-124">Requirements</span></span>



| <span data-ttu-id="97e86-125">需求</span><span class="sxs-lookup"><span data-stu-id="97e86-125">Requirement</span></span> | <span data-ttu-id="97e86-126">值</span><span class="sxs-lookup"><span data-stu-id="97e86-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e86-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97e86-127">Minimum supported client</span></span><br/> | <span data-ttu-id="97e86-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97e86-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97e86-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97e86-129">Minimum supported server</span></span><br/> | <span data-ttu-id="97e86-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="97e86-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="97e86-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="97e86-131">End of client support</span></span><br/>    | <span data-ttu-id="97e86-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="97e86-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="97e86-133">產品</span><span class="sxs-lookup"><span data-stu-id="97e86-133">Product</span></span><br/>                  | <span data-ttu-id="97e86-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="97e86-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="97e86-135">標頭</span><span class="sxs-lookup"><span data-stu-id="97e86-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e86-136"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="97e86-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="97e86-137">IID</span><span class="sxs-lookup"><span data-stu-id="97e86-137">IID</span></span><br/>                      | <span data-ttu-id="97e86-138">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="97e86-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="97e86-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97e86-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e86-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="97e86-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

