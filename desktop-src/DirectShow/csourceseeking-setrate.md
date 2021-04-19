---
description: SetRate 方法會設定播放速率。 這個方法會實 IMediaSeeking：： SetRate 方法。
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: 'CSourceSeeking. SetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994719"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="cc0fc-104">CSourceSeeking. SetRate 方法</span><span class="sxs-lookup"><span data-stu-id="cc0fc-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="cc0fc-105">`SetRate`方法會設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="cc0fc-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="cc0fc-106">這個方法會實 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="cc0fc-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc0fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="cc0fc-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="cc0fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="cc0fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc0fc-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="cc0fc-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="cc0fc-110">播放速率。</span><span class="sxs-lookup"><span data-stu-id="cc0fc-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc0fc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc0fc-111">Return value</span></span>

<span data-ttu-id="cc0fc-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cc0fc-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc0fc-113">備註</span><span class="sxs-lookup"><span data-stu-id="cc0fc-113">Remarks</span></span>

<span data-ttu-id="cc0fc-114">這個方法會更新 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) 成員變數的值，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0fc-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="cc0fc-115">方法不會驗證 *dRate* 參數。</span><span class="sxs-lookup"><span data-stu-id="cc0fc-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc0fc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc0fc-116">Requirements</span></span>



| <span data-ttu-id="cc0fc-117">需求</span><span class="sxs-lookup"><span data-stu-id="cc0fc-117">Requirement</span></span> | <span data-ttu-id="cc0fc-118">值</span><span class="sxs-lookup"><span data-stu-id="cc0fc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0fc-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cc0fc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc0fc-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cc0fc-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc0fc-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc0fc-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc0fc-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cc0fc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc0fc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc0fc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc0fc-124">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="cc0fc-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




