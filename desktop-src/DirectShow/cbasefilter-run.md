---
description: Run 方法會執行篩選。 這個方法會實 IMediaFilter：： Run 方法。
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: 'CBaseFilter： Run 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995267"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="2da6d-104">CBaseFilter 方法</span><span class="sxs-lookup"><span data-stu-id="2da6d-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="2da6d-105">`Run`方法會執行篩選。</span><span class="sxs-lookup"><span data-stu-id="2da6d-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="2da6d-106">這個方法會實 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法。</span><span class="sxs-lookup"><span data-stu-id="2da6d-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da6d-107">語法</span><span class="sxs-lookup"><span data-stu-id="2da6d-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="2da6d-108">參數</span><span class="sxs-lookup"><span data-stu-id="2da6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da6d-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="2da6d-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2da6d-110">對應于資料流程時間0的參考時間。</span><span class="sxs-lookup"><span data-stu-id="2da6d-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da6d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2da6d-111">Return value</span></span>

<span data-ttu-id="2da6d-112">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2da6d-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da6d-113">備註</span><span class="sxs-lookup"><span data-stu-id="2da6d-113">Remarks</span></span>

<span data-ttu-id="2da6d-114">如果篩選已停止，則這個方法會藉由呼叫 [**CBaseFilter：:P ause**](cbasefilter-pause.md) 方法來暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="2da6d-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="2da6d-115">然後，它會在每個篩選器的連接釘上呼叫 [**CBasePin：： Run**](cbasepin-run.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2da6d-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="2da6d-116">最後，它會將 [**CBaseFilter：： m \_ state**](cbasefilter-m-state.md) 成員變數設定為 \_ 正在執行狀態。</span><span class="sxs-lookup"><span data-stu-id="2da6d-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="2da6d-117">資料流程時間的計算方式為目前的參考時間減去 *tStart*。</span><span class="sxs-lookup"><span data-stu-id="2da6d-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="2da6d-118">時間戳記為零的媒體範例應該在時間 *tStart* 時轉譯。</span><span class="sxs-lookup"><span data-stu-id="2da6d-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da6d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2da6d-119">Requirements</span></span>



| <span data-ttu-id="2da6d-120">需求</span><span class="sxs-lookup"><span data-stu-id="2da6d-120">Requirement</span></span> | <span data-ttu-id="2da6d-121">值</span><span class="sxs-lookup"><span data-stu-id="2da6d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da6d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2da6d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2da6d-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2da6d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2da6d-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="2da6d-124">Library</span></span><br/> | <dl> <span data-ttu-id="2da6d-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2da6d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da6d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2da6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da6d-127">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="2da6d-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




