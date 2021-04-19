---
description: Get \_ SourceLeft 方法會抓取目前來源矩形的左座標。
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: 'CBaseControlVideo.get_SourceLeft 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984045"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="6e357-103">CBaseControlVideo. 取得 \_ SourceLeft 方法</span><span class="sxs-lookup"><span data-stu-id="6e357-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="6e357-104">方法會抓取 `get_SourceLeft` 目前來源矩形的左座標。</span><span class="sxs-lookup"><span data-stu-id="6e357-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e357-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e357-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="6e357-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e357-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e357-107">*pSourceLeft*</span><span class="sxs-lookup"><span data-stu-id="6e357-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="6e357-108">目前來源矩形左方座標的指標。</span><span class="sxs-lookup"><span data-stu-id="6e357-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e357-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e357-109">Return value</span></span>

<span data-ttu-id="6e357-110">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="6e357-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="6e357-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6e357-111">Return code</span></span>                                                                                           | <span data-ttu-id="6e357-112">Description</span><span class="sxs-lookup"><span data-stu-id="6e357-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e357-113"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="6e357-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="6e357-114">失敗。</span><span class="sxs-lookup"><span data-stu-id="6e357-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="6e357-115"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6e357-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="6e357-116">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="6e357-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6e357-117"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="6e357-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6e357-118">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="6e357-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="6e357-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="6e357-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="6e357-120">成功。</span><span class="sxs-lookup"><span data-stu-id="6e357-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6e357-121">備註</span><span class="sxs-lookup"><span data-stu-id="6e357-121">Remarks</span></span>

<span data-ttu-id="6e357-122">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="6e357-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="6e357-123">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="6e357-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="6e357-124">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="6e357-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="6e357-125">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="6e357-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e357-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e357-126">Requirements</span></span>



| <span data-ttu-id="6e357-127">需求</span><span class="sxs-lookup"><span data-stu-id="6e357-127">Requirement</span></span> | <span data-ttu-id="6e357-128">值</span><span class="sxs-lookup"><span data-stu-id="6e357-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e357-129">標頭</span><span class="sxs-lookup"><span data-stu-id="6e357-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6e357-130"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6e357-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6e357-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e357-131">Library</span></span><br/> | <dl> <span data-ttu-id="6e357-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6e357-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e357-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e357-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e357-134">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="6e357-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




