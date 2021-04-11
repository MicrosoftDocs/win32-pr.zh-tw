---
title: 'IVMParallelPort Name 屬性 (VPCCOMInterfaces .h) '
description: 平行埠的名稱。
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Name 屬性 Virtual PC
- Name 屬性 Virtual PC，IVMParallelPort 介面
- IVMParallelPort 介面 Virtual PC，Name 屬性
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093752"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="cb3f3-106">IVMParallelPort：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="cb3f3-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="cb3f3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb3f3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="cb3f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb3f3-109">抓取並設定平行埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="cb3f3-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3f3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb3f3-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="cb3f3-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cb3f3-112">Property value</span></span>

<span data-ttu-id="cb3f3-113">設定平行埠 (的名稱，例如 "LPT1" ) 。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb3f3-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cb3f3-114">Error codes</span></span>



| <span data-ttu-id="cb3f3-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="cb3f3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cb3f3-116">意義</span><span class="sxs-lookup"><span data-stu-id="cb3f3-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb3f3-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cb3f3-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="cb3f3-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cb3f3-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cb3f3-121"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f3-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="cb3f3-122">參數參考到不正確平行埠。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="cb3f3-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f3-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="cb3f3-124">此虛擬機器的設定無效。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="cb3f3-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f3-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cb3f3-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb3f3-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="cb3f3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb3f3-127">Requirements</span></span>



| <span data-ttu-id="cb3f3-128">需求</span><span class="sxs-lookup"><span data-stu-id="cb3f3-128">Requirement</span></span> | <span data-ttu-id="cb3f3-129">值</span><span class="sxs-lookup"><span data-stu-id="cb3f3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3f3-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb3f3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3f3-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb3f3-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb3f3-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb3f3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3f3-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="cb3f3-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb3f3-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cb3f3-134">End of client support</span></span><br/>    | <span data-ttu-id="cb3f3-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb3f3-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb3f3-136">產品</span><span class="sxs-lookup"><span data-stu-id="cb3f3-136">Product</span></span><br/>                  | <span data-ttu-id="cb3f3-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb3f3-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb3f3-138">標頭</span><span class="sxs-lookup"><span data-stu-id="cb3f3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb3f3-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3f3-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb3f3-140">IID</span><span class="sxs-lookup"><span data-stu-id="cb3f3-140">IID</span></span><br/>                      | <span data-ttu-id="cb3f3-141">IID \_ IVMParallelPort 定義為097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="cb3f3-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="cb3f3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb3f3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3f3-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="cb3f3-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

