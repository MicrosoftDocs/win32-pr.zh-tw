---
description: 指定已編碼影片的寬度和高度（如果影片已裁剪）。
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: 'AVEncVideoEncodeDimension 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107001319"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="3cb52-103">AVEncVideoEncodeDimension 屬性</span><span class="sxs-lookup"><span data-stu-id="3cb52-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="3cb52-104">指定已編碼影片的寬度和高度（如果影片已裁剪）。</span><span class="sxs-lookup"><span data-stu-id="3cb52-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="3cb52-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3cb52-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3cb52-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="3cb52-106">Data type</span></span>

<span data-ttu-id="3cb52-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="3cb52-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3cb52-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="3cb52-108">Property GUID</span></span>

<span data-ttu-id="3cb52-109">**CODECAPI \_ AVEncVideoEncodeDimension**</span><span class="sxs-lookup"><span data-stu-id="3cb52-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="3cb52-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="3cb52-110">Property value</span></span>

<span data-ttu-id="3cb52-111">值的上層16位包含寬度（以圖元為單位），而較低的16個位包含高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3cb52-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb52-112">備註</span><span class="sxs-lookup"><span data-stu-id="3cb52-112">Remarks</span></span>

<span data-ttu-id="3cb52-113">應用程式可以設定此屬性來裁剪輸入影片。</span><span class="sxs-lookup"><span data-stu-id="3cb52-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="3cb52-114">指定的大小必須小於輸入影片框架的大小。</span><span class="sxs-lookup"><span data-stu-id="3cb52-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="3cb52-115">您可以使用 [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) 屬性來指定裁剪矩形的左邊和頂端角落。</span><span class="sxs-lookup"><span data-stu-id="3cb52-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="3cb52-116">編碼器可將此屬性作為功能傳回。</span><span class="sxs-lookup"><span data-stu-id="3cb52-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="3cb52-117">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。</span><span class="sxs-lookup"><span data-stu-id="3cb52-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="3cb52-118">針對 UVC 1.5 攝影機編碼器，不支援 [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) 。</span><span class="sxs-lookup"><span data-stu-id="3cb52-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb52-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cb52-119">Requirements</span></span>



| <span data-ttu-id="3cb52-120">需求</span><span class="sxs-lookup"><span data-stu-id="3cb52-120">Requirement</span></span> | <span data-ttu-id="3cb52-121">值</span><span class="sxs-lookup"><span data-stu-id="3cb52-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb52-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cb52-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb52-123">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cb52-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3cb52-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cb52-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb52-125">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cb52-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3cb52-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3cb52-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb52-127"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb52-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb52-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cb52-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb52-129">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="3cb52-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3cb52-130">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="3cb52-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

