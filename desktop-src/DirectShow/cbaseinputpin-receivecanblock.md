---
description: ReceiveCanBlock 方法會判斷 IMemInputPin：： Receive 方法的呼叫是否可能封鎖。 這個方法會實 IMemInputPin：： ReceiveCanBlock 方法。
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: 'CBaseInputPin. ReceiveCanBlock 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996088"
---
# <a name="cbaseinputpinreceivecanblock-method"></a><span data-ttu-id="549be-104">CBaseInputPin. ReceiveCanBlock 方法</span><span class="sxs-lookup"><span data-stu-id="549be-104">CBaseInputPin.ReceiveCanBlock method</span></span>

<span data-ttu-id="549be-105">`ReceiveCanBlock`方法會判斷 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)方法的呼叫是否可能封鎖。</span><span class="sxs-lookup"><span data-stu-id="549be-105">The `ReceiveCanBlock` method determines whether calls to the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method might block.</span></span> <span data-ttu-id="549be-106">這個方法會實 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) 方法。</span><span class="sxs-lookup"><span data-stu-id="549be-106">This method implements the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="549be-107">語法</span><span class="sxs-lookup"><span data-stu-id="549be-107">Syntax</span></span>


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a><span data-ttu-id="549be-108">參數</span><span class="sxs-lookup"><span data-stu-id="549be-108">Parameters</span></span>

<span data-ttu-id="549be-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="549be-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="549be-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="549be-110">Return value</span></span>

<span data-ttu-id="549be-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="549be-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="549be-112">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="549be-112">Possible value include those listed in the following table.</span></span>



| <span data-ttu-id="549be-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="549be-113">Return code</span></span>                                                                             | <span data-ttu-id="549be-114">Description</span><span class="sxs-lookup"><span data-stu-id="549be-114">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="549be-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="549be-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="549be-116">Pin 不會封鎖 **接聽** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="549be-116">The pin will not block on a call to **Receive**.</span></span><br/> |
| <dl> <span data-ttu-id="549be-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="549be-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="549be-118">Pin 可能會封鎖 **接聽** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="549be-118">The pin might block on a call to **Receive**.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="549be-119">備註</span><span class="sxs-lookup"><span data-stu-id="549be-119">Remarks</span></span>

<span data-ttu-id="549be-120">\_如果保證無法封鎖 **接收** 方法的呼叫，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="549be-120">Return S\_FALSE if calls to the **Receive** method are guaranteed not to block.</span></span> <span data-ttu-id="549be-121">否則，請傳回 \_ [確定] 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="549be-121">Otherwise, return S\_OK or an error code.</span></span> <span data-ttu-id="549be-122">如果 **接收** 方法呼叫下游 Pin 的 **receive** ，則下游 pin 可能會封鎖; `ReceiveCanBlock` 必須將該因素列入考慮。</span><span class="sxs-lookup"><span data-stu-id="549be-122">If the **Receive** method calls **Receive** on a downstream pin, the downstream pin might block; `ReceiveCanBlock` must take that factor into account.</span></span>

<span data-ttu-id="549be-123">上游篩選器可以使用這個方法來判斷它的執行緒策略。</span><span class="sxs-lookup"><span data-stu-id="549be-123">An upstream filter can use this method to determine its threading strategy.</span></span> <span data-ttu-id="549be-124">如果 **接收** 方法可能會封鎖，上游篩選可能會決定使用可緩衝資料的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="549be-124">If the **Receive** method might block, the upstream filter might decide to use a worker thread that buffers data.</span></span> <span data-ttu-id="549be-125">如需此策略的執行，請參閱 [**COutputQueue**](coutputqueue.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="549be-125">See the [**COutputQueue**](coutputqueue.md) class for an implementation of this strategy.</span></span>

<span data-ttu-id="549be-126">在基類中， \_ 當下列任一條件成立時，這個方法會傳回 S OK：</span><span class="sxs-lookup"><span data-stu-id="549be-126">In the base class, this method returns S\_OK when any of the following are true:</span></span>

-   <span data-ttu-id="549be-127">篩選沒有輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="549be-127">The filter has no output pins.</span></span>
-   <span data-ttu-id="549be-128">連線到此篩選的輸入 pin 可能會封鎖。</span><span class="sxs-lookup"><span data-stu-id="549be-128">An input pin connected to this filter signals that it might block.</span></span>
-   <span data-ttu-id="549be-129">連接到此篩選的輸入 pin 不支援 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。</span><span class="sxs-lookup"><span data-stu-id="549be-129">An input pin connected to this filter does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="549be-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="549be-130">Requirements</span></span>



| <span data-ttu-id="549be-131">需求</span><span class="sxs-lookup"><span data-stu-id="549be-131">Requirement</span></span> | <span data-ttu-id="549be-132">值</span><span class="sxs-lookup"><span data-stu-id="549be-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549be-133">標頭</span><span class="sxs-lookup"><span data-stu-id="549be-133">Header</span></span><br/>  | <dl> <span data-ttu-id="549be-134"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="549be-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="549be-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="549be-135">Library</span></span><br/> | <dl> <span data-ttu-id="549be-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="549be-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="549be-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="549be-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549be-138">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="549be-138">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




