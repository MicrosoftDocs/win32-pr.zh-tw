---
description: 如果在資料流程處理期間發生錯誤，則會呼叫 OnError 方法。 衍生的類別必須執行此方法。
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: 'CPullPin： OnError 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999379"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="9980d-104">CPullPin 的 OnError 方法</span><span class="sxs-lookup"><span data-stu-id="9980d-104">CPullPin.OnError method</span></span>

<span data-ttu-id="9980d-105">`OnError`如果在串流處理期間發生錯誤，則會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="9980d-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="9980d-106">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="9980d-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9980d-107">語法</span><span class="sxs-lookup"><span data-stu-id="9980d-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="9980d-108">參數</span><span class="sxs-lookup"><span data-stu-id="9980d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9980d-109">*小時*</span><span class="sxs-lookup"><span data-stu-id="9980d-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="9980d-110">指定失敗的方法所傳回的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="9980d-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9980d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9980d-111">Return value</span></span>

<span data-ttu-id="9980d-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9980d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9980d-113">備註</span><span class="sxs-lookup"><span data-stu-id="9980d-113">Remarks</span></span>

<span data-ttu-id="9980d-114">每當發生會中止資料提取執行緒的錯誤時，物件就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9980d-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="9980d-115">篩選可以使用這個方法，以正常方式從資料流程錯誤中復原。</span><span class="sxs-lookup"><span data-stu-id="9980d-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="9980d-116">在大部分的情況下，會從上游篩選傳回錯誤，因此上游篩選器會負責向篩選圖形管理員報告該錯誤。</span><span class="sxs-lookup"><span data-stu-id="9980d-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="9980d-117">如果錯誤發生在 [**CPullPin：： Receive**](cpullpin-receive.md) 方法內，您的篩選器應該會傳送 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="9980d-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="9980d-118"> (參閱 [**IMediaEventSink：： Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)。 ) </span><span class="sxs-lookup"><span data-stu-id="9980d-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="9980d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9980d-119">Requirements</span></span>



| <span data-ttu-id="9980d-120">需求</span><span class="sxs-lookup"><span data-stu-id="9980d-120">Requirement</span></span> | <span data-ttu-id="9980d-121">值</span><span class="sxs-lookup"><span data-stu-id="9980d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9980d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9980d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9980d-123"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="9980d-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="9980d-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9980d-124">Library</span></span><br/> | <dl> <span data-ttu-id="9980d-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9980d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9980d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9980d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9980d-127">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9980d-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




