---
description: ScheduleSample 方法會排定轉譯的範例。
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: 'CBaseRenderer. ScheduleSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980186"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="a0a19-103">CBaseRenderer. ScheduleSample 方法</span><span class="sxs-lookup"><span data-stu-id="a0a19-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="a0a19-104">方法會排定轉譯的 `ScheduleSample` 範例。</span><span class="sxs-lookup"><span data-stu-id="a0a19-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a19-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0a19-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="a0a19-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a19-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="a0a19-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a0a19-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a0a19-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a19-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0a19-109">Return value</span></span>

<span data-ttu-id="a0a19-110">如果已排程範例，則傳回 **TRUE** ; 如果已卸載樣本，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a0a19-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a19-111">備註</span><span class="sxs-lookup"><span data-stu-id="a0a19-111">Remarks</span></span>

<span data-ttu-id="a0a19-112">這個方法會先判斷是否應該立即轉譯範例、在未來轉譯或卸載範例。</span><span class="sxs-lookup"><span data-stu-id="a0a19-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="a0a19-113"> (這麼做，它會呼叫 [**CBaseRenderer：： GetSampleTimes**](cbaserenderer-getsampletimes.md) 方法。 ) 如果應該立即轉譯範例，則方法會表示 [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a0a19-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="a0a19-114">如果未來應轉譯此範例，則方法會呼叫 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法來進行排程。</span><span class="sxs-lookup"><span data-stu-id="a0a19-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a19-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0a19-115">Requirements</span></span>



| <span data-ttu-id="a0a19-116">需求</span><span class="sxs-lookup"><span data-stu-id="a0a19-116">Requirement</span></span> | <span data-ttu-id="a0a19-117">值</span><span class="sxs-lookup"><span data-stu-id="a0a19-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a19-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a0a19-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a0a19-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a0a19-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0a19-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="a0a19-120">Library</span></span><br/> | <dl> <span data-ttu-id="a0a19-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a0a19-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a19-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0a19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a19-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="a0a19-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




