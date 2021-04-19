---
description: StreamTime 方法會抓取目前的資料流程時間。
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: 'CBaseFilter. StreamTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987901"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="0326c-103">CBaseFilter. StreamTime 方法</span><span class="sxs-lookup"><span data-stu-id="0326c-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="0326c-104">**StreamTime** 方法會抓取目前的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="0326c-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="0326c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0326c-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="0326c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0326c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0326c-107">*rtStream* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="0326c-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0326c-108">[**CRefTime**](creftime.md)物件的參考，該物件會接收目前的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="0326c-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0326c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0326c-109">Return value</span></span>

<span data-ttu-id="0326c-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0326c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0326c-111">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="0326c-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0326c-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0326c-112">Return code</span></span>                                                                                      | <span data-ttu-id="0326c-113">Description</span><span class="sxs-lookup"><span data-stu-id="0326c-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="0326c-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0326c-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="0326c-115">成功。</span><span class="sxs-lookup"><span data-stu-id="0326c-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="0326c-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="0326c-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="0326c-117">沒有可用的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="0326c-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0326c-118">備註</span><span class="sxs-lookup"><span data-stu-id="0326c-118">Remarks</span></span>

<span data-ttu-id="0326c-119">資料流程時間定義為目前的參考時間 (如參考時鐘所指定) 減去 [**CBaseFilter：： m \_ tStart**](cbasefilter-m-tstart.md)) 所指定的開始時間 (。</span><span class="sxs-lookup"><span data-stu-id="0326c-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="0326c-120">媒體範例的 *時間戳記* 會指定應呈現的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="0326c-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="0326c-121">如果時間戳記小於目前資料流程時間的樣本尚未轉譯，則會延遲。</span><span class="sxs-lookup"><span data-stu-id="0326c-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="0326c-122">這個方法會藉由呼叫 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 取得目前的參考時間，然後減去初始開始時間，來取得資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="0326c-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="0326c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0326c-123">Requirements</span></span>



| <span data-ttu-id="0326c-124">需求</span><span class="sxs-lookup"><span data-stu-id="0326c-124">Requirement</span></span> | <span data-ttu-id="0326c-125">值</span><span class="sxs-lookup"><span data-stu-id="0326c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0326c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0326c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0326c-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0326c-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0326c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="0326c-128">Library</span></span><br/> | <dl> <span data-ttu-id="0326c-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0326c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0326c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0326c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0326c-131">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="0326c-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0326c-132">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="0326c-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




