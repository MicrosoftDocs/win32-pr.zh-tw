---
description: GetSyncSource 方法會抓取篩選所使用的參考時鐘。 這個方法會實 IMediaFilter：： GetSyncSource 方法。
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: 'CBaseFilter. GetSyncSource 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996442"
---
# <a name="cbasefiltergetsyncsource-method"></a><span data-ttu-id="ae754-104">CBaseFilter. GetSyncSource 方法</span><span class="sxs-lookup"><span data-stu-id="ae754-104">CBaseFilter.GetSyncSource method</span></span>

<span data-ttu-id="ae754-105">`GetSyncSource`方法會抓取篩選所使用的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="ae754-105">The `GetSyncSource` method retrieves the reference clock that the filter is using.</span></span> <span data-ttu-id="ae754-106">這個方法會實 [**IMediaFilter：： GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) 方法。</span><span class="sxs-lookup"><span data-stu-id="ae754-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae754-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae754-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="ae754-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae754-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae754-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="ae754-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="ae754-110">接收時鐘 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="ae754-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae754-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae754-111">Return value</span></span>

<span data-ttu-id="ae754-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="ae754-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae754-113">備註</span><span class="sxs-lookup"><span data-stu-id="ae754-113">Remarks</span></span>

<span data-ttu-id="ae754-114">如果篩選未使用參考時鐘， *\* pClock* 會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ae754-114">If the filter is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="ae754-115">當方法傳回時，如果 *\* pClock* 為非 **Null**，則 **IReferenceClock** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="ae754-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="ae754-116">當您完成時，請務必放開。</span><span class="sxs-lookup"><span data-stu-id="ae754-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae754-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae754-117">Requirements</span></span>



| <span data-ttu-id="ae754-118">需求</span><span class="sxs-lookup"><span data-stu-id="ae754-118">Requirement</span></span> | <span data-ttu-id="ae754-119">值</span><span class="sxs-lookup"><span data-stu-id="ae754-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae754-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ae754-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ae754-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ae754-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae754-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="ae754-122">Library</span></span><br/> | <dl> <span data-ttu-id="ae754-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ae754-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae754-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae754-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae754-125">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="ae754-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




