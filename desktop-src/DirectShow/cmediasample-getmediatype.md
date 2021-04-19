---
description: 如果媒體類型與先前的範例不同，則 GetMediaType 方法會抓取媒體類型。 這個方法會實 IMediaSample：： GetMediaType 方法。
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: 'CMediaSample. GetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990572"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="6a7af-104">CMediaSample. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="6a7af-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="6a7af-105">`GetMediaType`如果媒體類型與先前的範例不同，則方法會抓取媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6a7af-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="6a7af-106">這個方法會實 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="6a7af-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7af-107">語法</span><span class="sxs-lookup"><span data-stu-id="6a7af-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="6a7af-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a7af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a7af-109">*ppMediaType*</span><span class="sxs-lookup"><span data-stu-id="6a7af-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="6a7af-110">接收 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="6a7af-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="6a7af-111">如果媒體類型尚未從上一個範例變更， *\* ppMediaType* 會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6a7af-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a7af-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a7af-112">Return value</span></span>

<span data-ttu-id="6a7af-113">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6a7af-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6a7af-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a7af-114">Return code</span></span>                                                                                   | <span data-ttu-id="6a7af-115">Description</span><span class="sxs-lookup"><span data-stu-id="6a7af-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a7af-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7af-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="6a7af-117">媒體類型尚未從上一個範例變更。</span><span class="sxs-lookup"><span data-stu-id="6a7af-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="6a7af-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7af-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6a7af-119">成功。</span><span class="sxs-lookup"><span data-stu-id="6a7af-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="6a7af-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7af-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6a7af-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6a7af-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="6a7af-122">備註</span><span class="sxs-lookup"><span data-stu-id="6a7af-122">Remarks</span></span>

<span data-ttu-id="6a7af-123">當您完成媒體類型時，請呼叫 [**DeleteMediaType**](deletemediatype.md) 公用程式函式來釋放記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="6a7af-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="6a7af-124">[**CMediaSample：： m \_ pMediaType**](cmediasample-m-pmediatype.md)成員變數會指定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6a7af-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="6a7af-125">[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數指定媒體類型是否已變更。</span><span class="sxs-lookup"><span data-stu-id="6a7af-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a7af-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a7af-126">Requirements</span></span>



| <span data-ttu-id="6a7af-127">需求</span><span class="sxs-lookup"><span data-stu-id="6a7af-127">Requirement</span></span> | <span data-ttu-id="6a7af-128">值</span><span class="sxs-lookup"><span data-stu-id="6a7af-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7af-129">標頭</span><span class="sxs-lookup"><span data-stu-id="6a7af-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6a7af-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6a7af-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6a7af-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a7af-131">Library</span></span><br/> | <dl> <span data-ttu-id="6a7af-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6a7af-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7af-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a7af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7af-134">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="6a7af-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




