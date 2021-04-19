---
description: 通知方法會通知 pin，要求品質變更。 這個方法會執行 IQualityControl：： Notify 方法。
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: 'CBaseInputPin： Notify 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984793"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="4d7a8-104">CBaseInputPin。通知方法</span><span class="sxs-lookup"><span data-stu-id="4d7a8-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="4d7a8-105">`Notify`方法會通知 pin，要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="4d7a8-106">這個方法會 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d7a8-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="4d7a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d7a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7a8-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="4d7a8-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7a8-110">傳送品質控制訊息之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="4d7a8-111">*問*</span><span class="sxs-lookup"><span data-stu-id="4d7a8-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7a8-112">包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7a8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d7a8-113">Return value</span></span>

<span data-ttu-id="4d7a8-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7a8-115">備註</span><span class="sxs-lookup"><span data-stu-id="4d7a8-115">Remarks</span></span>

<span data-ttu-id="4d7a8-116">篩選通常會將品質控制訊息傳遞至上游輸出 pin，而不是輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="4d7a8-117">因此，這個方法會傳回 \_ [確定]，而不執行任何操作。</span><span class="sxs-lookup"><span data-stu-id="4d7a8-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d7a8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d7a8-118">Requirements</span></span>



| <span data-ttu-id="4d7a8-119">需求</span><span class="sxs-lookup"><span data-stu-id="4d7a8-119">Requirement</span></span> | <span data-ttu-id="4d7a8-120">值</span><span class="sxs-lookup"><span data-stu-id="4d7a8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7a8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4d7a8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4d7a8-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4d7a8-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4d7a8-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d7a8-123">Library</span></span><br/> | <dl> <span data-ttu-id="4d7a8-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4d7a8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7a8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d7a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7a8-126">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="4d7a8-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="4d7a8-127">品質控制管理</span><span class="sxs-lookup"><span data-stu-id="4d7a8-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




