---
title: 'IVMMouse UsingAbsoluteCoordinates 屬性 (VPCCOMInterfaces .h) '
description: 抓取滑鼠座標是否代表絕對或相對座標。
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- UsingAbsoluteCoordinates 屬性 Virtual PC
- UsingAbsoluteCoordinates 屬性 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，UsingAbsoluteCoordinates 屬性
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509199"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="08dad-106">IVMMouse：： UsingAbsoluteCoordinates 屬性</span><span class="sxs-lookup"><span data-stu-id="08dad-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="08dad-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="08dad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="08dad-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="08dad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="08dad-109">抓取滑鼠座標是否代表絕對或相對座標。</span><span class="sxs-lookup"><span data-stu-id="08dad-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="08dad-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="08dad-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="08dad-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="08dad-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="08dad-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="08dad-112">Property value</span></span>

<span data-ttu-id="08dad-113">**變異 \_TRUE** 表示將滑鼠裝置設定為使用絕對座標， **VARIANT \_ FALSE** 表示使用相對座標。</span><span class="sxs-lookup"><span data-stu-id="08dad-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08dad-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="08dad-114">Error codes</span></span>



| <span data-ttu-id="08dad-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="08dad-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="08dad-116">意義</span><span class="sxs-lookup"><span data-stu-id="08dad-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08dad-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="08dad-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="08dad-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="08dad-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="08dad-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="08dad-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="08dad-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="08dad-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="08dad-121"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="08dad-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="08dad-122">此滑鼠裝置所連接的虛擬機器目前不在執行中。</span><span class="sxs-lookup"><span data-stu-id="08dad-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="08dad-123"><dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="08dad-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="08dad-124">未安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="08dad-124">Integration components are not installed.</span></span> <span data-ttu-id="08dad-125">需要整合元件才能使用絕對座標。</span><span class="sxs-lookup"><span data-stu-id="08dad-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="08dad-126"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="08dad-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="08dad-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="08dad-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="08dad-128">備註</span><span class="sxs-lookup"><span data-stu-id="08dad-128">Remarks</span></span>

<span data-ttu-id="08dad-129">這個屬性只會在此物件的本機上，而新的 [**IVMMouse**](ivmmouse.md)物件會預設為 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="08dad-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="08dad-130">請注意，您必須安裝整合元件，才能使用絕對座標。</span><span class="sxs-lookup"><span data-stu-id="08dad-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="08dad-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="08dad-131">Requirements</span></span>



| <span data-ttu-id="08dad-132">需求</span><span class="sxs-lookup"><span data-stu-id="08dad-132">Requirement</span></span> | <span data-ttu-id="08dad-133">值</span><span class="sxs-lookup"><span data-stu-id="08dad-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="08dad-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08dad-134">Minimum supported client</span></span><br/> | <span data-ttu-id="08dad-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08dad-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08dad-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08dad-136">Minimum supported server</span></span><br/> | <span data-ttu-id="08dad-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="08dad-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="08dad-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="08dad-138">End of client support</span></span><br/>    | <span data-ttu-id="08dad-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="08dad-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="08dad-140">產品</span><span class="sxs-lookup"><span data-stu-id="08dad-140">Product</span></span><br/>                  | <span data-ttu-id="08dad-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="08dad-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="08dad-142">標頭</span><span class="sxs-lookup"><span data-stu-id="08dad-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="08dad-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="08dad-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="08dad-144">IID</span><span class="sxs-lookup"><span data-stu-id="08dad-144">IID</span></span><br/>                      | <span data-ttu-id="08dad-145">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="08dad-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="08dad-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08dad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08dad-147">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="08dad-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

