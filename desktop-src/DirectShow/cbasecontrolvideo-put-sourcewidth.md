---
description: Put \_ SourceWidth 方法會設定來源矩形的寬度。
ms.assetid: 0becea4f-e47e-4f64-ab95-0ee333ad48f3
title: 'CBaseControlVideo.put_SourceWidth 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1576389a90db71ee6d371f6e68c44ea39117c05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985548"
---
# <a name="cbasecontrolvideoput_sourcewidth-method"></a><span data-ttu-id="75149-103">CBaseControlVideo. put \_ SourceWidth 方法</span><span class="sxs-lookup"><span data-stu-id="75149-103">CBaseControlVideo.put\_SourceWidth method</span></span>

<span data-ttu-id="75149-104">`put_SourceWidth`方法會設定來源矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="75149-104">The `put_SourceWidth` method sets the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="75149-105">語法</span><span class="sxs-lookup"><span data-stu-id="75149-105">Syntax</span></span>


```C++
HRESULT put_SourceWidth(
   long SourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="75149-106">參數</span><span class="sxs-lookup"><span data-stu-id="75149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75149-107">*SourceWidth*</span><span class="sxs-lookup"><span data-stu-id="75149-107">*SourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="75149-108">來源矩形的新寬度。</span><span class="sxs-lookup"><span data-stu-id="75149-108">New width of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75149-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="75149-109">Return value</span></span>

<span data-ttu-id="75149-110">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="75149-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="75149-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="75149-111">Return code</span></span>                                                                                           | <span data-ttu-id="75149-112">Description</span><span class="sxs-lookup"><span data-stu-id="75149-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75149-113"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="75149-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="75149-114">失敗。</span><span class="sxs-lookup"><span data-stu-id="75149-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="75149-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75149-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="75149-116">無效引數。</span><span class="sxs-lookup"><span data-stu-id="75149-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="75149-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="75149-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="75149-118">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="75149-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="75149-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="75149-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="75149-120">成功。</span><span class="sxs-lookup"><span data-stu-id="75149-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="75149-121"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="75149-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="75149-122">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="75149-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75149-123">備註</span><span class="sxs-lookup"><span data-stu-id="75149-123">Remarks</span></span>

<span data-ttu-id="75149-124">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="75149-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="75149-125">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="75149-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="75149-126">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="75149-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="75149-127">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="75149-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="75149-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="75149-128">Requirements</span></span>



| <span data-ttu-id="75149-129">需求</span><span class="sxs-lookup"><span data-stu-id="75149-129">Requirement</span></span> | <span data-ttu-id="75149-130">值</span><span class="sxs-lookup"><span data-stu-id="75149-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75149-131">標頭</span><span class="sxs-lookup"><span data-stu-id="75149-131">Header</span></span><br/>  | <dl> <span data-ttu-id="75149-132"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="75149-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75149-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="75149-133">Library</span></span><br/> | <dl> <span data-ttu-id="75149-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="75149-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75149-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75149-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75149-136">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="75149-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




