---
title: 'IVMDisplay _GenerateThumbnail 方法 (VPCCOMInterfaces .h) '
description: '抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。 |IVMDisplay _GenerateThumbnail 方法 (VPCCOMInterfaces .h) '
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- _GenerateThumbnail 方法 Virtual PC
- _GenerateThumbnail 方法 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，_GenerateThumbnail 方法
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981790"
---
# <a name="ivmdisplay_generatethumbnail-method"></a><span data-ttu-id="50016-107">IVMDisplay：： \_ GenerateThumbnail 方法</span><span class="sxs-lookup"><span data-stu-id="50016-107">IVMDisplay::\_GenerateThumbnail method</span></span>

<span data-ttu-id="50016-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="50016-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="50016-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="50016-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="50016-110">抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="50016-110">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="50016-111">語法</span><span class="sxs-lookup"><span data-stu-id="50016-111">Syntax</span></span>


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a><span data-ttu-id="50016-112">參數</span><span class="sxs-lookup"><span data-stu-id="50016-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50016-113">*thumbnailImage* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="50016-113">*thumbnailImage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50016-114">圖元的陣列，表示虛擬機器畫面的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="50016-114">The array of pixels representing a thumbnail image of the virtual machine's screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50016-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="50016-115">Return value</span></span>

<span data-ttu-id="50016-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="50016-116">This method can return one of these values.</span></span>



| <span data-ttu-id="50016-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="50016-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="50016-118">Description</span><span class="sxs-lookup"><span data-stu-id="50016-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="50016-119"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50016-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="50016-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="50016-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="50016-121"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="50016-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="50016-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="50016-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="50016-123"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="50016-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="50016-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="50016-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50016-125">備註</span><span class="sxs-lookup"><span data-stu-id="50016-125">Remarks</span></span>

<span data-ttu-id="50016-126">此介面會比 [**縮圖**](ivmdisplay-thumbnail.md) 屬性更有效率地傳回縮圖，但無法從腳本用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="50016-126">This interface returns the thumbnail more efficiently than the [**Thumbnail**](ivmdisplay-thumbnail.md) property, but is not usable from scripting clients.</span></span> <span data-ttu-id="50016-127">縮圖一律為64圖元寬乘以48圖元高。</span><span class="sxs-lookup"><span data-stu-id="50016-127">The thumbnail is always 64 pixels wide by 48 pixels high.</span></span> <span data-ttu-id="50016-128">每個圖元都是32位，其中的前8個位代表圖元的藍色值，下8個位代表圖元的綠色值，而下一個8位代表圖元的紅色值。</span><span class="sxs-lookup"><span data-stu-id="50016-128">Each pixel is 32 bits, where the upper 8 bits represent the blue value of the pixel, the next 8 bits represent the green value of the pixel, and the next 8 bits represent the red value of the pixel.</span></span> <span data-ttu-id="50016-129">陣列中的第一個64元素是縮圖的第一個資料列，下一個64元素是第二個數據列，依此類推。</span><span class="sxs-lookup"><span data-stu-id="50016-129">The first 64 elements in the array is the first row of the thumbnail, the next 64 elements is the second row, and so on.</span></span> <span data-ttu-id="50016-130">這個方法會傳回靜態的圖元陣列，這比傳回 **VARIANT** 值的 **SAFEARRAY** 更有效率，但與腳本用戶端不相容。</span><span class="sxs-lookup"><span data-stu-id="50016-130">This method returns a static array of pixels, which is more efficient than returning a **SAFEARRAY** of **VARIANT** values, but is not compatible with scripting clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="50016-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="50016-131">Requirements</span></span>



| <span data-ttu-id="50016-132">需求</span><span class="sxs-lookup"><span data-stu-id="50016-132">Requirement</span></span> | <span data-ttu-id="50016-133">值</span><span class="sxs-lookup"><span data-stu-id="50016-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50016-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50016-134">Minimum supported client</span></span><br/> | <span data-ttu-id="50016-135">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50016-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50016-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50016-136">Minimum supported server</span></span><br/> | <span data-ttu-id="50016-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="50016-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="50016-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="50016-138">End of client support</span></span><br/>    | <span data-ttu-id="50016-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50016-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50016-140">產品</span><span class="sxs-lookup"><span data-stu-id="50016-140">Product</span></span><br/>                  | <span data-ttu-id="50016-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="50016-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="50016-142">標頭</span><span class="sxs-lookup"><span data-stu-id="50016-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="50016-143"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="50016-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="50016-144">IID</span><span class="sxs-lookup"><span data-stu-id="50016-144">IID</span></span><br/>                      | <span data-ttu-id="50016-145">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="50016-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="50016-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50016-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50016-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="50016-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

