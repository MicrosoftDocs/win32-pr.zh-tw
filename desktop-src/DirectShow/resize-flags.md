---
description: 如果影片的大小不符合輸出維度，這些旗標會指定如何轉譯影片來源。
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: '調整旗標 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001120"
---
# <a name="resize-flags"></a><span data-ttu-id="eee42-103">調整旗標</span><span class="sxs-lookup"><span data-stu-id="eee42-103">Resize Flags</span></span>

<span data-ttu-id="eee42-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="eee42-104">\[Deprecated.</span></span> <span data-ttu-id="eee42-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="eee42-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="eee42-106">如果影片的大小不符合輸出維度，這些旗標會指定如何轉譯影片來源。</span><span class="sxs-lookup"><span data-stu-id="eee42-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="eee42-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="eee42-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="eee42-108">Description</span><span class="sxs-lookup"><span data-stu-id="eee42-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="eee42-109"><dt>**RESIZEF \_STRETCH**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eee42-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="eee42-110">影像會伸展以符合兩個維度中的目標框架大小，而不會保留長寬比。</span><span class="sxs-lookup"><span data-stu-id="eee42-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="eee42-111"><dt>**RESIZEF \_裁剪**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eee42-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="eee42-112">影像未調整大小。</span><span class="sxs-lookup"><span data-stu-id="eee42-112">The image is not resized.</span></span> <span data-ttu-id="eee42-113">如果影像小於目標框架，周圍區域會是黑色。</span><span class="sxs-lookup"><span data-stu-id="eee42-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="eee42-114">如果影像大於目標框架，則會裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="eee42-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="eee42-115"><dt>**RESIZEF \_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eee42-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="eee42-116">影像會調整大小以配合一個維度的目標框架，同時保留外觀比例。</span><span class="sxs-lookup"><span data-stu-id="eee42-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="eee42-117">如果影像中的寬度和高度比例與目標框架中的比率不符，則會建立黑邊。</span><span class="sxs-lookup"><span data-stu-id="eee42-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="eee42-118"><dt>**RESIZEF \_PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eee42-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="eee42-119">影像會調整大小以填滿整個目標框架，同時保留外觀比例。</span><span class="sxs-lookup"><span data-stu-id="eee42-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="eee42-120">這個模式不會建立黑邊，而是沿著兩側或在頂端和底部裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="eee42-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="eee42-121">備註</span><span class="sxs-lookup"><span data-stu-id="eee42-121">Remarks</span></span>

<span data-ttu-id="eee42-122">下列影像顯示這些旗標的效果。</span><span class="sxs-lookup"><span data-stu-id="eee42-122">The following images show the effects of these flags.</span></span>

![調整旗標](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="eee42-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="eee42-124">Requirements</span></span>



| <span data-ttu-id="eee42-125">需求</span><span class="sxs-lookup"><span data-stu-id="eee42-125">Requirement</span></span> | <span data-ttu-id="eee42-126">值</span><span class="sxs-lookup"><span data-stu-id="eee42-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eee42-127">標頭</span><span class="sxs-lookup"><span data-stu-id="eee42-127">Header</span></span><br/> | <dl> <span data-ttu-id="eee42-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="eee42-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee42-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eee42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee42-130">**IAMTimelineSrc::GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="eee42-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="eee42-131">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="eee42-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




