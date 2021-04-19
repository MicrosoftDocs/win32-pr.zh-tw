---
description: SetDefaultDestinationPosition 方法會將轉譯器設定回使用預設的目的地位置， (通常是整個視窗工作區) 。
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: 'CBaseControlVideo. SetDefaultDestinationPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985748"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a><span data-ttu-id="070e6-103">CBaseControlVideo. SetDefaultDestinationPosition 方法</span><span class="sxs-lookup"><span data-stu-id="070e6-103">CBaseControlVideo.SetDefaultDestinationPosition method</span></span>

<span data-ttu-id="070e6-104">方法會將轉譯器 `SetDefaultDestinationPosition` 設定回使用預設的目的地位置， (通常是整個視窗工作區) 。</span><span class="sxs-lookup"><span data-stu-id="070e6-104">The `SetDefaultDestinationPosition` method sets the renderer back to using the default destination position (typically the entire window client area).</span></span>

## <a name="syntax"></a><span data-ttu-id="070e6-105">語法</span><span class="sxs-lookup"><span data-stu-id="070e6-105">Syntax</span></span>


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a><span data-ttu-id="070e6-106">參數</span><span class="sxs-lookup"><span data-stu-id="070e6-106">Parameters</span></span>

<span data-ttu-id="070e6-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="070e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="070e6-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="070e6-108">Return value</span></span>

<span data-ttu-id="070e6-109">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="070e6-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="070e6-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="070e6-110">Return code</span></span>                                                                                           | <span data-ttu-id="070e6-111">Description</span><span class="sxs-lookup"><span data-stu-id="070e6-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="070e6-112"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="070e6-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="070e6-113">失敗。</span><span class="sxs-lookup"><span data-stu-id="070e6-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="070e6-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="070e6-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="070e6-115">成功。</span><span class="sxs-lookup"><span data-stu-id="070e6-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="070e6-116"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="070e6-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="070e6-117">無法執行作業，因為沒有連接的釘選。</span><span class="sxs-lookup"><span data-stu-id="070e6-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="070e6-118">備註</span><span class="sxs-lookup"><span data-stu-id="070e6-118">Remarks</span></span>

<span data-ttu-id="070e6-119">應用程式可以透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面變更影片的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="070e6-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="070e6-120">來源矩形會影響原生影片來源的哪個區段會顯示在顯示上;目的地矩形會影響播放影片時的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="070e6-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="070e6-121">目的地矩形相對於現正播放之視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="070e6-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="070e6-122">視窗的左上角是座標 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="070e6-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="070e6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="070e6-123">Requirements</span></span>



| <span data-ttu-id="070e6-124">需求</span><span class="sxs-lookup"><span data-stu-id="070e6-124">Requirement</span></span> | <span data-ttu-id="070e6-125">值</span><span class="sxs-lookup"><span data-stu-id="070e6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070e6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="070e6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="070e6-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="070e6-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="070e6-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="070e6-128">Library</span></span><br/> | <dl> <span data-ttu-id="070e6-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="070e6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="070e6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="070e6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070e6-131">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="070e6-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




