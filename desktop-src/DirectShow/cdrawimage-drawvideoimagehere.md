---
description: DrawVideoImageHere 方法會從媒體範例將影像繪製到指定的裝置內容。
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: 'CDrawImage. DrawVideoImageHere 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989784"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="ec7b8-103">CDrawImage. DrawVideoImageHere 方法</span><span class="sxs-lookup"><span data-stu-id="ec7b8-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="ec7b8-104">`DrawVideoImageHere`方法會從媒體範例將影像繪製到指定的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="ec7b8-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="ec7b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec7b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec7b8-107">*hdc*</span><span class="sxs-lookup"><span data-stu-id="ec7b8-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7b8-108">裝置內容的控制碼，將會在其中進行繪製。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="ec7b8-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="ec7b8-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7b8-110">包含影像之範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="ec7b8-111">*lprcSrc*</span><span class="sxs-lookup"><span data-stu-id="ec7b8-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7b8-112">要用於繪圖的來源矩形指標。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="ec7b8-113">如果是 **Null**，則會使用 [**CDrawImage：： m \_ SourceRect**](cdrawimage-m-sourcerect.md) 中的矩形。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="ec7b8-114">*lprcDst*</span><span class="sxs-lookup"><span data-stu-id="ec7b8-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="ec7b8-115">要用於繪圖的目標矩形指標。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="ec7b8-116">如果是 **Null**，則會使用 [**CDrawImage：： m \_ TargetRect**](cdrawimage-m-targetrect.md) 中的矩形。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec7b8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec7b8-117">Return value</span></span>

<span data-ttu-id="ec7b8-118">如果成功， **則傳回 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ec7b8-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7b8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec7b8-119">Requirements</span></span>



| <span data-ttu-id="ec7b8-120">需求</span><span class="sxs-lookup"><span data-stu-id="ec7b8-120">Requirement</span></span> | <span data-ttu-id="ec7b8-121">值</span><span class="sxs-lookup"><span data-stu-id="ec7b8-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7b8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ec7b8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ec7b8-123"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ec7b8-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec7b8-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec7b8-124">Library</span></span><br/> | <dl> <span data-ttu-id="ec7b8-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ec7b8-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7b8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec7b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7b8-127">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="ec7b8-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




