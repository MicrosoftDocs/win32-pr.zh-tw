---
description: SetSourcePosition 方法會為影片設定新的來源位置。
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: 'CBaseControlVideo. SetSourcePosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5493779b623108f713f8da252e8696140883395b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984877"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a><span data-ttu-id="838c8-103">CBaseControlVideo. SetSourcePosition 方法</span><span class="sxs-lookup"><span data-stu-id="838c8-103">CBaseControlVideo.SetSourcePosition method</span></span>

<span data-ttu-id="838c8-104">`SetSourcePosition`方法會為影片設定新的來源位置。</span><span class="sxs-lookup"><span data-stu-id="838c8-104">The `SetSourcePosition` method sets a new source position for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="838c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="838c8-105">Syntax</span></span>


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="838c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="838c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838c8-107">*離開*</span><span class="sxs-lookup"><span data-stu-id="838c8-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="838c8-108">新的左座標。</span><span class="sxs-lookup"><span data-stu-id="838c8-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="838c8-109">*前幾個*</span><span class="sxs-lookup"><span data-stu-id="838c8-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="838c8-110">新的上方座標。</span><span class="sxs-lookup"><span data-stu-id="838c8-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="838c8-111">*寬度*</span><span class="sxs-lookup"><span data-stu-id="838c8-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="838c8-112">新寬度。</span><span class="sxs-lookup"><span data-stu-id="838c8-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="838c8-113">*高度*</span><span class="sxs-lookup"><span data-stu-id="838c8-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="838c8-114">新的高度。</span><span class="sxs-lookup"><span data-stu-id="838c8-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838c8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="838c8-115">Return value</span></span>

<span data-ttu-id="838c8-116">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="838c8-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="838c8-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="838c8-117">Return code</span></span>                                                                                           | <span data-ttu-id="838c8-118">Description</span><span class="sxs-lookup"><span data-stu-id="838c8-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="838c8-119"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="838c8-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="838c8-120">失敗。</span><span class="sxs-lookup"><span data-stu-id="838c8-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="838c8-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="838c8-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="838c8-122">無效引數。</span><span class="sxs-lookup"><span data-stu-id="838c8-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="838c8-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="838c8-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="838c8-124">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="838c8-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="838c8-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="838c8-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="838c8-126">成功。</span><span class="sxs-lookup"><span data-stu-id="838c8-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="838c8-127"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="838c8-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="838c8-128">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="838c8-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="838c8-129">備註</span><span class="sxs-lookup"><span data-stu-id="838c8-129">Remarks</span></span>

<span data-ttu-id="838c8-130">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="838c8-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="838c8-131">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="838c8-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="838c8-132">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="838c8-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="838c8-133">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="838c8-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="838c8-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="838c8-134">Requirements</span></span>



| <span data-ttu-id="838c8-135">需求</span><span class="sxs-lookup"><span data-stu-id="838c8-135">Requirement</span></span> | <span data-ttu-id="838c8-136">值</span><span class="sxs-lookup"><span data-stu-id="838c8-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838c8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="838c8-137">Header</span></span><br/>  | <dl> <span data-ttu-id="838c8-138"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="838c8-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="838c8-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="838c8-139">Library</span></span><br/> | <dl> <span data-ttu-id="838c8-140"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="838c8-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="838c8-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="838c8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838c8-142">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="838c8-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




