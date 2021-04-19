---
description: GetTime 方法會抓取這個範例開始和完成的資料流程時間。 這個方法會實 IMediaSample：： GetTime 方法。
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: 'CMediaSample. GetTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998595"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="aa131-104">CMediaSample. GetTime 方法</span><span class="sxs-lookup"><span data-stu-id="aa131-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="aa131-105">`GetTime`方法會抓取這個範例開始和完成的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="aa131-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="aa131-106">這個方法會實 [**IMediaSample：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) 方法。</span><span class="sxs-lookup"><span data-stu-id="aa131-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa131-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa131-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="aa131-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa131-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa131-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="aa131-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="aa131-110">接收開始資料流程時間之變數的指標，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="aa131-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="aa131-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="aa131-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="aa131-112">接收結束資料流程時間之變數的指標，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="aa131-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="aa131-113">如果範例沒有停止時間，此值會設定為開始時間加一。</span><span class="sxs-lookup"><span data-stu-id="aa131-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa131-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa131-114">Return value</span></span>

<span data-ttu-id="aa131-115">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="aa131-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="aa131-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aa131-116">Return code</span></span>                                                                                                   | <span data-ttu-id="aa131-117">Description</span><span class="sxs-lookup"><span data-stu-id="aa131-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="aa131-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="aa131-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="aa131-119">成功。</span><span class="sxs-lookup"><span data-stu-id="aa131-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="aa131-120"><dt>**VFW \_ S \_ 沒有 \_ 停止 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="aa131-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="aa131-121">範例有有效的開始時間，但沒有停止時間。</span><span class="sxs-lookup"><span data-stu-id="aa131-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="aa131-122"><dt>**\_ \_ \_ \_ 未設定 VFW E 取樣 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="aa131-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="aa131-123">範例沒有有效的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="aa131-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="aa131-124">備註</span><span class="sxs-lookup"><span data-stu-id="aa131-124">Remarks</span></span>

<span data-ttu-id="aa131-125">[**CMediaSample：： m \_ Start**](cmediasample-m-start.md)和 [**CMediaSample：： m \_ End**](cmediasample-m-end.md)成員變數會指定時間戳記。</span><span class="sxs-lookup"><span data-stu-id="aa131-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="aa131-126">[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定時間戳記是否有效。</span><span class="sxs-lookup"><span data-stu-id="aa131-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="aa131-127">如需時間戳記的詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="aa131-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa131-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa131-128">Requirements</span></span>



| <span data-ttu-id="aa131-129">需求</span><span class="sxs-lookup"><span data-stu-id="aa131-129">Requirement</span></span> | <span data-ttu-id="aa131-130">值</span><span class="sxs-lookup"><span data-stu-id="aa131-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa131-131">標頭</span><span class="sxs-lookup"><span data-stu-id="aa131-131">Header</span></span><br/>  | <dl> <span data-ttu-id="aa131-132"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="aa131-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aa131-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="aa131-133">Library</span></span><br/> | <dl> <span data-ttu-id="aa131-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="aa131-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa131-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa131-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa131-136">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="aa131-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




