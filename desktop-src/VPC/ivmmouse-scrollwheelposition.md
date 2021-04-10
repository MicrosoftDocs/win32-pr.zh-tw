---
title: 'IVMMouse ScrollWheelPosition 屬性 (VPCCOMInterfaces .h) '
description: 調整滑鼠 (相對) 的 z 座標。
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- ScrollWheelPosition 屬性 Virtual PC
- ScrollWheelPosition 屬性 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，ScrollWheelPosition 屬性
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686404"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="9a7ac-106">IVMMouse：： ScrollWheelPosition 屬性</span><span class="sxs-lookup"><span data-stu-id="9a7ac-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="9a7ac-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9a7ac-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="9a7ac-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9a7ac-109">調整滑鼠 (相對) 的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="9a7ac-110">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7ac-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a7ac-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="9a7ac-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9a7ac-112">Property value</span></span>

<span data-ttu-id="9a7ac-113">Z 座標，指出滑鼠沿著 Z 軸移動的圖元數。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a7ac-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9a7ac-114">Error codes</span></span>



| <span data-ttu-id="9a7ac-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="9a7ac-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="9a7ac-116">意義</span><span class="sxs-lookup"><span data-stu-id="9a7ac-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a7ac-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="9a7ac-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="9a7ac-119"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="9a7ac-120">此滑鼠裝置所連接的虛擬機器目前不在執行中。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="9a7ac-121"><dt>VM \_E \_ 滑鼠 \_ 非 \_ </dt>使用中 <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="9a7ac-122">滑鼠裝置尚未開機，或目前未在虛擬機器中啟用。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="9a7ac-123"><dt>VM \_E \_ 使用 \_ 絕對 \_ 座標</dt> <dt>0xA0040801</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="9a7ac-124">當滑鼠裝置使用絕對座標時，無法設定捲軸位置。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="9a7ac-125"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="9a7ac-126">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="9a7ac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a7ac-127">Requirements</span></span>



| <span data-ttu-id="9a7ac-128">需求</span><span class="sxs-lookup"><span data-stu-id="9a7ac-128">Requirement</span></span> | <span data-ttu-id="9a7ac-129">值</span><span class="sxs-lookup"><span data-stu-id="9a7ac-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7ac-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a7ac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7ac-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a7ac-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9a7ac-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a7ac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7ac-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="9a7ac-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9a7ac-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9a7ac-134">End of client support</span></span><br/>    | <span data-ttu-id="9a7ac-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a7ac-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9a7ac-136">產品</span><span class="sxs-lookup"><span data-stu-id="9a7ac-136">Product</span></span><br/>                  | <span data-ttu-id="9a7ac-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9a7ac-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9a7ac-138">標頭</span><span class="sxs-lookup"><span data-stu-id="9a7ac-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7ac-139"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9a7ac-140">IID</span><span class="sxs-lookup"><span data-stu-id="9a7ac-140">IID</span></span><br/>                      | <span data-ttu-id="9a7ac-141">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="9a7ac-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="9a7ac-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a7ac-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7ac-143">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="9a7ac-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

