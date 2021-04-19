---
description: BeginFlush 方法會通知擁有篩選以排清下游篩選。 衍生的類別必須執行此方法。
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: 'CPullPin. BeginFlush 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989831"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="c5ea1-104">CPullPin. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="c5ea1-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="c5ea1-105">`BeginFlush`方法會通知擁有篩選以排清下游篩選。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="c5ea1-106">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ea1-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5ea1-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="c5ea1-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5ea1-108">Parameters</span></span>

<span data-ttu-id="c5ea1-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5ea1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5ea1-110">Return value</span></span>

<span data-ttu-id="c5ea1-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ea1-112">備註</span><span class="sxs-lookup"><span data-stu-id="c5ea1-112">Remarks</span></span>

<span data-ttu-id="c5ea1-113">[**CPullPin：： Seek**](cpullpin-seek.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="c5ea1-114">在每個從這個物件接收資料的下游輸入 pin 上，執行此方法以呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="c5ea1-115">如果您篩選的輸出 pin (s) 衍生自 [**CBaseOutputPin**](cbaseoutputpin.md)，請呼叫 [**CBaseOutputPin：:D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="c5ea1-116">這項設計可讓篩選準則直接在 **CPullPin** 物件上呼叫 **seek** 來搜尋資料流程。</span><span class="sxs-lookup"><span data-stu-id="c5ea1-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ea1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5ea1-117">Requirements</span></span>



| <span data-ttu-id="c5ea1-118">需求</span><span class="sxs-lookup"><span data-stu-id="c5ea1-118">Requirement</span></span> | <span data-ttu-id="c5ea1-119">值</span><span class="sxs-lookup"><span data-stu-id="c5ea1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ea1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c5ea1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c5ea1-121"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea1-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c5ea1-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5ea1-122">Library</span></span><br/> | <dl> <span data-ttu-id="c5ea1-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c5ea1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ea1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5ea1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ea1-125">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="c5ea1-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




