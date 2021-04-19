---
description: RegisterMediaTime 方法會快取目前範例中的時間戳記。 這個方法會使用 *StartTime* 和 *EndTime* 參數。
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) -StartTime 和 EndTime 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106984494"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="e006b-104">CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) -StartTime 和 EndTime 參數</span><span class="sxs-lookup"><span data-stu-id="e006b-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="e006b-105">[**RegisterMediaTime**](crendererpospassthru-registermediatime.md)方法會快取目前範例中的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e006b-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e006b-106">語法</span><span class="sxs-lookup"><span data-stu-id="e006b-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="e006b-107">參數</span><span class="sxs-lookup"><span data-stu-id="e006b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e006b-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="e006b-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e006b-109">範例開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="e006b-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e006b-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="e006b-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e006b-111">範例結束時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="e006b-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e006b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e006b-112">Return value</span></span>

<span data-ttu-id="e006b-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e006b-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e006b-114">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="e006b-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e006b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e006b-115">Return code</span></span>                                                                          | <span data-ttu-id="e006b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e006b-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="e006b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e006b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e006b-118">成功。</span><span class="sxs-lookup"><span data-stu-id="e006b-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e006b-119">備註</span><span class="sxs-lookup"><span data-stu-id="e006b-119">Remarks</span></span>

<span data-ttu-id="e006b-120">這個方法會儲存 *StartTime* 和 *EndTime* 中提供的時間戳記值。</span><span class="sxs-lookup"><span data-stu-id="e006b-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="e006b-121">[**CRendererPosPassThru：： GetMediaTime**](crendererpospassthru-getmediatime.md)方法會抓取相同的值。</span><span class="sxs-lookup"><span data-stu-id="e006b-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="e006b-122">篩選應該針對它收到的每個範例呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e006b-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="e006b-123">方法會多載，以接受範例的指標或時間戳記值本身。</span><span class="sxs-lookup"><span data-stu-id="e006b-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="e006b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e006b-124">Requirements</span></span>



| <span data-ttu-id="e006b-125">需求</span><span class="sxs-lookup"><span data-stu-id="e006b-125">Requirement</span></span> | <span data-ttu-id="e006b-126">值</span><span class="sxs-lookup"><span data-stu-id="e006b-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e006b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e006b-127">Header</span></span>  | <span data-ttu-id="e006b-128">Ctlutil (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="e006b-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="e006b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="e006b-129">Library</span></span> | <span data-ttu-id="e006b-130"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="e006b-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




