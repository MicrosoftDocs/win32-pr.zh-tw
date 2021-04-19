---
title: 'IVMHostInfo ProcessorFeaturesString 屬性 (VPCCOMInterfaces .h) '
description: 抓取主機處理器所支援的清單功能。
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- ProcessorFeaturesString 屬性 Virtual PC
- ProcessorFeaturesString 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，ProcessorFeaturesString 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966080"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="37f48-106">IVMHostInfo：:P rocessorFeaturesString 屬性</span><span class="sxs-lookup"><span data-stu-id="37f48-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="37f48-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="37f48-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="37f48-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="37f48-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="37f48-109">抓取主機處理器所支援的清單功能。</span><span class="sxs-lookup"><span data-stu-id="37f48-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="37f48-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="37f48-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f48-111">語法</span><span class="sxs-lookup"><span data-stu-id="37f48-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="37f48-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="37f48-112">Property value</span></span>

<span data-ttu-id="37f48-113">以逗號分隔的功能清單。</span><span class="sxs-lookup"><span data-stu-id="37f48-113">A comma-delimited list of features.</span></span> <span data-ttu-id="37f48-114">例如，「MMX、SSE、SSE2、x86-64」。</span><span class="sxs-lookup"><span data-stu-id="37f48-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="37f48-115">值</span><span class="sxs-lookup"><span data-stu-id="37f48-115">Value</span></span>                                                                                 | <span data-ttu-id="37f48-116">意義</span><span class="sxs-lookup"><span data-stu-id="37f48-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="37f48-117"><dt>"AMD-V"</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="37f48-118">支援 AMD 虛擬化延伸模組。</span><span class="sxs-lookup"><span data-stu-id="37f48-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="37f48-119"><dt>"Intel VT"</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="37f48-120">支援 Intel 虛擬化技術擴充功能。</span><span class="sxs-lookup"><span data-stu-id="37f48-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="37f48-121"><dt>"HAVD"</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="37f48-122">硬體輔助虛擬化已停用。</span><span class="sxs-lookup"><span data-stu-id="37f48-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="37f48-123"><dt>使用</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="37f48-124">啟用硬體輔助虛擬化。</span><span class="sxs-lookup"><span data-stu-id="37f48-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="37f48-125"><dt>™</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="37f48-126">支援 MMX 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="37f48-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="37f48-127"><dt>SSE</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="37f48-128">支援 Streaming SIMD Extensions。</span><span class="sxs-lookup"><span data-stu-id="37f48-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="37f48-129"><dt>發揮</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="37f48-130">支援 Streaming SIMD Extensions 2。</span><span class="sxs-lookup"><span data-stu-id="37f48-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="37f48-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="37f48-132">支援 Streaming SIMD Extensions 3。</span><span class="sxs-lookup"><span data-stu-id="37f48-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="37f48-133"><dt>"TXTE"</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="37f48-134">支援受信任的執行技術擴充功能。</span><span class="sxs-lookup"><span data-stu-id="37f48-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="37f48-135"><dt>"x86-64"</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="37f48-136">支援 x86-64 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="37f48-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="37f48-137">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="37f48-137">Error codes</span></span>



| <span data-ttu-id="37f48-138">名稱/值</span><span class="sxs-lookup"><span data-stu-id="37f48-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="37f48-139">意義</span><span class="sxs-lookup"><span data-stu-id="37f48-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="37f48-140"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="37f48-141">作業成功。</span><span class="sxs-lookup"><span data-stu-id="37f48-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="37f48-142"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="37f48-143">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="37f48-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="37f48-144"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="37f48-145">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="37f48-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="37f48-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="37f48-146">Requirements</span></span>



| <span data-ttu-id="37f48-147">需求</span><span class="sxs-lookup"><span data-stu-id="37f48-147">Requirement</span></span> | <span data-ttu-id="37f48-148">值</span><span class="sxs-lookup"><span data-stu-id="37f48-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f48-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37f48-149">Minimum supported client</span></span><br/> | <span data-ttu-id="37f48-150">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37f48-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37f48-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37f48-151">Minimum supported server</span></span><br/> | <span data-ttu-id="37f48-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="37f48-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="37f48-153">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="37f48-153">End of client support</span></span><br/>    | <span data-ttu-id="37f48-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37f48-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="37f48-155">產品</span><span class="sxs-lookup"><span data-stu-id="37f48-155">Product</span></span><br/>                  | <span data-ttu-id="37f48-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="37f48-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="37f48-157">標頭</span><span class="sxs-lookup"><span data-stu-id="37f48-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f48-158"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="37f48-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="37f48-159">IID</span><span class="sxs-lookup"><span data-stu-id="37f48-159">IID</span></span><br/>                      | <span data-ttu-id="37f48-160">IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="37f48-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="37f48-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37f48-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f48-162">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="37f48-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

