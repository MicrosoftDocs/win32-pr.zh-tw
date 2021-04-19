---
description: Receive 方法會接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: 'CTransformFilter 的 Receive 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979511"
---
# <a name="ctransformfilterreceive-method"></a><span data-ttu-id="c7544-103">CTransformFilter 接收方法</span><span class="sxs-lookup"><span data-stu-id="c7544-103">CTransformFilter.Receive method</span></span>

<span data-ttu-id="c7544-104">`Receive`方法會接收媒體範例、進行處理，並將輸出範例傳遞給下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="c7544-104">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7544-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7544-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="c7544-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7544-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7544-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="c7544-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c7544-108">輸入範例上 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c7544-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7544-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7544-109">Return value</span></span>

<span data-ttu-id="c7544-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c7544-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c7544-111">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="c7544-111">Possible values include the following:</span></span>



| <span data-ttu-id="c7544-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c7544-112">Return code</span></span>                                                                             | <span data-ttu-id="c7544-113">Description</span><span class="sxs-lookup"><span data-stu-id="c7544-113">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c7544-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c7544-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c7544-115">上游篩選應停止傳送範例。</span><span class="sxs-lookup"><span data-stu-id="c7544-115">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="c7544-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c7544-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c7544-117">成功。</span><span class="sxs-lookup"><span data-stu-id="c7544-117">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="c7544-118">備註</span><span class="sxs-lookup"><span data-stu-id="c7544-118">Remarks</span></span>

<span data-ttu-id="c7544-119">篩選的輸入 pin 會在收到範例時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c7544-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="c7544-120">這個方法會呼叫 [**CTransformFilter：： InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) 方法，以準備新的輸出範例。</span><span class="sxs-lookup"><span data-stu-id="c7544-120">This method calls the [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) method, which prepares a new output sample.</span></span> <span data-ttu-id="c7544-121">然後，它會呼叫衍生類別必須執行的 [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7544-121">Then it calls the [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="c7544-122">**轉換** 方法會處理輸入資料並產生輸出資料。</span><span class="sxs-lookup"><span data-stu-id="c7544-122">The **Transform** method processes the input data and produces output data.</span></span>

<span data-ttu-id="c7544-123">如果 **轉換** 方法傳回 \_ FALSE，則方法會卸載 `Receive` 此範例。</span><span class="sxs-lookup"><span data-stu-id="c7544-123">If the **Transform** method returns S\_FALSE, the `Receive` method drops this sample.</span></span> <span data-ttu-id="c7544-124">在第一個捨棄的範例中，篩選準則會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="c7544-124">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="c7544-125">否則，如果 **轉換** 方法傳回 S \_ OK，則篩選會傳遞輸出範例。</span><span class="sxs-lookup"><span data-stu-id="c7544-125">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="c7544-126">若要這樣做，它會對下游輸入 pin 呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。</span><span class="sxs-lookup"><span data-stu-id="c7544-126">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7544-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7544-127">Requirements</span></span>



| <span data-ttu-id="c7544-128">需求</span><span class="sxs-lookup"><span data-stu-id="c7544-128">Requirement</span></span> | <span data-ttu-id="c7544-129">值</span><span class="sxs-lookup"><span data-stu-id="c7544-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7544-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c7544-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c7544-131"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c7544-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c7544-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7544-132">Library</span></span><br/> | <dl> <span data-ttu-id="c7544-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c7544-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7544-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7544-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7544-135">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c7544-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




