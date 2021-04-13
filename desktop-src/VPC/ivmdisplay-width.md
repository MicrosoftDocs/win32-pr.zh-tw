---
title: 'IVMDisplay Width 屬性 (VPCCOMInterfaces .h) '
description: VM 的顯示寬度（以圖元為單位）。
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Width 屬性 Virtual PC
- Width 屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，Width 屬性
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509259"
---
# <a name="ivmdisplaywidth-property"></a><span data-ttu-id="42bad-106">IVMDisplay：： Width 屬性</span><span class="sxs-lookup"><span data-stu-id="42bad-106">IVMDisplay::Width property</span></span>

<span data-ttu-id="42bad-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="42bad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="42bad-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="42bad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="42bad-109">抓取虛擬機器 (VM) 顯示的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="42bad-109">Retrieves the width of the virtual machine's (VM's) display, in pixels.</span></span>

<span data-ttu-id="42bad-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="42bad-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42bad-111">語法</span><span class="sxs-lookup"><span data-stu-id="42bad-111">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a><span data-ttu-id="42bad-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="42bad-112">Property value</span></span>

<span data-ttu-id="42bad-113">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="42bad-113">The width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42bad-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="42bad-114">Error codes</span></span>



| <span data-ttu-id="42bad-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="42bad-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="42bad-116">意義</span><span class="sxs-lookup"><span data-stu-id="42bad-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42bad-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="42bad-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="42bad-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="42bad-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="42bad-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="42bad-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="42bad-121"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="42bad-122">虛擬機器必須正在執行，才能進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="42bad-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="42bad-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="42bad-124">虛擬機器無效或目前未執行。</span><span class="sxs-lookup"><span data-stu-id="42bad-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="42bad-125"><dt>VM \_E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="42bad-126">找不到虛擬機器的有效顯示。</span><span class="sxs-lookup"><span data-stu-id="42bad-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="42bad-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="42bad-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="42bad-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="42bad-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="42bad-129">Requirements</span></span>



| <span data-ttu-id="42bad-130">需求</span><span class="sxs-lookup"><span data-stu-id="42bad-130">Requirement</span></span> | <span data-ttu-id="42bad-131">值</span><span class="sxs-lookup"><span data-stu-id="42bad-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bad-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42bad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="42bad-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42bad-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42bad-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42bad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="42bad-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="42bad-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="42bad-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="42bad-136">End of client support</span></span><br/>    | <span data-ttu-id="42bad-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42bad-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="42bad-138">產品</span><span class="sxs-lookup"><span data-stu-id="42bad-138">Product</span></span><br/>                  | <span data-ttu-id="42bad-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="42bad-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="42bad-140">標頭</span><span class="sxs-lookup"><span data-stu-id="42bad-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="42bad-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="42bad-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="42bad-142">IID</span><span class="sxs-lookup"><span data-stu-id="42bad-142">IID</span></span><br/>                      | <span data-ttu-id="42bad-143">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="42bad-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="42bad-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42bad-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42bad-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="42bad-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

