---
description: ReconnectPin 方法會中斷現有的 pin 連線，並使用指定的媒體類型將它重新連接到相同的 pin。
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: 'CBaseFilter. ReconnectPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986575"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="7f816-103">CBaseFilter. ReconnectPin 方法</span><span class="sxs-lookup"><span data-stu-id="7f816-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="7f816-104">`ReconnectPin`方法會中斷現有的 pin 連線，並使用指定的媒體類型將它重新連接到相同的 pin。</span><span class="sxs-lookup"><span data-stu-id="7f816-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f816-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f816-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="7f816-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f816-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f816-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="7f816-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="7f816-108">釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7f816-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7f816-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="7f816-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7f816-110">指定媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f816-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f816-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f816-111">Return value</span></span>

<span data-ttu-id="7f816-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7f816-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7f816-113">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="7f816-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="7f816-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7f816-114">Return code</span></span>                                                                                   | <span data-ttu-id="7f816-115">Description</span><span class="sxs-lookup"><span data-stu-id="7f816-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f816-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7f816-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7f816-117">成功。</span><span class="sxs-lookup"><span data-stu-id="7f816-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="7f816-118"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="7f816-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="7f816-119">[**m \_ pGraph**](cbasefilter-m-pgraph.md) 成員變數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f816-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f816-120">備註</span><span class="sxs-lookup"><span data-stu-id="7f816-120">Remarks</span></span>

<span data-ttu-id="7f816-121">這個方法會在篩選圖形管理員上呼叫 [**IFilterGraph2：： ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f816-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="7f816-122">如果無法使用 [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) 介面，方法會呼叫 [**IFilterGraph：： Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect)。</span><span class="sxs-lookup"><span data-stu-id="7f816-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f816-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f816-123">Requirements</span></span>



| <span data-ttu-id="7f816-124">需求</span><span class="sxs-lookup"><span data-stu-id="7f816-124">Requirement</span></span> | <span data-ttu-id="7f816-125">值</span><span class="sxs-lookup"><span data-stu-id="7f816-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f816-126">標頭</span><span class="sxs-lookup"><span data-stu-id="7f816-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7f816-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f816-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7f816-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f816-128">Library</span></span><br/> | <dl> <span data-ttu-id="7f816-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f816-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f816-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f816-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f816-131">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="7f816-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




