---
description: NotifyEvent 方法會將事件通知傳送至篩選圖形管理員。
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: 'CBaseFilter. NotifyEvent 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983185"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="4e471-103">CBaseFilter. NotifyEvent 方法</span><span class="sxs-lookup"><span data-stu-id="4e471-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="4e471-104">`NotifyEvent`方法會將事件通知傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="4e471-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e471-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e471-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="4e471-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e471-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e471-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="4e471-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4e471-108">事件通知碼。</span><span class="sxs-lookup"><span data-stu-id="4e471-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4e471-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="4e471-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4e471-110">事件的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="4e471-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="4e471-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="4e471-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4e471-112">事件的第二個參數。</span><span class="sxs-lookup"><span data-stu-id="4e471-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e471-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e471-113">Return value</span></span>

<span data-ttu-id="4e471-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4e471-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4e471-115">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="4e471-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="4e471-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4e471-116">Return code</span></span>                                                                               | <span data-ttu-id="4e471-117">Description</span><span class="sxs-lookup"><span data-stu-id="4e471-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e471-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="4e471-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="4e471-119">篩選圖形管理員不接受事件通知。</span><span class="sxs-lookup"><span data-stu-id="4e471-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="4e471-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4e471-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4e471-121">成功。</span><span class="sxs-lookup"><span data-stu-id="4e471-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4e471-122"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4e471-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="4e471-123">篩選沒有指向 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4e471-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e471-124">備註</span><span class="sxs-lookup"><span data-stu-id="4e471-124">Remarks</span></span>

<span data-ttu-id="4e471-125">如需通知碼和參數值的清單，請參閱 [事件通知碼](event-notification-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="4e471-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="4e471-126">在基類中，如果事件程式碼為 EC \_ 完成，方法會將 *EventParam2* 參數設定為篩選的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="4e471-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e471-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e471-127">Requirements</span></span>



| <span data-ttu-id="4e471-128">需求</span><span class="sxs-lookup"><span data-stu-id="4e471-128">Requirement</span></span> | <span data-ttu-id="4e471-129">值</span><span class="sxs-lookup"><span data-stu-id="4e471-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e471-130">標頭</span><span class="sxs-lookup"><span data-stu-id="4e471-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4e471-131"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4e471-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e471-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e471-132">Library</span></span><br/> | <dl> <span data-ttu-id="4e471-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4e471-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e471-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e471-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e471-135">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4e471-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




