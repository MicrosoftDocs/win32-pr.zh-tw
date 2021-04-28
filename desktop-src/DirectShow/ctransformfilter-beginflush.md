---
description: CTransformFilter. BeginFlush 方法-BeginFlush 方法開始進行清除作業。
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: 'CTransformFilter. BeginFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085156"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="c40b2-103">CTransformFilter. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="c40b2-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="c40b2-104">`BeginFlush`方法會開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="c40b2-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c40b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c40b2-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="c40b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c40b2-106">Parameters</span></span>

<span data-ttu-id="c40b2-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c40b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c40b2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c40b2-108">Return value</span></span>

<span data-ttu-id="c40b2-109">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c40b2-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c40b2-110">備註</span><span class="sxs-lookup"><span data-stu-id="c40b2-110">Remarks</span></span>

<span data-ttu-id="c40b2-111">在排清作業開始時，輸入釘選的 [**CTransformInputPin：： BeginFlush**](ctransforminputpin-beginflush.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c40b2-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="c40b2-112">這個方法會將 `BeginFlush` 呼叫傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="c40b2-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="c40b2-113">如果衍生類別使用背景工作執行緒來傳遞範例，則在排清作業期間，應該捨棄任何已排入佇列的資料。</span><span class="sxs-lookup"><span data-stu-id="c40b2-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="c40b2-114">可以在 `BeginFlush` 方法中或在 [**EndFlush**](ctransformfilter-endflush.md) 方法中完成。</span><span class="sxs-lookup"><span data-stu-id="c40b2-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="c40b2-115">不過請注意，的呼叫 `BeginFlush` 不會與資料流程處理執行緒同步處理。</span><span class="sxs-lookup"><span data-stu-id="c40b2-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="c40b2-116">如果 `BeginFlush` 方法捨棄佇列資料，則篩選準則必須小心，不要在 `BeginFlush` 和 **EndFlush** 呼叫之間處理任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="c40b2-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="c40b2-117">如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="c40b2-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c40b2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c40b2-118">Requirements</span></span>



| <span data-ttu-id="c40b2-119">需求</span><span class="sxs-lookup"><span data-stu-id="c40b2-119">Requirement</span></span> | <span data-ttu-id="c40b2-120">值</span><span class="sxs-lookup"><span data-stu-id="c40b2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c40b2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c40b2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c40b2-122"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c40b2-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c40b2-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c40b2-123">Library</span></span><br/> | <dl> <span data-ttu-id="c40b2-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c40b2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c40b2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c40b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c40b2-126">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c40b2-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




