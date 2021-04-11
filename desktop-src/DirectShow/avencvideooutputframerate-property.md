---
description: 指定編碼器輸出資料流程的畫面播放速率（以每秒畫面格數為單位）。
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: 'AVEncVideoOutputFrameRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687792"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="d01d0-103">AVEncVideoOutputFrameRate 屬性</span><span class="sxs-lookup"><span data-stu-id="d01d0-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="d01d0-104">指定編碼器輸出資料流程的畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d01d0-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="d01d0-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d01d0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d01d0-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="d01d0-106">Data type</span></span>

<span data-ttu-id="d01d0-107">**UINT64** (**VT \_ UI8**) </span><span class="sxs-lookup"><span data-stu-id="d01d0-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d01d0-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="d01d0-108">Property GUID</span></span>

<span data-ttu-id="d01d0-109">**CODECAPI \_ AVEncVideoOutputFrameRate**</span><span class="sxs-lookup"><span data-stu-id="d01d0-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="d01d0-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d01d0-110">Property value</span></span>

<span data-ttu-id="d01d0-111">這個屬性的值是定義畫面播放速率的比率。</span><span class="sxs-lookup"><span data-stu-id="d01d0-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="d01d0-112">上方的32位包含分子，而較低的32位則包含分母。</span><span class="sxs-lookup"><span data-stu-id="d01d0-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="d01d0-113">下表顯示一般畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d01d0-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="d01d0-114">畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="d01d0-114">Frame rate</span></span> | <span data-ttu-id="d01d0-115">外觀比例</span><span class="sxs-lookup"><span data-stu-id="d01d0-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="d01d0-116">23.97</span><span class="sxs-lookup"><span data-stu-id="d01d0-116">23.97</span></span>      | <span data-ttu-id="d01d0-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="d01d0-117">24000/1001</span></span> |
| <span data-ttu-id="d01d0-118">24</span><span class="sxs-lookup"><span data-stu-id="d01d0-118">24</span></span>         | <span data-ttu-id="d01d0-119">24/1</span><span class="sxs-lookup"><span data-stu-id="d01d0-119">24/1</span></span>       |
| <span data-ttu-id="d01d0-120">25</span><span class="sxs-lookup"><span data-stu-id="d01d0-120">25</span></span>         | <span data-ttu-id="d01d0-121">25/1</span><span class="sxs-lookup"><span data-stu-id="d01d0-121">25/1</span></span>       |
| <span data-ttu-id="d01d0-122">29.97</span><span class="sxs-lookup"><span data-stu-id="d01d0-122">29.97</span></span>      | <span data-ttu-id="d01d0-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="d01d0-123">30000/1001</span></span> |
| <span data-ttu-id="d01d0-124">30</span><span class="sxs-lookup"><span data-stu-id="d01d0-124">30</span></span>         | <span data-ttu-id="d01d0-125">30/1</span><span class="sxs-lookup"><span data-stu-id="d01d0-125">30/1</span></span>       |
| <span data-ttu-id="d01d0-126">50</span><span class="sxs-lookup"><span data-stu-id="d01d0-126">50</span></span>         | <span data-ttu-id="d01d0-127">50/1</span><span class="sxs-lookup"><span data-stu-id="d01d0-127">50/1</span></span>       |
| <span data-ttu-id="d01d0-128">59.94</span><span class="sxs-lookup"><span data-stu-id="d01d0-128">59.94</span></span>      | <span data-ttu-id="d01d0-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="d01d0-129">60000/1001</span></span> |
| <span data-ttu-id="d01d0-130">60</span><span class="sxs-lookup"><span data-stu-id="d01d0-130">60</span></span>         | <span data-ttu-id="d01d0-131">60/1</span><span class="sxs-lookup"><span data-stu-id="d01d0-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="d01d0-132">備註</span><span class="sxs-lookup"><span data-stu-id="d01d0-132">Remarks</span></span>

<span data-ttu-id="d01d0-133">應用程式可以設定此屬性來指定輸出畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="d01d0-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="d01d0-134">編碼器也可以將此屬性作為功能傳回。</span><span class="sxs-lookup"><span data-stu-id="d01d0-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="d01d0-135">根據編碼器，值可能會限制為輸入畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="d01d0-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="d01d0-136">如果沒有，則編碼器能夠在內部轉換畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="d01d0-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="d01d0-137">請參閱 [**AVEncVideoOutputFrameRateConversion 屬性**](avencvideooutputframerateconversion-property.md)。</span><span class="sxs-lookup"><span data-stu-id="d01d0-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="d01d0-138">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。</span><span class="sxs-lookup"><span data-stu-id="d01d0-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="d01d0-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="d01d0-139">Requirements</span></span>



| <span data-ttu-id="d01d0-140">需求</span><span class="sxs-lookup"><span data-stu-id="d01d0-140">Requirement</span></span> | <span data-ttu-id="d01d0-141">值</span><span class="sxs-lookup"><span data-stu-id="d01d0-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d01d0-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d01d0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d01d0-143">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d01d0-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d01d0-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d01d0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d01d0-145">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d01d0-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d01d0-146">標頭</span><span class="sxs-lookup"><span data-stu-id="d01d0-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d01d0-147"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d01d0-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01d0-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d01d0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01d0-149">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="d01d0-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d01d0-150">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="d01d0-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

