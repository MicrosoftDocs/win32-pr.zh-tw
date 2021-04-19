---
description: SetSyncSource 方法會設定篩選的參考時鐘。 這個方法會實 IMediaFilter：： SetSyncSource 方法。
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: 'CBaseFilter. SetSyncSource 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8eaab23f1afd7e7b502d6828bc3f10cbfec49410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980172"
---
# <a name="cbasefiltersetsyncsource-method"></a><span data-ttu-id="ce289-104">CBaseFilter. SetSyncSource 方法</span><span class="sxs-lookup"><span data-stu-id="ce289-104">CBaseFilter.SetSyncSource method</span></span>

<span data-ttu-id="ce289-105">**SetSyncSource** 方法會設定篩選的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="ce289-105">The **SetSyncSource** method sets a reference clock for the filter.</span></span> <span data-ttu-id="ce289-106">這個方法會實 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法。</span><span class="sxs-lookup"><span data-stu-id="ce289-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce289-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce289-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="ce289-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce289-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="ce289-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="ce289-110">時鐘 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ce289-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce289-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce289-111">Return value</span></span>

<span data-ttu-id="ce289-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ce289-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce289-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce289-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce289-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce289-114">Requirements</span></span>



| <span data-ttu-id="ce289-115">需求</span><span class="sxs-lookup"><span data-stu-id="ce289-115">Requirement</span></span> | <span data-ttu-id="ce289-116">值</span><span class="sxs-lookup"><span data-stu-id="ce289-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce289-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ce289-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ce289-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ce289-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce289-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce289-119">Library</span></span><br/> | <dl> <span data-ttu-id="ce289-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ce289-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce289-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce289-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce289-122">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="ce289-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




