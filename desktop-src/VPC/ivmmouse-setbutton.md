---
title: 'IVMMouse SetButton 方法 (VPCCOMInterfaces .h) '
description: 將目前狀態 () 指定的滑鼠按鍵。
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- SetButton 方法 Virtual PC
- SetButton 方法 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，SetButton 方法
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105677"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="3e886-106">IVMMouse：： SetButton 方法</span><span class="sxs-lookup"><span data-stu-id="3e886-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="3e886-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3e886-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e886-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3e886-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e886-109">將目前狀態 () 指定的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="3e886-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e886-110">語法</span><span class="sxs-lookup"><span data-stu-id="3e886-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="3e886-111">參數</span><span class="sxs-lookup"><span data-stu-id="3e886-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e886-112">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e886-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e886-113">按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="3e886-113">The button index.</span></span> <span data-ttu-id="3e886-114">如需值的清單，請參閱 [**VMMouseButton**](vmmousebutton.md)。</span><span class="sxs-lookup"><span data-stu-id="3e886-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e886-115">*向下* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e886-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e886-116">新的按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="3e886-116">The new button state.</span></span> <span data-ttu-id="3e886-117">如果按鈕狀態設為 down，則使用 **TRUE** ，如果要設定為向上則使用 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3e886-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e886-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e886-118">Return value</span></span>

<span data-ttu-id="3e886-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3e886-119">This method can return one of these values.</span></span>



| <span data-ttu-id="3e886-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3e886-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="3e886-121">Description</span><span class="sxs-lookup"><span data-stu-id="3e886-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e886-122"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e886-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="3e886-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3e886-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="3e886-124"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3e886-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="3e886-125">*ButtonIndex* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="3e886-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="3e886-126"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3e886-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="3e886-127">此滑鼠裝置所連接的虛擬機器目前不在執行中。</span><span class="sxs-lookup"><span data-stu-id="3e886-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="3e886-128"><dt>**VM \_E \_ 滑鼠 \_ 非 \_**</dt>使用中 <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="3e886-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="3e886-129">無法完成作業，因為滑鼠裝置未啟動，或虛擬機器中目前未處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="3e886-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="3e886-130"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3e886-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="3e886-131">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3e886-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="3e886-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e886-132">Requirements</span></span>



| <span data-ttu-id="3e886-133">需求</span><span class="sxs-lookup"><span data-stu-id="3e886-133">Requirement</span></span> | <span data-ttu-id="3e886-134">值</span><span class="sxs-lookup"><span data-stu-id="3e886-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e886-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e886-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3e886-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e886-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e886-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e886-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3e886-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e886-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e886-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3e886-139">End of client support</span></span><br/>    | <span data-ttu-id="3e886-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e886-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e886-141">產品</span><span class="sxs-lookup"><span data-stu-id="3e886-141">Product</span></span><br/>                  | <span data-ttu-id="3e886-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e886-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e886-143">標頭</span><span class="sxs-lookup"><span data-stu-id="3e886-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e886-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e886-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e886-145">IID</span><span class="sxs-lookup"><span data-stu-id="3e886-145">IID</span></span><br/>                      | <span data-ttu-id="3e886-146">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="3e886-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="3e886-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e886-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e886-148">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="3e886-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

