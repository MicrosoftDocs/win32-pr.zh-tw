---
description: 預設介面 stride，適用于未壓縮的影片媒體類型。 Stride 是從一個圖元到下一個資料列所需的位元組數目。
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: 'MF_MT_DEFAULT_STRIDE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191886"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="283b9-104">MF \_ MT \_ 預設 \_ STRIDE 屬性</span><span class="sxs-lookup"><span data-stu-id="283b9-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="283b9-105">預設介面 stride，適用于未壓縮的影片媒體類型。</span><span class="sxs-lookup"><span data-stu-id="283b9-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="283b9-106">Stride 是從一個圖元到下一個資料列所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="283b9-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="283b9-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="283b9-107">Data type</span></span>

<span data-ttu-id="283b9-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="283b9-108">**UINT32**</span></span>

<span data-ttu-id="283b9-109">視為 **INT32** 值。</span><span class="sxs-lookup"><span data-stu-id="283b9-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="283b9-110">備註</span><span class="sxs-lookup"><span data-stu-id="283b9-110">Remarks</span></span>

<span data-ttu-id="283b9-111">屬性值會儲存為 **UINT32**，但應轉換成32位帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="283b9-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="283b9-112">Stride 可以是負數。</span><span class="sxs-lookup"><span data-stu-id="283b9-112">Stride can be negative.</span></span>

<span data-ttu-id="283b9-113">由上而下的影像而言，Stride 是正面的，而最下層的影像則為負數。</span><span class="sxs-lookup"><span data-stu-id="283b9-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="283b9-114">這個屬性會為記憶體中的影像的 *連續* 表示提供跨距，也就是在每個資料列之後，不含額外填補位元組的標記法。</span><span class="sxs-lookup"><span data-stu-id="283b9-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="283b9-115">如果媒體緩衝區支援 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面，請使用 [**IMF2DBuffer：： Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) 方法來取得介面的實際跨距，其中可能包含額外的填補位元組。</span><span class="sxs-lookup"><span data-stu-id="283b9-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="283b9-116">如需 surface stride 的詳細資訊，請參閱 [影像 stride](image-stride.md)。</span><span class="sxs-lookup"><span data-stu-id="283b9-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="283b9-117">如需如何計算預設 stride 的範例，請參閱 [未壓縮的視訊緩衝區](uncompressed-video-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="283b9-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="283b9-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="283b9-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="283b9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="283b9-119">Requirements</span></span>



| <span data-ttu-id="283b9-120">需求</span><span class="sxs-lookup"><span data-stu-id="283b9-120">Requirement</span></span> | <span data-ttu-id="283b9-121">值</span><span class="sxs-lookup"><span data-stu-id="283b9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="283b9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="283b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="283b9-123">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="283b9-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="283b9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="283b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="283b9-125">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="283b9-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="283b9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="283b9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="283b9-127"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="283b9-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="283b9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="283b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283b9-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="283b9-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="283b9-130">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="283b9-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="283b9-131">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="283b9-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="283b9-132">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="283b9-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="283b9-133">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="283b9-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="283b9-134">影像 Stride</span><span class="sxs-lookup"><span data-stu-id="283b9-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




