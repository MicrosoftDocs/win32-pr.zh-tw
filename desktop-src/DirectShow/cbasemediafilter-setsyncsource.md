---
description: SetSyncSource 方法會設定物件的參考時鐘。 這個方法會實 IMediaFilter：： SetSyncSource 方法。
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: 'CBaseMediaFilter. SetSyncSource 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998380"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="c8a7d-104">CBaseMediaFilter. SetSyncSource 方法</span><span class="sxs-lookup"><span data-stu-id="c8a7d-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="c8a7d-105">`SetSyncSource`方法會設定物件的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="c8a7d-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="c8a7d-106">這個方法會實 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法。</span><span class="sxs-lookup"><span data-stu-id="c8a7d-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8a7d-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="c8a7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8a7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a7d-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="c8a7d-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="c8a7d-110">時鐘 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8a7d-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a7d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8a7d-111">Return value</span></span>

<span data-ttu-id="c8a7d-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c8a7d-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a7d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8a7d-113">Requirements</span></span>



| <span data-ttu-id="c8a7d-114">需求</span><span class="sxs-lookup"><span data-stu-id="c8a7d-114">Requirement</span></span> | <span data-ttu-id="c8a7d-115">值</span><span class="sxs-lookup"><span data-stu-id="c8a7d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a7d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="c8a7d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c8a7d-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c8a7d-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c8a7d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8a7d-118">Library</span></span><br/> | <dl> <span data-ttu-id="c8a7d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c8a7d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a7d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8a7d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a7d-121">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c8a7d-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




