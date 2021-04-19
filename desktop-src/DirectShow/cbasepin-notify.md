---
description: 通知方法會通知 pin，要求品質變更。 這個方法會執行 IQualityControl：： Notify 方法。
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: 'CBasePin： Notify 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997699"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="eddd7-104">CBasePin。通知方法</span><span class="sxs-lookup"><span data-stu-id="eddd7-104">CBasePin.Notify method</span></span>

<span data-ttu-id="eddd7-105">`Notify`方法會通知 pin，要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="eddd7-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="eddd7-106">這個方法會 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。</span><span class="sxs-lookup"><span data-stu-id="eddd7-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eddd7-107">語法</span><span class="sxs-lookup"><span data-stu-id="eddd7-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="eddd7-108">參數</span><span class="sxs-lookup"><span data-stu-id="eddd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eddd7-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="eddd7-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="eddd7-110">傳遞品質控制訊息之篩選準則的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="eddd7-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="eddd7-111">*問*</span><span class="sxs-lookup"><span data-stu-id="eddd7-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="eddd7-112">指定包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality) 結構。</span><span class="sxs-lookup"><span data-stu-id="eddd7-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eddd7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eddd7-113">Return value</span></span>

<span data-ttu-id="eddd7-114">基類會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="eddd7-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="eddd7-115">備註</span><span class="sxs-lookup"><span data-stu-id="eddd7-115">Remarks</span></span>

<span data-ttu-id="eddd7-116">輸出圖釘應覆寫此方法，以接受品質控制訊息。</span><span class="sxs-lookup"><span data-stu-id="eddd7-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="eddd7-117">如果已安裝外部品質管制員 (請參閱 [**CBasePin：： SetSink**](cbasepin-setsink.md)) ，將訊息傳遞給該品質管制員。</span><span class="sxs-lookup"><span data-stu-id="eddd7-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="eddd7-118">否則，篩選器應該會處理訊息本身，或將訊息傳遞至上游。</span><span class="sxs-lookup"><span data-stu-id="eddd7-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="eddd7-119">如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。</span><span class="sxs-lookup"><span data-stu-id="eddd7-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eddd7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="eddd7-120">Requirements</span></span>



| <span data-ttu-id="eddd7-121">需求</span><span class="sxs-lookup"><span data-stu-id="eddd7-121">Requirement</span></span> | <span data-ttu-id="eddd7-122">值</span><span class="sxs-lookup"><span data-stu-id="eddd7-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eddd7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eddd7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eddd7-124"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eddd7-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eddd7-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="eddd7-125">Library</span></span><br/> | <dl> <span data-ttu-id="eddd7-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eddd7-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eddd7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eddd7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddd7-128">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="eddd7-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




