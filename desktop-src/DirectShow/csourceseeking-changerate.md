---
description: 當播放速率變更時，會呼叫 ChangeRate 方法。
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: 'CSourceSeeking. ChangeRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975999"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="a8ded-103">CSourceSeeking. ChangeRate 方法</span><span class="sxs-lookup"><span data-stu-id="a8ded-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="a8ded-104">`ChangeRate`當播放速率變更時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="a8ded-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ded-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8ded-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="a8ded-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8ded-106">Parameters</span></span>

<span data-ttu-id="a8ded-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a8ded-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8ded-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8ded-108">Return value</span></span>

<span data-ttu-id="a8ded-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a8ded-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ded-110">備註</span><span class="sxs-lookup"><span data-stu-id="a8ded-110">Remarks</span></span>

<span data-ttu-id="a8ded-111">[**CSourceSeeking：： SetRate**](csourceseeking-setrate.md)方法會呼叫這個方法，而衍生的類別必須在此方法中執行。</span><span class="sxs-lookup"><span data-stu-id="a8ded-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="a8ded-112">**SetRate** 方法會更新 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md)成員變數，但不會驗證新值。</span><span class="sxs-lookup"><span data-stu-id="a8ded-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="a8ded-113">應一律拒絕零的速率。</span><span class="sxs-lookup"><span data-stu-id="a8ded-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="a8ded-114">小於零的速率表示會有負面的播放。</span><span class="sxs-lookup"><span data-stu-id="a8ded-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="a8ded-115">大部分的篩選不支援負數速率。</span><span class="sxs-lookup"><span data-stu-id="a8ded-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="a8ded-116">下列範例顯示可能的實作為：</span><span class="sxs-lookup"><span data-stu-id="a8ded-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="a8ded-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8ded-117">Requirements</span></span>



| <span data-ttu-id="a8ded-118">需求</span><span class="sxs-lookup"><span data-stu-id="a8ded-118">Requirement</span></span> | <span data-ttu-id="a8ded-119">值</span><span class="sxs-lookup"><span data-stu-id="a8ded-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ded-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a8ded-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a8ded-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a8ded-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8ded-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8ded-122">Library</span></span><br/> | <dl> <span data-ttu-id="a8ded-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a8ded-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ded-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8ded-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ded-125">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="a8ded-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




