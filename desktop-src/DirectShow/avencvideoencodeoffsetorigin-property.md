---
description: 指定裁剪矩形的左邊和左上角（如果影片已裁剪）。
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: 'AVEncVideoEncodeOffsetOrigin 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108985"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="9fecf-103">AVEncVideoEncodeOffsetOrigin 屬性</span><span class="sxs-lookup"><span data-stu-id="9fecf-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="9fecf-104">指定裁剪矩形的左邊和左上角（如果影片已裁剪）。</span><span class="sxs-lookup"><span data-stu-id="9fecf-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="9fecf-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9fecf-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9fecf-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="9fecf-106">Data type</span></span>

<span data-ttu-id="9fecf-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="9fecf-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9fecf-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="9fecf-108">Property GUID</span></span>

<span data-ttu-id="9fecf-109">**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**</span><span class="sxs-lookup"><span data-stu-id="9fecf-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="9fecf-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9fecf-110">Property value</span></span>

<span data-ttu-id="9fecf-111">值的上層16位包含輸入框架左邊緣的位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9fecf-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="9fecf-112">較低的16個位包含輸入框架上邊緣的位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9fecf-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fecf-113">備註</span><span class="sxs-lookup"><span data-stu-id="9fecf-113">Remarks</span></span>

<span data-ttu-id="9fecf-114">應用程式可以設定此屬性來裁剪輸入影片。</span><span class="sxs-lookup"><span data-stu-id="9fecf-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="9fecf-115">您可以使用 [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) 屬性來指定裁剪矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="9fecf-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fecf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fecf-116">Requirements</span></span>



| <span data-ttu-id="9fecf-117">需求</span><span class="sxs-lookup"><span data-stu-id="9fecf-117">Requirement</span></span> | <span data-ttu-id="9fecf-118">值</span><span class="sxs-lookup"><span data-stu-id="9fecf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fecf-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fecf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9fecf-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fecf-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9fecf-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fecf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9fecf-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fecf-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9fecf-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9fecf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fecf-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fecf-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fecf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fecf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fecf-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="9fecf-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9fecf-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="9fecf-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




