---
description: Get \_ SourceTop 方法會抓取目前來源矩形的上方座標。
ms.assetid: 78dbd1e6-f591-487e-b9fe-fcbda55f5338
title: 'CBaseControlVideo.get_SourceTop 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1c2a2a90b441571a23bfa4210002b352e388a98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993330"
---
# <a name="cbasecontrolvideoget_sourcetop-method"></a><span data-ttu-id="2007a-103">CBaseControlVideo. 取得 \_ SourceTop 方法</span><span class="sxs-lookup"><span data-stu-id="2007a-103">CBaseControlVideo.get\_SourceTop method</span></span>

<span data-ttu-id="2007a-104">方法會抓取 `get_SourceTop` 目前來源矩形的上方座標。</span><span class="sxs-lookup"><span data-stu-id="2007a-104">The `get_SourceTop` method retrieves the top coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="2007a-105">語法</span><span class="sxs-lookup"><span data-stu-id="2007a-105">Syntax</span></span>


```C++
HRESULT get_SourceTop(
   long *pSourceTop
);
```



## <a name="parameters"></a><span data-ttu-id="2007a-106">參數</span><span class="sxs-lookup"><span data-stu-id="2007a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2007a-107">*pSourceTop*</span><span class="sxs-lookup"><span data-stu-id="2007a-107">*pSourceTop*</span></span> 
</dt> <dd>

<span data-ttu-id="2007a-108">來源矩形的上方座標指標。</span><span class="sxs-lookup"><span data-stu-id="2007a-108">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2007a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2007a-109">Return value</span></span>

<span data-ttu-id="2007a-110">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="2007a-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="2007a-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2007a-111">Return code</span></span>                                                                                           | <span data-ttu-id="2007a-112">Description</span><span class="sxs-lookup"><span data-stu-id="2007a-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2007a-113"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="2007a-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="2007a-114">失敗。</span><span class="sxs-lookup"><span data-stu-id="2007a-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="2007a-115"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2007a-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="2007a-116">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="2007a-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2007a-117"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="2007a-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2007a-118">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="2007a-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="2007a-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="2007a-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="2007a-120">成功。</span><span class="sxs-lookup"><span data-stu-id="2007a-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="2007a-121">備註</span><span class="sxs-lookup"><span data-stu-id="2007a-121">Remarks</span></span>

<span data-ttu-id="2007a-122">此成員函式會實 [**IBasicVideo：： get \_ SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) 方法。</span><span class="sxs-lookup"><span data-stu-id="2007a-122">This member function implements the [**IBasicVideo::get\_SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) method.</span></span>

<span data-ttu-id="2007a-123">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="2007a-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="2007a-124">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="2007a-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="2007a-125">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="2007a-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="2007a-126">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="2007a-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="2007a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2007a-127">Requirements</span></span>



| <span data-ttu-id="2007a-128">需求</span><span class="sxs-lookup"><span data-stu-id="2007a-128">Requirement</span></span> | <span data-ttu-id="2007a-129">值</span><span class="sxs-lookup"><span data-stu-id="2007a-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2007a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2007a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2007a-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2007a-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2007a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="2007a-132">Library</span></span><br/> | <dl> <span data-ttu-id="2007a-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2007a-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2007a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2007a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2007a-135">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="2007a-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




