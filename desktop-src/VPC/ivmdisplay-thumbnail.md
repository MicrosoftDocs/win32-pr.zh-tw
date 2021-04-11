---
title: 'IVMDisplay 縮圖屬性 (VPCCOMInterfaces .h) '
description: '抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。 |IVMDisplay 縮圖屬性 (VPCCOMInterfaces .h) '
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- 縮圖屬性虛擬電腦
- 縮圖屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，縮圖屬性
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945781"
---
# <a name="ivmdisplaythumbnail-property"></a><span data-ttu-id="d2ce2-107">IVMDisplay：：縮圖屬性</span><span class="sxs-lookup"><span data-stu-id="d2ce2-107">IVMDisplay::Thumbnail property</span></span>

<span data-ttu-id="d2ce2-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d2ce2-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d2ce2-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d2ce2-110">抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

<span data-ttu-id="d2ce2-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ce2-112">語法</span><span class="sxs-lookup"><span data-stu-id="d2ce2-112">Syntax</span></span>


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a><span data-ttu-id="d2ce2-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="d2ce2-113">Property value</span></span>

<span data-ttu-id="d2ce2-114">型別 VT \_ ARRAY \| VT variant 的變數 \_ ，其中包含 vt UI4 型別的專案 \_ ，縮圖中的每個圖元都有一個。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-114">A variant of type VT\_ARRAY \| VT\_VARIANT containing entries of type VT\_UI4, one for each pixel in the thumbnail.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d2ce2-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d2ce2-115">Error codes</span></span>



| <span data-ttu-id="d2ce2-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="d2ce2-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d2ce2-117">意義</span><span class="sxs-lookup"><span data-stu-id="d2ce2-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d2ce2-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce2-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d2ce2-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d2ce2-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d2ce2-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d2ce2-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce2-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d2ce2-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-123">An unexpected error has occurred.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d2ce2-124">備註</span><span class="sxs-lookup"><span data-stu-id="d2ce2-124">Remarks</span></span>

<span data-ttu-id="d2ce2-125">這個介面會傳回比 [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md)方法更有效率的縮圖，但可從腳本用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-125">This interface returns the thumbnail less efficiently than the [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) method, but is usable from scripting clients.</span></span> <span data-ttu-id="d2ce2-126">縮圖一律為64圖元寬乘以48圖元高。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-126">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="d2ce2-127">每個圖元都是32位。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-127">Each pixel is 32 bits.</span></span> <span data-ttu-id="d2ce2-128">陣列中的第一個64元素是縮圖中的第一個資料列，下一個64元素是第二個數據列，依此類推。</span><span class="sxs-lookup"><span data-stu-id="d2ce2-128">The first 64 elements in the array is the first row of pixels in the thumbnail, the next 64 elements is the second row, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ce2-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2ce2-129">Requirements</span></span>



| <span data-ttu-id="d2ce2-130">需求</span><span class="sxs-lookup"><span data-stu-id="d2ce2-130">Requirement</span></span> | <span data-ttu-id="d2ce2-131">值</span><span class="sxs-lookup"><span data-stu-id="d2ce2-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ce2-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2ce2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ce2-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2ce2-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2ce2-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2ce2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ce2-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="d2ce2-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d2ce2-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d2ce2-136">End of client support</span></span><br/>    | <span data-ttu-id="d2ce2-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2ce2-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d2ce2-138">產品</span><span class="sxs-lookup"><span data-stu-id="d2ce2-138">Product</span></span><br/>                  | <span data-ttu-id="d2ce2-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d2ce2-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d2ce2-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d2ce2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2ce2-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce2-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d2ce2-142">IID</span><span class="sxs-lookup"><span data-stu-id="d2ce2-142">IID</span></span><br/>                      | <span data-ttu-id="d2ce2-143">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="d2ce2-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d2ce2-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2ce2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ce2-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="d2ce2-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

