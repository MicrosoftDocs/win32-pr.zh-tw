---
description: Get \_ DestinationHeight 方法會抓取目前的目的地矩形高度。
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: 'CBaseControlVideo.get_DestinationHeight 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc4fc63e63adbc42b75ae9a24d1c47e7d985c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992169"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a><span data-ttu-id="5cd61-103">CBaseControlVideo. 取得 \_ DestinationHeight 方法</span><span class="sxs-lookup"><span data-stu-id="5cd61-103">CBaseControlVideo.get\_DestinationHeight method</span></span>

<span data-ttu-id="5cd61-104">方法會抓取 `get_DestinationHeight` 目前的目的地矩形高度。</span><span class="sxs-lookup"><span data-stu-id="5cd61-104">The `get_DestinationHeight` method retrieves the current destination rectangle height.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cd61-105">語法</span><span class="sxs-lookup"><span data-stu-id="5cd61-105">Syntax</span></span>


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5cd61-106">參數</span><span class="sxs-lookup"><span data-stu-id="5cd61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cd61-107">*pDestinationHeight*</span><span class="sxs-lookup"><span data-stu-id="5cd61-107">*pDestinationHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5cd61-108">目的地高度的指標。</span><span class="sxs-lookup"><span data-stu-id="5cd61-108">Pointer to the destination height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cd61-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cd61-109">Return value</span></span>

<span data-ttu-id="5cd61-110">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="5cd61-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="5cd61-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5cd61-111">Return code</span></span>                                                                                           | <span data-ttu-id="5cd61-112">Description</span><span class="sxs-lookup"><span data-stu-id="5cd61-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5cd61-113"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="5cd61-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="5cd61-114">失敗。</span><span class="sxs-lookup"><span data-stu-id="5cd61-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="5cd61-115"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5cd61-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5cd61-116">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="5cd61-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5cd61-117"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="5cd61-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5cd61-118">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="5cd61-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5cd61-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="5cd61-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="5cd61-120">成功。</span><span class="sxs-lookup"><span data-stu-id="5cd61-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="5cd61-121">備註</span><span class="sxs-lookup"><span data-stu-id="5cd61-121">Remarks</span></span>

<span data-ttu-id="5cd61-122">此成員函式會實 [**IBasicVideo：： get \_ DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) 方法。</span><span class="sxs-lookup"><span data-stu-id="5cd61-122">This member function implements the [**IBasicVideo::get\_DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) method.</span></span>

<span data-ttu-id="5cd61-123">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="5cd61-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="5cd61-124">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響它的播放位置。</span><span class="sxs-lookup"><span data-stu-id="5cd61-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where it will be played.</span></span> <span data-ttu-id="5cd61-125">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="5cd61-125">The destination rectangle is relative to the client area of the window that it is playing in.</span></span> <span data-ttu-id="5cd61-126">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="5cd61-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cd61-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cd61-127">Requirements</span></span>



| <span data-ttu-id="5cd61-128">需求</span><span class="sxs-lookup"><span data-stu-id="5cd61-128">Requirement</span></span> | <span data-ttu-id="5cd61-129">值</span><span class="sxs-lookup"><span data-stu-id="5cd61-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd61-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5cd61-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5cd61-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5cd61-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5cd61-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="5cd61-132">Library</span></span><br/> | <dl> <span data-ttu-id="5cd61-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5cd61-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cd61-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cd61-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd61-135">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="5cd61-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




