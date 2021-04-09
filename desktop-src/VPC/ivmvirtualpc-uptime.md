---
title: 'IVMVirtualPC 執行時間屬性 (VPCCOMInterfaces .h) '
description: 捕獲 Windows Virtual PC 應用程式執行的秒數。
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- 執行時間屬性 Virtual PC
- 執行時間屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面虛擬電腦，執行時間屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab07128380a097677e0ad8acca5208e5cef11da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686396"
---
# <a name="ivmvirtualpcuptime-property"></a><span data-ttu-id="b98c9-106">IVMVirtualPC：：執行時間屬性</span><span class="sxs-lookup"><span data-stu-id="b98c9-106">IVMVirtualPC::UpTime property</span></span>

<span data-ttu-id="b98c9-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b98c9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b98c9-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b98c9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b98c9-109">捕獲 Windows Virtual PC 應用程式執行的秒數。</span><span class="sxs-lookup"><span data-stu-id="b98c9-109">Retrieves the number of seconds the Windows Virtual PC application has been running.</span></span>

<span data-ttu-id="b98c9-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b98c9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b98c9-111">語法</span><span class="sxs-lookup"><span data-stu-id="b98c9-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="b98c9-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="b98c9-112">Property value</span></span>

<span data-ttu-id="b98c9-113">Windows Virtual PC 應用程式執行的秒數。</span><span class="sxs-lookup"><span data-stu-id="b98c9-113">The number of seconds that the Windows Virtual PC application has been running.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b98c9-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b98c9-114">Error codes</span></span>



| <span data-ttu-id="b98c9-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="b98c9-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="b98c9-116">意義</span><span class="sxs-lookup"><span data-stu-id="b98c9-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b98c9-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b98c9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="b98c9-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b98c9-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b98c9-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b98c9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="b98c9-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b98c9-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b98c9-121"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b98c9-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="b98c9-122">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b98c9-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b98c9-123"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="b98c9-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="b98c9-124">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b98c9-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b98c9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b98c9-125">Requirements</span></span>



| <span data-ttu-id="b98c9-126">需求</span><span class="sxs-lookup"><span data-stu-id="b98c9-126">Requirement</span></span> | <span data-ttu-id="b98c9-127">值</span><span class="sxs-lookup"><span data-stu-id="b98c9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b98c9-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b98c9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b98c9-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b98c9-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b98c9-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b98c9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b98c9-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="b98c9-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b98c9-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b98c9-132">End of client support</span></span><br/>    | <span data-ttu-id="b98c9-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b98c9-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b98c9-134">產品</span><span class="sxs-lookup"><span data-stu-id="b98c9-134">Product</span></span><br/>                  | <span data-ttu-id="b98c9-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b98c9-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b98c9-136">標頭</span><span class="sxs-lookup"><span data-stu-id="b98c9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b98c9-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b98c9-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b98c9-138">IID</span><span class="sxs-lookup"><span data-stu-id="b98c9-138">IID</span></span><br/>                      | <span data-ttu-id="b98c9-139">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b98c9-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b98c9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b98c9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b98c9-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="b98c9-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

