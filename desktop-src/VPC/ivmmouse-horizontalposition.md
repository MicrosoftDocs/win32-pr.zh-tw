---
title: 'IVMMouse HorizontalPosition 屬性 (VPCCOMInterfaces .h) '
description: 滑鼠的絕對 x 座標。
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- HorizontalPosition 屬性 Virtual PC
- HorizontalPosition 屬性 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，HorizontalPosition 屬性
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8506ad0d4583b9829ca2b1832686d32e67ded261
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935027"
---
# <a name="ivmmousehorizontalposition-property"></a><span data-ttu-id="ab998-106">IVMMouse：： HorizontalPosition 屬性</span><span class="sxs-lookup"><span data-stu-id="ab998-106">IVMMouse::HorizontalPosition property</span></span>

<span data-ttu-id="ab998-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ab998-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ab998-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ab998-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ab998-109">抓取滑鼠的絕對 x 座標。</span><span class="sxs-lookup"><span data-stu-id="ab998-109">Retrieves the absolute x-coordinate of the mouse.</span></span>

<span data-ttu-id="ab998-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ab998-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab998-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab998-111">Syntax</span></span>


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="ab998-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="ab998-112">Property value</span></span>

<span data-ttu-id="ab998-113">表示滑鼠新位置的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="ab998-113">The x-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="ab998-114">使用絕對座標時，此值會指定滑鼠的新 x 座標。</span><span class="sxs-lookup"><span data-stu-id="ab998-114">When using absolute coordinates, this value specifies the new x-coordinate of the mouse.</span></span> <span data-ttu-id="ab998-115">使用相對座標時，此值會指定要以 x 方向移動滑鼠的圖元數。</span><span class="sxs-lookup"><span data-stu-id="ab998-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the x direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ab998-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ab998-116">Error codes</span></span>



| <span data-ttu-id="ab998-117">名稱/值</span><span class="sxs-lookup"><span data-stu-id="ab998-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="ab998-118">意義</span><span class="sxs-lookup"><span data-stu-id="ab998-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab998-119"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="ab998-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ab998-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="ab998-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="ab998-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ab998-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="ab998-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="ab998-124">此滑鼠裝置所連接的虛擬機器目前不在執行中。</span><span class="sxs-lookup"><span data-stu-id="ab998-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="ab998-125"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="ab998-126">您必須安裝整合元件才能取出滑鼠位置，或在使用絕對座標時設定滑鼠位置。</span><span class="sxs-lookup"><span data-stu-id="ab998-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="ab998-127"><dt>VM \_E \_ 使用 \_ 相對 \_ 座標</dt> <dt>0xA0040802</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="ab998-128">滑鼠裝置目前設定為使用相對滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="ab998-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="ab998-129"><dt>VM \_E \_ 滑鼠 \_ 非 \_ </dt>使用中 <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="ab998-130">如果滑鼠裝置未啟動，或虛擬機器中目前未啟用，則無法抓取絕對座標。</span><span class="sxs-lookup"><span data-stu-id="ab998-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="ab998-131"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="ab998-132">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ab998-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="ab998-133">備註</span><span class="sxs-lookup"><span data-stu-id="ab998-133">Remarks</span></span>

<span data-ttu-id="ab998-134">使用相對座標時，無法抓取此屬性。</span><span class="sxs-lookup"><span data-stu-id="ab998-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab998-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab998-135">Requirements</span></span>



| <span data-ttu-id="ab998-136">需求</span><span class="sxs-lookup"><span data-stu-id="ab998-136">Requirement</span></span> | <span data-ttu-id="ab998-137">值</span><span class="sxs-lookup"><span data-stu-id="ab998-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab998-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab998-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ab998-139">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab998-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab998-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab998-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ab998-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="ab998-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ab998-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ab998-142">End of client support</span></span><br/>    | <span data-ttu-id="ab998-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab998-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ab998-144">產品</span><span class="sxs-lookup"><span data-stu-id="ab998-144">Product</span></span><br/>                  | <span data-ttu-id="ab998-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ab998-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ab998-146">標頭</span><span class="sxs-lookup"><span data-stu-id="ab998-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab998-147"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab998-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ab998-148">IID</span><span class="sxs-lookup"><span data-stu-id="ab998-148">IID</span></span><br/>                      | <span data-ttu-id="ab998-149">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="ab998-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="ab998-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab998-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab998-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="ab998-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

