---
description: Put \_ DestinationTop 方法會設定目的地矩形的上方座標。
ms.assetid: d18996ac-85f2-4778-b0aa-1bc0c4d5f7d9
title: 'CBaseControlVideo.put_DestinationTop 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c89e4693d424412a43869509e046a5023e76341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995791"
---
# <a name="cbasecontrolvideoput_destinationtop-method"></a><span data-ttu-id="00e13-103">CBaseControlVideo. put \_ DestinationTop 方法</span><span class="sxs-lookup"><span data-stu-id="00e13-103">CBaseControlVideo.put\_DestinationTop method</span></span>

<span data-ttu-id="00e13-104">`put_DestinationTop`方法會設定目的地矩形的上方座標。</span><span class="sxs-lookup"><span data-stu-id="00e13-104">The `put_DestinationTop` method sets the top coordinate of the destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e13-105">語法</span><span class="sxs-lookup"><span data-stu-id="00e13-105">Syntax</span></span>


```C++
HRESULT put_DestinationTop(
   long DestinationTop
);
```



## <a name="parameters"></a><span data-ttu-id="00e13-106">參數</span><span class="sxs-lookup"><span data-stu-id="00e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e13-107">*DestinationTop*</span><span class="sxs-lookup"><span data-stu-id="00e13-107">*DestinationTop*</span></span> 
</dt> <dd>

<span data-ttu-id="00e13-108">目的地矩形的新頂端座標。</span><span class="sxs-lookup"><span data-stu-id="00e13-108">New top coordinate of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e13-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="00e13-109">Return value</span></span>

<span data-ttu-id="00e13-110">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="00e13-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="00e13-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="00e13-111">Return code</span></span>                                                                                           | <span data-ttu-id="00e13-112">Description</span><span class="sxs-lookup"><span data-stu-id="00e13-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00e13-113"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="00e13-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="00e13-114">失敗。</span><span class="sxs-lookup"><span data-stu-id="00e13-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="00e13-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00e13-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="00e13-116">無效引數。</span><span class="sxs-lookup"><span data-stu-id="00e13-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="00e13-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="00e13-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="00e13-118">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="00e13-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="00e13-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="00e13-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="00e13-120">成功。</span><span class="sxs-lookup"><span data-stu-id="00e13-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="00e13-121"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="00e13-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="00e13-122">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="00e13-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="00e13-123">備註</span><span class="sxs-lookup"><span data-stu-id="00e13-123">Remarks</span></span>

<span data-ttu-id="00e13-124">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="00e13-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="00e13-125">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="00e13-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="00e13-126">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="00e13-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="00e13-127">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="00e13-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="00e13-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="00e13-128">Requirements</span></span>



| <span data-ttu-id="00e13-129">需求</span><span class="sxs-lookup"><span data-stu-id="00e13-129">Requirement</span></span> | <span data-ttu-id="00e13-130">值</span><span class="sxs-lookup"><span data-stu-id="00e13-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e13-131">標頭</span><span class="sxs-lookup"><span data-stu-id="00e13-131">Header</span></span><br/>  | <dl> <span data-ttu-id="00e13-132"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="00e13-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00e13-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="00e13-133">Library</span></span><br/> | <dl> <span data-ttu-id="00e13-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="00e13-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e13-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00e13-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e13-136">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="00e13-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




