---
title: 'IVMMouse Click method (VPCCOMInterfaces. h) '
description: 模擬滑鼠按鍵的點擊。
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- 按一下 [方法虛擬電腦]
- 按一下 [方法 Virtual PC，IVMMouse 介面]
- IVMMouse 介面 Virtual PC，按一下 [方法]
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466829"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="fbc3e-106">IVMMouse：： Click 方法</span><span class="sxs-lookup"><span data-stu-id="fbc3e-106">IVMMouse::Click method</span></span>

<span data-ttu-id="fbc3e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fbc3e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fbc3e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fbc3e-109">模擬滑鼠按鍵的點擊。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc3e-110">語法</span><span class="sxs-lookup"><span data-stu-id="fbc3e-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="fbc3e-111">參數</span><span class="sxs-lookup"><span data-stu-id="fbc3e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc3e-112">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbc3e-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbc3e-113">要按一下之按鈕的索引。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-113">The index of the button being clicked.</span></span> <span data-ttu-id="fbc3e-114">如需值的清單，請參閱 [**VMMouseButton**](vmmousebutton.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc3e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbc3e-115">Return value</span></span>

<span data-ttu-id="fbc3e-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fbc3e-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="fbc3e-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="fbc3e-118">Description</span><span class="sxs-lookup"><span data-stu-id="fbc3e-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbc3e-119"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="fbc3e-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="fbc3e-121"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="fbc3e-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="fbc3e-123"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="fbc3e-124">此滑鼠裝置所連接的虛擬機器目前不在執行中。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="fbc3e-125"><dt>**VM \_E \_ 滑鼠 \_ 非 \_**</dt>使用中 <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="fbc3e-126">無法完成作業，因為滑鼠裝置未啟動，或虛擬機器中目前未處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="fbc3e-127"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="fbc3e-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbc3e-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="fbc3e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbc3e-129">Requirements</span></span>



| <span data-ttu-id="fbc3e-130">需求</span><span class="sxs-lookup"><span data-stu-id="fbc3e-130">Requirement</span></span> | <span data-ttu-id="fbc3e-131">值</span><span class="sxs-lookup"><span data-stu-id="fbc3e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc3e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbc3e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc3e-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbc3e-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbc3e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbc3e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc3e-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="fbc3e-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fbc3e-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fbc3e-136">End of client support</span></span><br/>    | <span data-ttu-id="fbc3e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbc3e-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fbc3e-138">產品</span><span class="sxs-lookup"><span data-stu-id="fbc3e-138">Product</span></span><br/>                  | <span data-ttu-id="fbc3e-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fbc3e-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fbc3e-140">標頭</span><span class="sxs-lookup"><span data-stu-id="fbc3e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc3e-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3e-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fbc3e-142">IID</span><span class="sxs-lookup"><span data-stu-id="fbc3e-142">IID</span></span><br/>                      | <span data-ttu-id="fbc3e-143">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="fbc3e-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="fbc3e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbc3e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc3e-145">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="fbc3e-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

