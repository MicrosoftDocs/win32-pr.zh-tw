---
description: CBaseInputPin 方法會開始進行清除作業。 這個方法會實 IPin：： BeginFlush 方法。
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: 'CBaseInputPin. BeginFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994284"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="a833d-104">CBaseInputPin. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="a833d-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="a833d-105">`CBaseInputPin`方法會開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="a833d-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="a833d-106">這個方法會實 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="a833d-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a833d-107">語法</span><span class="sxs-lookup"><span data-stu-id="a833d-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="a833d-108">參數</span><span class="sxs-lookup"><span data-stu-id="a833d-108">Parameters</span></span>

<span data-ttu-id="a833d-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a833d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a833d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a833d-110">Return value</span></span>

<span data-ttu-id="a833d-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a833d-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a833d-112">備註</span><span class="sxs-lookup"><span data-stu-id="a833d-112">Remarks</span></span>

<span data-ttu-id="a833d-113">這個方法會將 [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md) 旗標設定為 **TRUE**，這會導致 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法拒絕其他任何範例。</span><span class="sxs-lookup"><span data-stu-id="a833d-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="a833d-114">衍生的類別必須覆寫這個方法，並執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a833d-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="a833d-115">對下游輸入 pin 呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="a833d-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="a833d-116">如果 pin 尚未提供任何下游媒體範例，您可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="a833d-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="a833d-117">如果您的輸出圖釘衍生自 [**CBaseOutputPin**](cbaseoutputpin.md) 類別，您可以呼叫 [**CBaseOutputPin：:D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a833d-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="a833d-118">呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="a833d-118">Call the base class method.</span></span>
3.  <span data-ttu-id="a833d-119">開始捨棄已排入佇列的資料。</span><span class="sxs-lookup"><span data-stu-id="a833d-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="a833d-120">從任何封鎖的呼叫傳回至 **Receive** 方法。</span><span class="sxs-lookup"><span data-stu-id="a833d-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a833d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a833d-121">Requirements</span></span>



| <span data-ttu-id="a833d-122">需求</span><span class="sxs-lookup"><span data-stu-id="a833d-122">Requirement</span></span> | <span data-ttu-id="a833d-123">值</span><span class="sxs-lookup"><span data-stu-id="a833d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a833d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a833d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a833d-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a833d-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a833d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a833d-126">Library</span></span><br/> | <dl> <span data-ttu-id="a833d-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a833d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a833d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a833d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a833d-129">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="a833d-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




