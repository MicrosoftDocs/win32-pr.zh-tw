---
description: GetSourcePosition 方法會在一個不可部分完成的作業中，捕獲來源矩形的位置和維度。
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: 'CBaseControlVideo. GetSourcePosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991047"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="d36de-103">CBaseControlVideo. GetSourcePosition 方法</span><span class="sxs-lookup"><span data-stu-id="d36de-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="d36de-104">方法會在一個不可部分完成的作業 `GetSourcePosition` 中，捕獲來源矩形的位置和維度。</span><span class="sxs-lookup"><span data-stu-id="d36de-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36de-105">語法</span><span class="sxs-lookup"><span data-stu-id="d36de-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="d36de-106">參數</span><span class="sxs-lookup"><span data-stu-id="d36de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36de-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="d36de-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="d36de-108">來源矩形左方座標的指標。</span><span class="sxs-lookup"><span data-stu-id="d36de-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d36de-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="d36de-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="d36de-110">來源矩形的上方座標指標。</span><span class="sxs-lookup"><span data-stu-id="d36de-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d36de-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="d36de-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="d36de-112">來源矩形的寬度指標。</span><span class="sxs-lookup"><span data-stu-id="d36de-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d36de-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="d36de-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="d36de-114">來源矩形高度的指標。</span><span class="sxs-lookup"><span data-stu-id="d36de-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36de-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d36de-115">Return value</span></span>

<span data-ttu-id="d36de-116">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="d36de-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="d36de-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d36de-117">Return code</span></span>                                                                                           | <span data-ttu-id="d36de-118">Description</span><span class="sxs-lookup"><span data-stu-id="d36de-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d36de-119"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d36de-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="d36de-120">失敗。</span><span class="sxs-lookup"><span data-stu-id="d36de-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d36de-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d36de-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="d36de-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="d36de-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d36de-123"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="d36de-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d36de-124">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="d36de-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d36de-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="d36de-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="d36de-126">成功。</span><span class="sxs-lookup"><span data-stu-id="d36de-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d36de-127">備註</span><span class="sxs-lookup"><span data-stu-id="d36de-127">Remarks</span></span>

<span data-ttu-id="d36de-128">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="d36de-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="d36de-129">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="d36de-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="d36de-130">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="d36de-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="d36de-131">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="d36de-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="d36de-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d36de-132">Requirements</span></span>



| <span data-ttu-id="d36de-133">需求</span><span class="sxs-lookup"><span data-stu-id="d36de-133">Requirement</span></span> | <span data-ttu-id="d36de-134">值</span><span class="sxs-lookup"><span data-stu-id="d36de-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d36de-135">標頭</span><span class="sxs-lookup"><span data-stu-id="d36de-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d36de-136"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d36de-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d36de-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="d36de-137">Library</span></span><br/> | <dl> <span data-ttu-id="d36de-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d36de-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d36de-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d36de-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d36de-140">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="d36de-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




