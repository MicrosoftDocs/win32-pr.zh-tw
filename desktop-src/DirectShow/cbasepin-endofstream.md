---
description: EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會實 IPin：： EndOfStream 方法。 請只對輸入圖釘呼叫這個方法。
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: 'CBasePin. EndOfStream 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996479"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="268f1-105">CBasePin. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="268f1-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="268f1-106">`EndOfStream`方法會通知 pin，不需要任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="268f1-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="268f1-107">這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="268f1-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="268f1-108">請只對輸入圖釘呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="268f1-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="268f1-109">語法</span><span class="sxs-lookup"><span data-stu-id="268f1-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="268f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="268f1-110">Parameters</span></span>

<span data-ttu-id="268f1-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="268f1-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="268f1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="268f1-112">Return value</span></span>

<span data-ttu-id="268f1-113">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="268f1-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="268f1-114">備註</span><span class="sxs-lookup"><span data-stu-id="268f1-114">Remarks</span></span>

<span data-ttu-id="268f1-115">篩選準則應該將下游的結束資料流程通知傳遞至連線篩選的輸入接點。</span><span class="sxs-lookup"><span data-stu-id="268f1-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="268f1-116">如果篩選器是轉譯器，則應該將 [**EC \_ 完成**](ec-complete.md) 事件通知張貼至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="268f1-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="268f1-117">如需詳細資訊，請參閱 [篩選圖形中的](data-flow-in-the-filter-graph.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="268f1-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="268f1-118">在基類中，此方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="268f1-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="268f1-119">衍生類別應該覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="268f1-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="268f1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="268f1-120">Requirements</span></span>



| <span data-ttu-id="268f1-121">需求</span><span class="sxs-lookup"><span data-stu-id="268f1-121">Requirement</span></span> | <span data-ttu-id="268f1-122">值</span><span class="sxs-lookup"><span data-stu-id="268f1-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="268f1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="268f1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="268f1-124"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="268f1-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="268f1-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="268f1-125">Library</span></span><br/> | <dl> <span data-ttu-id="268f1-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="268f1-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268f1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="268f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268f1-128">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="268f1-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




