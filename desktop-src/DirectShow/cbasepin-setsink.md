---
description: SetSink 方法會設定外部品質管制員。 這個方法會實 IQualityControl：： SetSink 方法。
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: 'CBasePin. SetSink 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983013"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="890ea-104">CBasePin. SetSink 方法</span><span class="sxs-lookup"><span data-stu-id="890ea-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="890ea-105">`SetSink`方法會設定外部品質管制員。</span><span class="sxs-lookup"><span data-stu-id="890ea-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="890ea-106">這個方法會實 [**IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) 方法。</span><span class="sxs-lookup"><span data-stu-id="890ea-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="890ea-107">語法</span><span class="sxs-lookup"><span data-stu-id="890ea-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="890ea-108">參數</span><span class="sxs-lookup"><span data-stu-id="890ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="890ea-109">*piqc*</span><span class="sxs-lookup"><span data-stu-id="890ea-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="890ea-110">品質管制員 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="890ea-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="890ea-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="890ea-111">Return value</span></span>

<span data-ttu-id="890ea-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="890ea-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="890ea-113">備註</span><span class="sxs-lookup"><span data-stu-id="890ea-113">Remarks</span></span>

<span data-ttu-id="890ea-114">呼叫這個方法，將品質控制訊息重新導向至外部品質管制員。</span><span class="sxs-lookup"><span data-stu-id="890ea-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="890ea-115">如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。</span><span class="sxs-lookup"><span data-stu-id="890ea-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="890ea-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="890ea-116">Requirements</span></span>



| <span data-ttu-id="890ea-117">需求</span><span class="sxs-lookup"><span data-stu-id="890ea-117">Requirement</span></span> | <span data-ttu-id="890ea-118">值</span><span class="sxs-lookup"><span data-stu-id="890ea-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="890ea-119">標頭</span><span class="sxs-lookup"><span data-stu-id="890ea-119">Header</span></span><br/>  | <dl> <span data-ttu-id="890ea-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="890ea-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="890ea-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="890ea-121">Library</span></span><br/> | <dl> <span data-ttu-id="890ea-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="890ea-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="890ea-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="890ea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="890ea-124">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="890ea-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




