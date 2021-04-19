---
description: SlowRender 方法會使用 SetDIBitsToDevice 或 StretchDIBits 函數來繪製影片影像。
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: 'CDrawImage. SlowRender 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998611"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="f7312-103">CDrawImage. SlowRender 方法</span><span class="sxs-lookup"><span data-stu-id="f7312-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="f7312-104">`SlowRender`方法會使用 **SetDIBitsToDevice** 或 **StretchDIBits** 函式來繪製影片影像。</span><span class="sxs-lookup"><span data-stu-id="f7312-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7312-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7312-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="f7312-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7312-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7312-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="f7312-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f7312-108">包含影像之範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f7312-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7312-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7312-109">Return value</span></span>

<span data-ttu-id="f7312-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f7312-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7312-111">備註</span><span class="sxs-lookup"><span data-stu-id="f7312-111">Remarks</span></span>

<span data-ttu-id="f7312-112">如果 [**CDrawImage：： UsingImageAllocator**](cdrawimage-usingimageallocator.md) 傳回 **FALSE**，則 [**CDrawImage：:D rawimage**](cdrawimage-drawimage.md) 方法會使用 `SlowRender` 來繪製影片影像。</span><span class="sxs-lookup"><span data-stu-id="f7312-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="f7312-113">否則，DrawImage 會使用 **FastRender** 方法。</span><span class="sxs-lookup"><span data-stu-id="f7312-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7312-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7312-114">Requirements</span></span>



| <span data-ttu-id="f7312-115">需求</span><span class="sxs-lookup"><span data-stu-id="f7312-115">Requirement</span></span> | <span data-ttu-id="f7312-116">值</span><span class="sxs-lookup"><span data-stu-id="f7312-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7312-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f7312-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f7312-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f7312-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7312-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7312-119">Library</span></span><br/> | <dl> <span data-ttu-id="f7312-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f7312-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7312-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7312-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7312-122">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="f7312-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="f7312-123">**CDrawImage::FastRender**</span><span class="sxs-lookup"><span data-stu-id="f7312-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 




