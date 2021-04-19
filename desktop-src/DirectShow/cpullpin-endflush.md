---
description: EndFlush 方法會通知擁有篩選以結束清除作業。 衍生的類別必須執行此方法。
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: 'CPullPin. EndFlush 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999450"
---
# <a name="cpullpinendflush-method"></a><span data-ttu-id="98ee0-104">CPullPin. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="98ee0-104">CPullPin.EndFlush method</span></span>

<span data-ttu-id="98ee0-105">`EndFlush`方法會通知擁有篩選以結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="98ee0-105">The `EndFlush` method informs the owning filter to end a flush operation.</span></span> <span data-ttu-id="98ee0-106">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="98ee0-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ee0-107">語法</span><span class="sxs-lookup"><span data-stu-id="98ee0-107">Syntax</span></span>


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a><span data-ttu-id="98ee0-108">參數</span><span class="sxs-lookup"><span data-stu-id="98ee0-108">Parameters</span></span>

<span data-ttu-id="98ee0-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="98ee0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98ee0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="98ee0-110">Return value</span></span>

<span data-ttu-id="98ee0-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="98ee0-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ee0-112">備註</span><span class="sxs-lookup"><span data-stu-id="98ee0-112">Remarks</span></span>

<span data-ttu-id="98ee0-113">[**CPullPin：： Seek**](cpullpin-seek.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="98ee0-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="98ee0-114">在每個從這個物件接收資料的下游輸入 pin 上，執行此方法以呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="98ee0-114">Implement this method to call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="98ee0-115">如果您篩選的輸出 pin (s) 衍生自 **CBaseOutputPin**，請呼叫 **CBaseOutputPin：:D eliverendflush** 方法。</span><span class="sxs-lookup"><span data-stu-id="98ee0-115">If your filter's output pin(s) derive from **CBaseOutputPin**, call the **CBaseOutputPin::DeliverEndFlush** method.</span></span>

<span data-ttu-id="98ee0-116">這項設計可讓篩選準則直接在 **CPullPin** 物件上呼叫 **seek** 來搜尋資料流程。</span><span class="sxs-lookup"><span data-stu-id="98ee0-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ee0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="98ee0-117">Requirements</span></span>



| <span data-ttu-id="98ee0-118">需求</span><span class="sxs-lookup"><span data-stu-id="98ee0-118">Requirement</span></span> | <span data-ttu-id="98ee0-119">值</span><span class="sxs-lookup"><span data-stu-id="98ee0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ee0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="98ee0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="98ee0-121"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="98ee0-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="98ee0-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="98ee0-122">Library</span></span><br/> | <dl> <span data-ttu-id="98ee0-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="98ee0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ee0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98ee0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ee0-125">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="98ee0-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




