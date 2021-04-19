---
description: SetSyncSource 方法會通知目前參考時鐘的基類。
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: 'CBaseStreamControl. SetSyncSource 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981873"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="f01d5-103">CBaseStreamControl. SetSyncSource 方法</span><span class="sxs-lookup"><span data-stu-id="f01d5-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="f01d5-104">`SetSyncSource`方法會通知目前參考時鐘的基類。</span><span class="sxs-lookup"><span data-stu-id="f01d5-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="f01d5-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="f01d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="f01d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01d5-107">*pRefClock*</span><span class="sxs-lookup"><span data-stu-id="f01d5-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="f01d5-108">參考時鐘之 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f01d5-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01d5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f01d5-109">Return value</span></span>

<span data-ttu-id="f01d5-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f01d5-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f01d5-111">備註</span><span class="sxs-lookup"><span data-stu-id="f01d5-111">Remarks</span></span>

<span data-ttu-id="f01d5-112">從篩選的 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法內部呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f01d5-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="f01d5-113">**CBaseStreamControl** 類別會使用 **IReferenceClock** 介面，以確保它不會太快捨棄樣本。</span><span class="sxs-lookup"><span data-stu-id="f01d5-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="f01d5-114">範例</span><span class="sxs-lookup"><span data-stu-id="f01d5-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="f01d5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f01d5-115">Requirements</span></span>



| <span data-ttu-id="f01d5-116">需求</span><span class="sxs-lookup"><span data-stu-id="f01d5-116">Requirement</span></span> | <span data-ttu-id="f01d5-117">值</span><span class="sxs-lookup"><span data-stu-id="f01d5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f01d5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f01d5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f01d5-119"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f01d5-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f01d5-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="f01d5-120">Library</span></span><br/> | <dl> <span data-ttu-id="f01d5-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f01d5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f01d5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f01d5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01d5-123">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="f01d5-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




