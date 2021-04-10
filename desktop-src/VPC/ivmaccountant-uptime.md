---
title: 'IVMAccountant 執行時間屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器已執行的秒數。
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- 執行時間屬性 Virtual PC
- 執行時間屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面虛擬電腦，執行時間屬性
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c496aa9c32d402dcc8e84bad5410ec7774d2a80a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103979"
---
# <a name="ivmaccountantuptime-property"></a><span data-ttu-id="1900f-106">IVMAccountant：：執行時間屬性</span><span class="sxs-lookup"><span data-stu-id="1900f-106">IVMAccountant::UpTime property</span></span>

<span data-ttu-id="1900f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="1900f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1900f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="1900f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1900f-109">抓取虛擬機器已執行的秒數。</span><span class="sxs-lookup"><span data-stu-id="1900f-109">Retrieves the number of seconds that the virtual machine has been running.</span></span>

<span data-ttu-id="1900f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1900f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1900f-111">語法</span><span class="sxs-lookup"><span data-stu-id="1900f-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="1900f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="1900f-112">Property value</span></span>

<span data-ttu-id="1900f-113">秒數。</span><span class="sxs-lookup"><span data-stu-id="1900f-113">The number of seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1900f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1900f-114">Error codes</span></span>



| <span data-ttu-id="1900f-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="1900f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1900f-116">意義</span><span class="sxs-lookup"><span data-stu-id="1900f-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="1900f-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1900f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1900f-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="1900f-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="1900f-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1900f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1900f-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1900f-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="1900f-121"><dt>S \_FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1900f-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="1900f-122">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="1900f-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="1900f-123"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1900f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1900f-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1900f-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="1900f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1900f-125">Requirements</span></span>



| <span data-ttu-id="1900f-126">需求</span><span class="sxs-lookup"><span data-stu-id="1900f-126">Requirement</span></span> | <span data-ttu-id="1900f-127">值</span><span class="sxs-lookup"><span data-stu-id="1900f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1900f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1900f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1900f-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1900f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1900f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1900f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1900f-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="1900f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1900f-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1900f-132">End of client support</span></span><br/>    | <span data-ttu-id="1900f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1900f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1900f-134">產品</span><span class="sxs-lookup"><span data-stu-id="1900f-134">Product</span></span><br/>                  | <span data-ttu-id="1900f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1900f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1900f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="1900f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1900f-137"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="1900f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1900f-138">IID</span><span class="sxs-lookup"><span data-stu-id="1900f-138">IID</span></span><br/>                      | <span data-ttu-id="1900f-139">IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="1900f-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="1900f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1900f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1900f-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="1900f-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

