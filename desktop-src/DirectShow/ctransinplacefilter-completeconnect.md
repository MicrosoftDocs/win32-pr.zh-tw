---
description: CompleteConnect 方法會完成 pin 連接。
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: 'CTransInPlaceFilter. CompleteConnect 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981401"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="c14e2-103">CTransInPlaceFilter. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="c14e2-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="c14e2-104">`CompleteConnect`方法會完成 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="c14e2-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c14e2-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="c14e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c14e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c14e2-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="c14e2-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="c14e2-108">[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。</span><span class="sxs-lookup"><span data-stu-id="c14e2-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="c14e2-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="c14e2-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="c14e2-110">此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c14e2-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c14e2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c14e2-111">Return value</span></span>

<span data-ttu-id="c14e2-112">傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c14e2-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="c14e2-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="c14e2-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c14e2-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c14e2-114">Return code</span></span>                                                                                           | <span data-ttu-id="c14e2-115">Description</span><span class="sxs-lookup"><span data-stu-id="c14e2-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c14e2-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c14e2-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="c14e2-117">成功。</span><span class="sxs-lookup"><span data-stu-id="c14e2-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="c14e2-118"><dt>**VFW \_ E \_ NOT \_ IN \_ GRAPH**</dt></span><span class="sxs-lookup"><span data-stu-id="c14e2-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="c14e2-119">篩選不在篩選圖形中。</span><span class="sxs-lookup"><span data-stu-id="c14e2-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c14e2-120">備註</span><span class="sxs-lookup"><span data-stu-id="c14e2-120">Remarks</span></span>

<span data-ttu-id="c14e2-121">這個方法會覆寫 [**CTransformFilter：： CompleteConnect**](ctransformfilter-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c14e2-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="c14e2-122">篩選器的行為取決於 pin 連接的順序：</span><span class="sxs-lookup"><span data-stu-id="c14e2-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="c14e2-123">如果輸入 pin 是先連接的，則連接會使用暫存配置器。</span><span class="sxs-lookup"><span data-stu-id="c14e2-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="c14e2-124">當輸出連接時，篩選器會重新連接輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="c14e2-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="c14e2-125">重新連接輸入 pin 會導致上游篩選器重新協商配置器。</span><span class="sxs-lookup"><span data-stu-id="c14e2-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="c14e2-126">在該時間點，輸入釘選來自下游篩選器的配置器。</span><span class="sxs-lookup"><span data-stu-id="c14e2-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="c14e2-127">如需詳細資訊，請參閱 [**CTransInPlaceInputPin：： GetAllocator**](ctransinplaceinputpin-getallocator.md)。</span><span class="sxs-lookup"><span data-stu-id="c14e2-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="c14e2-128">如果輸出連接是先連接的，則輸出釘選不會選取配置器。</span><span class="sxs-lookup"><span data-stu-id="c14e2-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="c14e2-129">當輸入 pin 連線時，會為這兩個連接協調配置器。</span><span class="sxs-lookup"><span data-stu-id="c14e2-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="c14e2-130">如果輸入和輸出媒體類型不同，則篩選會使用輸入類型重新連接輸出釘選。</span><span class="sxs-lookup"><span data-stu-id="c14e2-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="c14e2-131">篩選器會藉由呼叫 [**CBaseFilter：： ReconnectPin**](cbasefilter-reconnectpin.md) 方法來執行所有 pin 重新連接。</span><span class="sxs-lookup"><span data-stu-id="c14e2-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="c14e2-132">**ReconnectPin** 方法接著會在篩選圖形管理員上呼叫 [**IFilterGraph2：： ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex)方法。</span><span class="sxs-lookup"><span data-stu-id="c14e2-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="c14e2-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c14e2-133">Requirements</span></span>



| <span data-ttu-id="c14e2-134">需求</span><span class="sxs-lookup"><span data-stu-id="c14e2-134">Requirement</span></span> | <span data-ttu-id="c14e2-135">值</span><span class="sxs-lookup"><span data-stu-id="c14e2-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c14e2-136">標頭</span><span class="sxs-lookup"><span data-stu-id="c14e2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c14e2-137"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c14e2-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c14e2-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="c14e2-138">Library</span></span><br/> | <dl> <span data-ttu-id="c14e2-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c14e2-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c14e2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c14e2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14e2-141">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c14e2-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




