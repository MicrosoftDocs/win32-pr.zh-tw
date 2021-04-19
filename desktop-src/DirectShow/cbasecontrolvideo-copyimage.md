---
description: 建立映射的記憶體複本。
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: 'CBaseControlVideo. CopyImage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990613"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="68bd7-103">CBaseControlVideo. CopyImage 方法</span><span class="sxs-lookup"><span data-stu-id="68bd7-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="68bd7-104">建立映射的記憶體複本。</span><span class="sxs-lookup"><span data-stu-id="68bd7-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="68bd7-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="68bd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="68bd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68bd7-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="68bd7-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="68bd7-108">包含影片影像之範例的指標。</span><span class="sxs-lookup"><span data-stu-id="68bd7-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="68bd7-109">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="68bd7-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="68bd7-110">代表影片影像的格式指標。</span><span class="sxs-lookup"><span data-stu-id="68bd7-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="68bd7-111">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="68bd7-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="68bd7-112">輸出緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="68bd7-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="68bd7-113">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="68bd7-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="68bd7-114">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="68bd7-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="68bd7-115">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="68bd7-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="68bd7-116">來源影片矩形的指標。</span><span class="sxs-lookup"><span data-stu-id="68bd7-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68bd7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="68bd7-117">Return value</span></span>

<span data-ttu-id="68bd7-118">如果 *pVideoImage* 參數為 **Null**，則會以輸出緩衝區儲存影像所需的位元組數填入 *pBufferSize* 參數。</span><span class="sxs-lookup"><span data-stu-id="68bd7-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="68bd7-119">如果傳入的緩衝區太小，或成員函式無法配置足夠的記憶體，則成員函式會傳回 E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="68bd7-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bd7-120">備註</span><span class="sxs-lookup"><span data-stu-id="68bd7-120">Remarks</span></span>

<span data-ttu-id="68bd7-121">成員函式會從範例抓取影像，並將它複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="68bd7-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="68bd7-122">複製到輸出緩衝區的影片區段會反映透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面設定的來源矩形 (但不會反映) 的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="68bd7-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="68bd7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="68bd7-123">Requirements</span></span>



| <span data-ttu-id="68bd7-124">需求</span><span class="sxs-lookup"><span data-stu-id="68bd7-124">Requirement</span></span> | <span data-ttu-id="68bd7-125">值</span><span class="sxs-lookup"><span data-stu-id="68bd7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68bd7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="68bd7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="68bd7-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68bd7-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68bd7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="68bd7-128">Library</span></span><br/> | <dl> <span data-ttu-id="68bd7-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="68bd7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bd7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68bd7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bd7-131">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="68bd7-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




