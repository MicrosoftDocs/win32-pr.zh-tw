---
description: DrawImage 方法會在影片視窗上繪製一個影片畫面。
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: 'CDrawImage. DrawImage 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976041"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="fe6d7-103">CDrawImage. DrawImage 方法</span><span class="sxs-lookup"><span data-stu-id="fe6d7-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="fe6d7-104">`DrawImage`方法會在影片視窗上繪製一個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe6d7-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="fe6d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe6d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6d7-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="fe6d7-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6d7-108">包含影像之範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6d7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe6d7-109">Return value</span></span>

<span data-ttu-id="fe6d7-110">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6d7-111">備註</span><span class="sxs-lookup"><span data-stu-id="fe6d7-111">Remarks</span></span>

<span data-ttu-id="fe6d7-112">這個方法會委派給 [**CDrawImage：： FastRender**](cdrawimage-fastrender.md) 或 [**CDrawImage：： SlowRender**](cdrawimage-slowrender.md)，這取決於篩選準則是否擁有提供範例的配置器。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="fe6d7-113">如果篩選準則擁有配置器，則會保證範例是 [**CImageSample**](cimagesample.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="fe6d7-114">在此情況下，此範例會使用 GDI 所配置的共用記憶體，而且可以使用 **BitBlt** 或 **StretchBlt** 來繪製影像。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="fe6d7-115">否則，必須使用較慢的 **SetDIBitsToDevice** 或 **StretchDIBits** 函數來繪製影像。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="fe6d7-116">在 debug 組建中，此方法會呼叫 **DisplaySampleTimes** ，以在影片影像上繪製範例的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe6d7-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6d7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe6d7-117">Requirements</span></span>



| <span data-ttu-id="fe6d7-118">需求</span><span class="sxs-lookup"><span data-stu-id="fe6d7-118">Requirement</span></span> | <span data-ttu-id="fe6d7-119">值</span><span class="sxs-lookup"><span data-stu-id="fe6d7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6d7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fe6d7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fe6d7-121"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fe6d7-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fe6d7-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe6d7-122">Library</span></span><br/> | <dl> <span data-ttu-id="fe6d7-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fe6d7-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6d7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe6d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6d7-125">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="fe6d7-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="fe6d7-126">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="fe6d7-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




