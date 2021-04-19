---
description: EndOfStream 方法會在物件傳遞最後一個樣本之後呼叫。 衍生的類別必須執行此方法。
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: 'CPullPin. EndOfStream 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979516"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="6ca3a-104">CPullPin. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="6ca3a-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="6ca3a-105">在 `EndOfStream` 物件傳遞最後一個範例之後，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="6ca3a-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="6ca3a-106">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="6ca3a-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca3a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6ca3a-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="6ca3a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6ca3a-108">Parameters</span></span>

<span data-ttu-id="6ca3a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6ca3a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ca3a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ca3a-110">Return value</span></span>

<span data-ttu-id="6ca3a-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6ca3a-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca3a-112">備註</span><span class="sxs-lookup"><span data-stu-id="6ca3a-112">Remarks</span></span>

<span data-ttu-id="6ca3a-113">您可以使用這個方法，在每個從這個物件接收資料的下游輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 。</span><span class="sxs-lookup"><span data-stu-id="6ca3a-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="6ca3a-114">如果您篩選的輸出 pin (s) 衍生自 [**CBaseOutputPin**](cbaseoutputpin.md)，請呼叫 [**CBaseOutputPin：:D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6ca3a-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca3a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ca3a-115">Requirements</span></span>



| <span data-ttu-id="6ca3a-116">需求</span><span class="sxs-lookup"><span data-stu-id="6ca3a-116">Requirement</span></span> | <span data-ttu-id="6ca3a-117">值</span><span class="sxs-lookup"><span data-stu-id="6ca3a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca3a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6ca3a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6ca3a-119"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca3a-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="6ca3a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ca3a-120">Library</span></span><br/> | <dl> <span data-ttu-id="6ca3a-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6ca3a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca3a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ca3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca3a-123">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="6ca3a-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




