---
description: EndFlush 方法會結束清除作業。 實行 IPin：： EndFlush 方法。
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: 'CBaseInputPin. EndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994217"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="a91cb-104">CBaseInputPin. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="a91cb-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="a91cb-105">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="a91cb-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="a91cb-106">實行 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="a91cb-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91cb-107">語法</span><span class="sxs-lookup"><span data-stu-id="a91cb-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="a91cb-108">參數</span><span class="sxs-lookup"><span data-stu-id="a91cb-108">Parameters</span></span>

<span data-ttu-id="a91cb-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a91cb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a91cb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a91cb-110">Return value</span></span>

<span data-ttu-id="a91cb-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a91cb-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a91cb-112">備註</span><span class="sxs-lookup"><span data-stu-id="a91cb-112">Remarks</span></span>

<span data-ttu-id="a91cb-113">這個方法會將 [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md) 旗標設定為 **TRUE**，這 [**會讓 CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法接受範例。</span><span class="sxs-lookup"><span data-stu-id="a91cb-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="a91cb-114">衍生的類別必須覆寫這個方法，並執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a91cb-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="a91cb-115">釋放任何緩衝的資料，並等候所有已排入佇列的樣本被捨棄。</span><span class="sxs-lookup"><span data-stu-id="a91cb-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="a91cb-116">清除任何擱置中的 [**EC \_ 完成**](ec-complete.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="a91cb-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="a91cb-117">呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="a91cb-117">Call the base class method.</span></span>
4.  <span data-ttu-id="a91cb-118">對下游輸入 pin 呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 。</span><span class="sxs-lookup"><span data-stu-id="a91cb-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="a91cb-119">如果 pin 尚未提供任何下游媒體範例，您可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="a91cb-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="a91cb-120">如果您的輸出圖釘衍生自 [**CBaseOutputPin**](cbaseoutputpin.md) 類別，您可以呼叫 [**CBaseOutputPin：:D eliverendflush**](cbaseoutputpin-deliverendflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a91cb-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91cb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a91cb-121">Requirements</span></span>



| <span data-ttu-id="a91cb-122">需求</span><span class="sxs-lookup"><span data-stu-id="a91cb-122">Requirement</span></span> | <span data-ttu-id="a91cb-123">值</span><span class="sxs-lookup"><span data-stu-id="a91cb-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91cb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a91cb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a91cb-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a91cb-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a91cb-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a91cb-126">Library</span></span><br/> | <dl> <span data-ttu-id="a91cb-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a91cb-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a91cb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a91cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91cb-129">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="a91cb-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




