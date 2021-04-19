---
description: GetMediaType 方法會捕獲慣用的媒體類型。
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: CSourceStream. GetMediaType 方法 (Source .h) -pMediaType 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106995135"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="0e405-103">CSourceStream. GetMediaType 方法 (Source .h) </span><span class="sxs-lookup"><span data-stu-id="0e405-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="0e405-104">`GetMediaType`方法會捕獲慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0e405-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e405-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e405-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="0e405-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e405-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e405-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="0e405-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="0e405-108">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0e405-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e405-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e405-109">Return value</span></span>

<span data-ttu-id="0e405-110">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0e405-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="0e405-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0e405-111">Return code</span></span>                                                                                            | <span data-ttu-id="0e405-112">Description</span><span class="sxs-lookup"><span data-stu-id="0e405-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0e405-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0e405-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="0e405-114">成功。</span><span class="sxs-lookup"><span data-stu-id="0e405-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="0e405-115"><dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt></span><span class="sxs-lookup"><span data-stu-id="0e405-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="0e405-116">索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="0e405-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="0e405-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e405-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="0e405-118">索引小於零。</span><span class="sxs-lookup"><span data-stu-id="0e405-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="0e405-119"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="0e405-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="0e405-120">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0e405-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="0e405-121">備註</span><span class="sxs-lookup"><span data-stu-id="0e405-121">Remarks</span></span>

<span data-ttu-id="0e405-122">此方法有兩個版本。</span><span class="sxs-lookup"><span data-stu-id="0e405-122">There are two versions of this method.</span></span> <span data-ttu-id="0e405-123">其中一個版本會覆寫 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法，並接受索引值做為參數。</span><span class="sxs-lookup"><span data-stu-id="0e405-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="0e405-124">另一個版本是設計來取得單一媒體類型，因此它缺少索引參數。</span><span class="sxs-lookup"><span data-stu-id="0e405-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="0e405-125">單一參數方法會傳回 E 未 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="0e405-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="0e405-126">雙參數方法會驗證 *ipositionsummaryview* 參數是否為零，然後呼叫單一參數版本。</span><span class="sxs-lookup"><span data-stu-id="0e405-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="0e405-127">根據 pin 所支援的媒體類型數目，您必須覆寫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="0e405-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="0e405-128">如果 pin 只支援一種媒體類型，請覆寫單一參數版本。</span><span class="sxs-lookup"><span data-stu-id="0e405-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="0e405-129">填入釘選支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0e405-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="0e405-130">如果 pin 支援一個以上的媒體類型，請覆寫兩個參數的版本。</span><span class="sxs-lookup"><span data-stu-id="0e405-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="0e405-131">也覆寫 [**CSourceStream：： CheckMediaType**](csourcestream-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0e405-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e405-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e405-132">Requirements</span></span>



| <span data-ttu-id="0e405-133">需求</span><span class="sxs-lookup"><span data-stu-id="0e405-133">Requirement</span></span> | <span data-ttu-id="0e405-134">值</span><span class="sxs-lookup"><span data-stu-id="0e405-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e405-135">標頭</span><span class="sxs-lookup"><span data-stu-id="0e405-135">Header</span></span><br/>  | <dl> <span data-ttu-id="0e405-136"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="0e405-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0e405-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e405-137">Library</span></span><br/> | <dl> <span data-ttu-id="0e405-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0e405-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e405-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e405-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e405-140">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="0e405-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




