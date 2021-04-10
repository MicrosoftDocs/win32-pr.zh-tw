---
title: 'IVMVirtualMachine HasSSE 屬性 (VPCCOMInterfaces .h) '
description: '判斷處理器是否支援 SSE 指令集。 |IVMVirtualMachine HasSSE 屬性 (VPCCOMInterfaces .h) '
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- HasSSE 屬性 Virtual PC
- HasSSE 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，HasSSE 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853907"
---
# <a name="ivmvirtualmachinehassse-property"></a><span data-ttu-id="4648d-107">IVMVirtualMachine：： HasSSE 屬性</span><span class="sxs-lookup"><span data-stu-id="4648d-107">IVMVirtualMachine::HasSSE property</span></span>

<span data-ttu-id="4648d-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="4648d-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4648d-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="4648d-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4648d-110">判斷處理器是否支援 SSE 指令集。</span><span class="sxs-lookup"><span data-stu-id="4648d-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="4648d-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4648d-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4648d-112">語法</span><span class="sxs-lookup"><span data-stu-id="4648d-112">Syntax</span></span>


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="4648d-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="4648d-113">Property value</span></span>

<span data-ttu-id="4648d-114">如果處理器支援 SSE 指令集，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4648d-114">**TRUE** if the processor supported the SSE instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4648d-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4648d-115">Error codes</span></span>



| <span data-ttu-id="4648d-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="4648d-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4648d-117">意義</span><span class="sxs-lookup"><span data-stu-id="4648d-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4648d-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4648d-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4648d-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="4648d-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4648d-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4648d-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4648d-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4648d-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4648d-122"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="4648d-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4648d-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="4648d-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="4648d-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4648d-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4648d-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4648d-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4648d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4648d-126">Requirements</span></span>



| <span data-ttu-id="4648d-127">需求</span><span class="sxs-lookup"><span data-stu-id="4648d-127">Requirement</span></span> | <span data-ttu-id="4648d-128">值</span><span class="sxs-lookup"><span data-stu-id="4648d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4648d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4648d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4648d-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4648d-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4648d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4648d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4648d-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="4648d-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4648d-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4648d-133">End of client support</span></span><br/>    | <span data-ttu-id="4648d-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4648d-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4648d-135">產品</span><span class="sxs-lookup"><span data-stu-id="4648d-135">Product</span></span><br/>                  | <span data-ttu-id="4648d-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4648d-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4648d-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4648d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4648d-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="4648d-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4648d-139">IID</span><span class="sxs-lookup"><span data-stu-id="4648d-139">IID</span></span><br/>                      | <span data-ttu-id="4648d-140">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4648d-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4648d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4648d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4648d-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4648d-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

