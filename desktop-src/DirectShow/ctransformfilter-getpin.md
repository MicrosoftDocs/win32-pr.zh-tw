---
description: GetPin 方法會抓取 pin。
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: 'CTransformFilter. GetPin 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979514"
---
# <a name="ctransformfiltergetpin-method"></a><span data-ttu-id="524fb-103">CTransformFilter. GetPin 方法</span><span class="sxs-lookup"><span data-stu-id="524fb-103">CTransformFilter.GetPin method</span></span>

<span data-ttu-id="524fb-104">方法會抓取 `GetPin` pin。</span><span class="sxs-lookup"><span data-stu-id="524fb-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="524fb-105">語法</span><span class="sxs-lookup"><span data-stu-id="524fb-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="524fb-106">參數</span><span class="sxs-lookup"><span data-stu-id="524fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="524fb-107">*n*</span><span class="sxs-lookup"><span data-stu-id="524fb-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="524fb-108">指定之 pin 的編號，從零開始編制索引。</span><span class="sxs-lookup"><span data-stu-id="524fb-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="524fb-109">在此篩選準則中，pin 0 是輸入 pin，而 pin 1 是輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="524fb-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="524fb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="524fb-110">Return value</span></span>

<span data-ttu-id="524fb-111">傳回 [**CBasePin**](cbasepin.md) 物件的指標，該物件會執行釘選，如果方法失敗，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="524fb-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="524fb-112">備註</span><span class="sxs-lookup"><span data-stu-id="524fb-112">Remarks</span></span>

<span data-ttu-id="524fb-113">這個方法會實作為純虛擬 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="524fb-113">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span> <span data-ttu-id="524fb-114">第一次呼叫方法時，它會建立兩個圖釘。</span><span class="sxs-lookup"><span data-stu-id="524fb-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="524fb-115">這個方法不會遞增傳回的釘選上的參考計數，因此傳回的 pin 沒有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="524fb-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="524fb-116">如果呼叫端需要保留 pin 的參考，則應該在 pin 上呼叫 **IUnknown：： AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="524fb-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="524fb-117">如果篩選使用預設的 [**CTransformInputPin**](ctransforminputpin.md) 和 [**CTransformOutputPin**](ctransformoutputpin.md) 釘選，您可能不需要覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="524fb-117">If the filter uses the default [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="524fb-118">但是，如果篩選使用擴充這些類別的釘選，您必須覆寫這個方法以建立該類型的釘選。</span><span class="sxs-lookup"><span data-stu-id="524fb-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="524fb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="524fb-119">Requirements</span></span>



| <span data-ttu-id="524fb-120">需求</span><span class="sxs-lookup"><span data-stu-id="524fb-120">Requirement</span></span> | <span data-ttu-id="524fb-121">值</span><span class="sxs-lookup"><span data-stu-id="524fb-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="524fb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="524fb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="524fb-123"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="524fb-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="524fb-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="524fb-124">Library</span></span><br/> | <dl> <span data-ttu-id="524fb-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="524fb-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="524fb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="524fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524fb-127">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="524fb-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




