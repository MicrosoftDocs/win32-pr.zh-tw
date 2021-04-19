---
description: FastRender 方法會使用 BitBlt 或 StretchBlt 函數來繪製影片影像。
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: 'CDrawImage. FastRender 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981121"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="cc71f-103">CDrawImage. FastRender 方法</span><span class="sxs-lookup"><span data-stu-id="cc71f-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="cc71f-104">`FastRender`方法會使用 **BitBlt** 或 **StretchBlt** 函式來繪製影片影像。</span><span class="sxs-lookup"><span data-stu-id="cc71f-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc71f-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc71f-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="cc71f-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc71f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc71f-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="cc71f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="cc71f-108">包含影像之範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="cc71f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc71f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc71f-109">Return value</span></span>

<span data-ttu-id="cc71f-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cc71f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc71f-111">備註</span><span class="sxs-lookup"><span data-stu-id="cc71f-111">Remarks</span></span>

<span data-ttu-id="cc71f-112">[**CDrawImage：:D rawimage**](cdrawimage-drawimage.md)方法會呼叫這個方法，但只有在連接的配置器是 [**CImageAllocator**](cimageallocator.md)物件時才會呼叫。</span><span class="sxs-lookup"><span data-stu-id="cc71f-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="cc71f-113">在此情況下，媒體範例保證是 [**CImageSample**](cimagesample.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="cc71f-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="cc71f-114">**CImageSample** 物件使用 **CreateDIBSection** 函式來配置點陣圖的共用記憶體，讓您可以使用 **BitBlt** 或 **StretchBlt** 來繪製影像。</span><span class="sxs-lookup"><span data-stu-id="cc71f-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="cc71f-115">如果來源和目標矩形完全相符，這個方法會呼叫 **BitBlt** ，否則會呼叫 **StretchBlt** 。</span><span class="sxs-lookup"><span data-stu-id="cc71f-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="cc71f-116">如果篩選器不擁有配置器，則 **DrawImage** 方法會使用 [**CDrawImage：： SlowRender**](cdrawimage-slowrender.md) 來繪製影像。</span><span class="sxs-lookup"><span data-stu-id="cc71f-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc71f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc71f-117">Requirements</span></span>



| <span data-ttu-id="cc71f-118">需求</span><span class="sxs-lookup"><span data-stu-id="cc71f-118">Requirement</span></span> | <span data-ttu-id="cc71f-119">值</span><span class="sxs-lookup"><span data-stu-id="cc71f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc71f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cc71f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cc71f-121"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cc71f-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc71f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc71f-122">Library</span></span><br/> | <dl> <span data-ttu-id="cc71f-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cc71f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc71f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc71f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc71f-125">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="cc71f-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




