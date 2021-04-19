---
description: SetMediaType 方法會設定範例的媒體類型。 這個方法會實 IMediaSample：： SetMediaType 方法。
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: 'CMediaSample. SetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977429"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="d97a8-104">CMediaSample. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="d97a8-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="d97a8-105">`SetMediaType`方法會設定範例的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d97a8-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="d97a8-106">這個方法會實 [**IMediaSample：： SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="d97a8-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="d97a8-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d97a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="d97a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97a8-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="d97a8-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d97a8-110">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d97a8-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97a8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d97a8-111">Return value</span></span>

<span data-ttu-id="d97a8-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d97a8-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d97a8-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d97a8-113">Return code</span></span>                                                                                   | <span data-ttu-id="d97a8-114">Description</span><span class="sxs-lookup"><span data-stu-id="d97a8-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="d97a8-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d97a8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d97a8-116">Success</span><span class="sxs-lookup"><span data-stu-id="d97a8-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="d97a8-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d97a8-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d97a8-118">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="d97a8-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d97a8-119">備註</span><span class="sxs-lookup"><span data-stu-id="d97a8-119">Remarks</span></span>

<span data-ttu-id="d97a8-120">這個方法會設定 [**CMediaSample：： m \_ pMediaType**](cmediasample-m-pmediatype.md) 成員變數（指定媒體類型），以及指定媒體類型是否已變更的 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="d97a8-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="d97a8-121">這個方法會複製 AM \_ 媒體 \_ 類型結構。</span><span class="sxs-lookup"><span data-stu-id="d97a8-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97a8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d97a8-122">Requirements</span></span>



| <span data-ttu-id="d97a8-123">需求</span><span class="sxs-lookup"><span data-stu-id="d97a8-123">Requirement</span></span> | <span data-ttu-id="d97a8-124">值</span><span class="sxs-lookup"><span data-stu-id="d97a8-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d97a8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d97a8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d97a8-126"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d97a8-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d97a8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d97a8-127">Library</span></span><br/> | <dl> <span data-ttu-id="d97a8-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d97a8-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d97a8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d97a8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d97a8-130">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="d97a8-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




