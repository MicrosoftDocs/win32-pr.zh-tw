---
description: GetDestinationPosition 方法會在一個不可部分完成的作業中抓取目的地矩形。
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: 'CBaseControlVideo. GetDestinationPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978527"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a><span data-ttu-id="9fb5a-103">CBaseControlVideo. GetDestinationPosition 方法</span><span class="sxs-lookup"><span data-stu-id="9fb5a-103">CBaseControlVideo.GetDestinationPosition method</span></span>

<span data-ttu-id="9fb5a-104">`GetDestinationPosition`方法會在一個不可部分完成的作業中抓取目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-104">The `GetDestinationPosition` method retrieves the destination rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb5a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fb5a-105">Syntax</span></span>


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="9fb5a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fb5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb5a-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="9fb5a-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb5a-108">目的地矩形左座標的指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5a-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="9fb5a-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb5a-110">目的地矩形的上方座標指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-110">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5a-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="9fb5a-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb5a-112">目的地矩形的寬度指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-112">Pointer to the width of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="9fb5a-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="9fb5a-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb5a-114">目的地矩形高度的指標。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-114">Pointer to the height of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb5a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fb5a-115">Return value</span></span>

<span data-ttu-id="9fb5a-116">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="9fb5a-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9fb5a-117">Return code</span></span>                                                                                           | <span data-ttu-id="9fb5a-118">Description</span><span class="sxs-lookup"><span data-stu-id="9fb5a-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9fb5a-119"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="9fb5a-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="9fb5a-120">失敗。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="9fb5a-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="9fb5a-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="9fb5a-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="9fb5a-123"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="9fb5a-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9fb5a-124">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="9fb5a-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="9fb5a-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="9fb5a-126">成功。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="9fb5a-127">備註</span><span class="sxs-lookup"><span data-stu-id="9fb5a-127">Remarks</span></span>

<span data-ttu-id="9fb5a-128">這個成員函式可以用來取代對 [**CBaseControlVideo：： get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)、 [**CBaseControlVideo：： get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)、 [**CBaseControlVideo：： get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)和 [**CBaseControlVideo：： get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) 成員函式的個別呼叫。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-128">This member function can be used in place of separate calls to the [**CBaseControlVideo::get\_DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get\_DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get\_DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md), and [**CBaseControlVideo::get\_DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) member functions.</span></span> <span data-ttu-id="9fb5a-129">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-129">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="9fb5a-130">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-130">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="9fb5a-131">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-131">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="9fb5a-132">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="9fb5a-132">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb5a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fb5a-133">Requirements</span></span>



| <span data-ttu-id="9fb5a-134">需求</span><span class="sxs-lookup"><span data-stu-id="9fb5a-134">Requirement</span></span> | <span data-ttu-id="9fb5a-135">值</span><span class="sxs-lookup"><span data-stu-id="9fb5a-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb5a-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9fb5a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9fb5a-137"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9fb5a-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9fb5a-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="9fb5a-138">Library</span></span><br/> | <dl> <span data-ttu-id="9fb5a-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9fb5a-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb5a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fb5a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb5a-141">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="9fb5a-141">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




