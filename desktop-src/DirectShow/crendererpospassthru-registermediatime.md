---
description: RegisterMediaTime 方法會快取目前範例中的時間戳記。
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: 'CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) '
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
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977681"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="319a2-103">CRendererPosPassThru. RegisterMediaTime 方法 (Ctlutil .h) </span><span class="sxs-lookup"><span data-stu-id="319a2-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="319a2-104">**RegisterMediaTime** 方法會快取目前範例中的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="319a2-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="319a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="319a2-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="319a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="319a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="319a2-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="319a2-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="319a2-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="319a2-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="319a2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="319a2-109">Return value</span></span>

<span data-ttu-id="319a2-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="319a2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="319a2-111">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="319a2-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="319a2-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="319a2-112">Return code</span></span>                                                                                                  | <span data-ttu-id="319a2-113">Description</span><span class="sxs-lookup"><span data-stu-id="319a2-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="319a2-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="319a2-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="319a2-115">成功。</span><span class="sxs-lookup"><span data-stu-id="319a2-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="319a2-116"><dt>**\_ \_ \_ \_ 未設定 VFW E 媒體 \_ 時間**</dt></span><span class="sxs-lookup"><span data-stu-id="319a2-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="319a2-117">此範例不會加上時間戳記。</span><span class="sxs-lookup"><span data-stu-id="319a2-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="319a2-118">備註</span><span class="sxs-lookup"><span data-stu-id="319a2-118">Remarks</span></span>

<span data-ttu-id="319a2-119">這個方法會儲存目前範例中的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="319a2-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="319a2-120">[**CRendererPosPassThru：： GetMediaTime**](crendererpospassthru-getmediatime.md)方法會抓取相同的值。</span><span class="sxs-lookup"><span data-stu-id="319a2-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="319a2-121">篩選應該針對它收到的每個範例呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="319a2-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="319a2-122">方法會多載，以接受範例的指標或時間戳記值本身。</span><span class="sxs-lookup"><span data-stu-id="319a2-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="319a2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="319a2-123">Requirements</span></span>



| <span data-ttu-id="319a2-124">需求</span><span class="sxs-lookup"><span data-stu-id="319a2-124">Requirement</span></span> | <span data-ttu-id="319a2-125">值</span><span class="sxs-lookup"><span data-stu-id="319a2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="319a2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="319a2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="319a2-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="319a2-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="319a2-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="319a2-128">Library</span></span><br/> | <dl> <span data-ttu-id="319a2-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="319a2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




