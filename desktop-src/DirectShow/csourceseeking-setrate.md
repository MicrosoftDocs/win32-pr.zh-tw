---
description: CSourceSeeking. SetRate 方法-SetRate 方法會設定播放速率。 這個方法會實 IMediaSeeking：： SetRate 方法。
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
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098736"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="5acf4-104">CSourceSeeking. SetRate 方法</span><span class="sxs-lookup"><span data-stu-id="5acf4-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="5acf4-105">`SetRate`方法會設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="5acf4-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="5acf4-106">這個方法會實 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="5acf4-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5acf4-107">語法</span><span class="sxs-lookup"><span data-stu-id="5acf4-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="5acf4-108">參數</span><span class="sxs-lookup"><span data-stu-id="5acf4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5acf4-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="5acf4-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="5acf4-110">播放速率。</span><span class="sxs-lookup"><span data-stu-id="5acf4-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5acf4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5acf4-111">Return value</span></span>

<span data-ttu-id="5acf4-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5acf4-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5acf4-113">備註</span><span class="sxs-lookup"><span data-stu-id="5acf4-113">Remarks</span></span>

<span data-ttu-id="5acf4-114">這個方法會更新 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) 成員變數的值，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeRate**](csourceseeking-changerate.md)。</span><span class="sxs-lookup"><span data-stu-id="5acf4-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="5acf4-115">方法不會驗證 *dRate* 參數。</span><span class="sxs-lookup"><span data-stu-id="5acf4-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5acf4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5acf4-116">Requirements</span></span>



| <span data-ttu-id="5acf4-117">需求</span><span class="sxs-lookup"><span data-stu-id="5acf4-117">Requirement</span></span> | <span data-ttu-id="5acf4-118">值</span><span class="sxs-lookup"><span data-stu-id="5acf4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5acf4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5acf4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5acf4-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5acf4-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5acf4-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="5acf4-121">Library</span></span><br/> | <dl> <span data-ttu-id="5acf4-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5acf4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5acf4-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5acf4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acf4-124">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="5acf4-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




