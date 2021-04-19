---
description: Run 方法會通知釘選篩選現在正在執行。
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: 'CBasePin： Run 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984315"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="b5056-103">CBasePin 方法</span><span class="sxs-lookup"><span data-stu-id="b5056-103">CBasePin.Run method</span></span>

<span data-ttu-id="b5056-104">`Run`方法會通知釘選篩選現在正在執行。</span><span class="sxs-lookup"><span data-stu-id="b5056-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5056-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5056-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="b5056-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5056-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="b5056-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b5056-108">傳遞至篩選器 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法的開始時間。</span><span class="sxs-lookup"><span data-stu-id="b5056-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5056-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5056-109">Return value</span></span>

<span data-ttu-id="b5056-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b5056-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5056-111">備註</span><span class="sxs-lookup"><span data-stu-id="b5056-111">Remarks</span></span>

<span data-ttu-id="b5056-112">當篩選從暫停變成執行中時， [**CBaseFilter**](cbasefilter.md) 類別會在所有篩選器的釘選上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b5056-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="b5056-113">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="b5056-113">This method does nothing in the base class.</span></span> <span data-ttu-id="b5056-114">衍生類別可以覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b5056-114">Derived classes can override this method.</span></span> <span data-ttu-id="b5056-115">例如，pin 可能會啟動可傳遞範例的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="b5056-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="b5056-116">除非這個成員函式傳回，否則篩選圖形管理員的內部狀態不會更新，因此請勿從此方法測試狀態。</span><span class="sxs-lookup"><span data-stu-id="b5056-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5056-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5056-117">Requirements</span></span>



| <span data-ttu-id="b5056-118">需求</span><span class="sxs-lookup"><span data-stu-id="b5056-118">Requirement</span></span> | <span data-ttu-id="b5056-119">值</span><span class="sxs-lookup"><span data-stu-id="b5056-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5056-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b5056-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b5056-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b5056-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b5056-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5056-122">Library</span></span><br/> | <dl> <span data-ttu-id="b5056-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b5056-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5056-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5056-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5056-125">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="b5056-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




