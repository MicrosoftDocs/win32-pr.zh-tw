---
description: GetMediaTime 方法會捕獲此範例的媒體時間。 這個方法會實 IMediaSample：： GetMediaTime 方法。
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: 'CMediaSample. GetMediaTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994228"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="8d299-104">CMediaSample. GetMediaTime 方法</span><span class="sxs-lookup"><span data-stu-id="8d299-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="8d299-105">`GetMediaTime`方法會捕獲此範例的媒體時間。</span><span class="sxs-lookup"><span data-stu-id="8d299-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="8d299-106">這個方法會實 [**IMediaSample：： GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) 方法。</span><span class="sxs-lookup"><span data-stu-id="8d299-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d299-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d299-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="8d299-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d299-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d299-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="8d299-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="8d299-110">接收媒體開始時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="8d299-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="8d299-111">*暫止*</span><span class="sxs-lookup"><span data-stu-id="8d299-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8d299-112">接收媒體停止時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="8d299-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d299-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d299-113">Return value</span></span>

<span data-ttu-id="8d299-114">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8d299-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8d299-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8d299-115">Return code</span></span>                                                                                                  | <span data-ttu-id="8d299-116">Description</span><span class="sxs-lookup"><span data-stu-id="8d299-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="8d299-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8d299-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="8d299-118">成功。</span><span class="sxs-lookup"><span data-stu-id="8d299-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8d299-119"><dt>**\_ \_ \_ \_ 未設定 VFW E 媒體 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="8d299-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="8d299-120">未設定此範例的媒體時間。</span><span class="sxs-lookup"><span data-stu-id="8d299-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8d299-121">備註</span><span class="sxs-lookup"><span data-stu-id="8d299-121">Remarks</span></span>

<span data-ttu-id="8d299-122">[**CMediaSample：： m \_ MediaEnd**](cmediasample-m-mediaend.md)成員變數會指定從 [**CMediaSample：： m \_ MediaStart**](cmediasample-m-mediastart.md)的位移，但由 *暫* 止參數接收的值是絕對媒體時間，以 **m \_ MediaStart**  +  **m \_ MediaEnd** 計算。</span><span class="sxs-lookup"><span data-stu-id="8d299-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="8d299-123">如需媒體時間的相關資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="8d299-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d299-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d299-124">Requirements</span></span>



| <span data-ttu-id="8d299-125">需求</span><span class="sxs-lookup"><span data-stu-id="8d299-125">Requirement</span></span> | <span data-ttu-id="8d299-126">值</span><span class="sxs-lookup"><span data-stu-id="8d299-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d299-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8d299-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8d299-128"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8d299-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8d299-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d299-129">Library</span></span><br/> | <dl> <span data-ttu-id="8d299-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8d299-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d299-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d299-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d299-132">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="8d299-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




