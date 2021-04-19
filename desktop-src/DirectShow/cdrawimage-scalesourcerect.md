---
description: 如果原生影片大小和媒體類型格式之間有差異，則 ScaleSourceRect 方法會調整矩形。
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: 'CDrawImage. ScaleSourceRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977625"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="dcc3b-103">CDrawImage. ScaleSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="dcc3b-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="dcc3b-104">`ScaleSourceRect`如果原生影片大小和媒體類型格式之間有差異，則此方法會調整矩形。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc3b-105">語法</span><span class="sxs-lookup"><span data-stu-id="dcc3b-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="dcc3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="dcc3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc3b-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="dcc3b-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="dcc3b-108">未縮放矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc3b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcc3b-109">Return value</span></span>

<span data-ttu-id="dcc3b-110">傳回縮放的矩形。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc3b-111">備註</span><span class="sxs-lookup"><span data-stu-id="dcc3b-111">Remarks</span></span>

<span data-ttu-id="dcc3b-112">在 **CDrawImage** 類別中，此方法會在沒有任何變更的情況下傳回 *pSource* 。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="dcc3b-113">如果篩選器會延伸傳入的影片影像，您可以覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="dcc3b-114">例如，原生影片大小可能是 320 240，但輸入釘選上的媒體類型可能是 640 480。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="dcc3b-115">在這種情況下，篩選準則必須以2的因數調整來源矩形。</span><span class="sxs-lookup"><span data-stu-id="dcc3b-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc3b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcc3b-116">Requirements</span></span>



| <span data-ttu-id="dcc3b-117">需求</span><span class="sxs-lookup"><span data-stu-id="dcc3b-117">Requirement</span></span> | <span data-ttu-id="dcc3b-118">值</span><span class="sxs-lookup"><span data-stu-id="dcc3b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc3b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="dcc3b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dcc3b-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dcc3b-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcc3b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcc3b-121">Library</span></span><br/> | <dl> <span data-ttu-id="dcc3b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dcc3b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcc3b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcc3b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc3b-124">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="dcc3b-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




