---
title: 'IVMMouse GetButton 方法 (VPCCOMInterfaces .h) '
description: 抓取指定滑鼠按鍵的目前狀態。
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- GetButton 方法 Virtual PC
- GetButton 方法 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，GetButton 方法
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686407"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="56b6b-106">IVMMouse：： GetButton 方法</span><span class="sxs-lookup"><span data-stu-id="56b6b-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="56b6b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="56b6b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56b6b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="56b6b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56b6b-109">抓取所指定滑鼠按鍵的目前狀態 (向上或向下) 。</span><span class="sxs-lookup"><span data-stu-id="56b6b-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b6b-110">語法</span><span class="sxs-lookup"><span data-stu-id="56b6b-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="56b6b-111">參數</span><span class="sxs-lookup"><span data-stu-id="56b6b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b6b-112">*buttonIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56b6b-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56b6b-113">正在要求其狀態的按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="56b6b-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="56b6b-114">如需值的清單，請參閱 [**VMMouseButton**](vmmousebutton.md)。</span><span class="sxs-lookup"><span data-stu-id="56b6b-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="56b6b-115">*isDown* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="56b6b-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="56b6b-116">指定之按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="56b6b-116">The state of the indicated button.</span></span> <span data-ttu-id="56b6b-117">如果此按鈕目前在虛擬機器中是關閉的，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="56b6b-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b6b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="56b6b-118">Return value</span></span>

<span data-ttu-id="56b6b-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56b6b-119">This method can return one of these values.</span></span>



| <span data-ttu-id="56b6b-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="56b6b-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="56b6b-121">Description</span><span class="sxs-lookup"><span data-stu-id="56b6b-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56b6b-122"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="56b6b-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="56b6b-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="56b6b-124"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="56b6b-125">*IsDown* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="56b6b-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="56b6b-126"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="56b6b-127">*ButtonIndex* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="56b6b-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="56b6b-128"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="56b6b-129">此滑鼠裝置所連接的虛擬機器目前不在執行中。</span><span class="sxs-lookup"><span data-stu-id="56b6b-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="56b6b-130"><dt>**VM \_E \_ 滑鼠 \_ 非 \_**</dt>使用中 <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="56b6b-131">滑鼠裝置尚未開機。</span><span class="sxs-lookup"><span data-stu-id="56b6b-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="56b6b-132"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="56b6b-133">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="56b6b-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="56b6b-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="56b6b-134">Requirements</span></span>



| <span data-ttu-id="56b6b-135">需求</span><span class="sxs-lookup"><span data-stu-id="56b6b-135">Requirement</span></span> | <span data-ttu-id="56b6b-136">值</span><span class="sxs-lookup"><span data-stu-id="56b6b-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b6b-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56b6b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="56b6b-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b6b-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56b6b-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56b6b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="56b6b-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="56b6b-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56b6b-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="56b6b-141">End of client support</span></span><br/>    | <span data-ttu-id="56b6b-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56b6b-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56b6b-143">產品</span><span class="sxs-lookup"><span data-stu-id="56b6b-143">Product</span></span><br/>                  | <span data-ttu-id="56b6b-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56b6b-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56b6b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="56b6b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b6b-146"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="56b6b-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56b6b-147">IID</span><span class="sxs-lookup"><span data-stu-id="56b6b-147">IID</span></span><br/>                      | <span data-ttu-id="56b6b-148">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="56b6b-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="56b6b-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56b6b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b6b-150">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="56b6b-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

