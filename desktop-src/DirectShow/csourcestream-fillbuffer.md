---
description: FillBuffer 方法會以資料填滿媒體範例。
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: 'CSourceStream. FillBuffer 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989561"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="004a7-103">CSourceStream. FillBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="004a7-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="004a7-104">`FillBuffer`方法會以資料填滿媒體範例。</span><span class="sxs-lookup"><span data-stu-id="004a7-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="004a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="004a7-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="004a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="004a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004a7-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="004a7-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="004a7-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="004a7-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004a7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="004a7-109">Return value</span></span>

<span data-ttu-id="004a7-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="004a7-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="004a7-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="004a7-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="004a7-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="004a7-112">Return code</span></span>                                                                             | <span data-ttu-id="004a7-113">Description</span><span class="sxs-lookup"><span data-stu-id="004a7-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="004a7-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="004a7-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="004a7-115">資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="004a7-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="004a7-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="004a7-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="004a7-117">Success</span><span class="sxs-lookup"><span data-stu-id="004a7-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="004a7-118">備註</span><span class="sxs-lookup"><span data-stu-id="004a7-118">Remarks</span></span>

<span data-ttu-id="004a7-119">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="004a7-119">The derived class must implement this method.</span></span>

<span data-ttu-id="004a7-120">提供給這個方法的媒體範例沒有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="004a7-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="004a7-121">衍生類別應該呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法來設定時間戳記。</span><span class="sxs-lookup"><span data-stu-id="004a7-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="004a7-122">如果適用于媒體類型，則衍生類別也應該透過呼叫 [**IMediaSample：： SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) 方法來設定媒體時間。</span><span class="sxs-lookup"><span data-stu-id="004a7-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="004a7-123">如需詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="004a7-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="004a7-124">在 \_ 資料流程結尾傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="004a7-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="004a7-125">這會導致 **CSourceStream** 類別傳送資料流程結束通知，並中止緩衝區處理迴圈。</span><span class="sxs-lookup"><span data-stu-id="004a7-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="004a7-126">如需詳細資訊，請參閱 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 。</span><span class="sxs-lookup"><span data-stu-id="004a7-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="004a7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="004a7-127">Requirements</span></span>



| <span data-ttu-id="004a7-128">需求</span><span class="sxs-lookup"><span data-stu-id="004a7-128">Requirement</span></span> | <span data-ttu-id="004a7-129">值</span><span class="sxs-lookup"><span data-stu-id="004a7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="004a7-130">標頭</span><span class="sxs-lookup"><span data-stu-id="004a7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="004a7-131"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="004a7-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="004a7-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="004a7-132">Library</span></span><br/> | <dl> <span data-ttu-id="004a7-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="004a7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="004a7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="004a7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004a7-135">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="004a7-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




