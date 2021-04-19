---
description: OnDirectRender 方法會收集控制同步處理和品質控制的計時資訊。
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: 'CBaseVideoRenderer. OnDirectRender 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981113"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="c9d7f-103">CBaseVideoRenderer. OnDirectRender 方法</span><span class="sxs-lookup"><span data-stu-id="c9d7f-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="c9d7f-104">**OnDirectRender** 方法會收集控制同步處理和品質控制的計時資訊。</span><span class="sxs-lookup"><span data-stu-id="c9d7f-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d7f-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9d7f-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c9d7f-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9d7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d7f-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c9d7f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d7f-108">媒體範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c9d7f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d7f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9d7f-109">Return value</span></span>

<span data-ttu-id="c9d7f-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c9d7f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9d7f-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9d7f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d7f-112">備註</span><span class="sxs-lookup"><span data-stu-id="c9d7f-112">Remarks</span></span>

<span data-ttu-id="c9d7f-113">呼叫這個方法，而不是 [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) 和 [**OnRenderEnd**](cbasevideorenderer-onrenderend.md)。</span><span class="sxs-lookup"><span data-stu-id="c9d7f-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="c9d7f-114">DirectDraw 影片轉譯器會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c9d7f-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d7f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9d7f-115">Requirements</span></span>



| <span data-ttu-id="c9d7f-116">需求</span><span class="sxs-lookup"><span data-stu-id="c9d7f-116">Requirement</span></span> | <span data-ttu-id="c9d7f-117">值</span><span class="sxs-lookup"><span data-stu-id="c9d7f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d7f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c9d7f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c9d7f-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c9d7f-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9d7f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9d7f-120">Library</span></span><br/> | <dl> <span data-ttu-id="c9d7f-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c9d7f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d7f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9d7f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d7f-123">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="c9d7f-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




