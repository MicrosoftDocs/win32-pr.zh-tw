---
description: GetMediaType 方法會捕獲慣用的媒體類型。 這個方法會使用 *ipositionsummaryview* 和 *pMediaType* 參數。
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: CSourceStream. GetMediaType 方法 (Source .h) -Ipositionsummaryview 和 pMediaType 參數
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106998692"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="924b0-104">CSourceStream. GetMediaType 方法 (Source .h) -Ipositionsummaryview 和 pMediaType 參數</span><span class="sxs-lookup"><span data-stu-id="924b0-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="924b0-105">**GetMediaType** 方法會捕獲慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="924b0-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="924b0-106">語法</span><span class="sxs-lookup"><span data-stu-id="924b0-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="924b0-107">參數</span><span class="sxs-lookup"><span data-stu-id="924b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="924b0-108">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="924b0-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="924b0-109">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="924b0-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="924b0-110">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="924b0-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="924b0-111">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="924b0-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="924b0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="924b0-112">Return value</span></span>

<span data-ttu-id="924b0-113">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="924b0-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="924b0-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="924b0-114">Return code</span></span>                                                                                            | <span data-ttu-id="924b0-115">Description</span><span class="sxs-lookup"><span data-stu-id="924b0-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="924b0-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="924b0-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="924b0-117">成功。</span><span class="sxs-lookup"><span data-stu-id="924b0-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="924b0-118"><dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt></span><span class="sxs-lookup"><span data-stu-id="924b0-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="924b0-119">索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="924b0-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="924b0-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="924b0-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="924b0-121">索引小於零。</span><span class="sxs-lookup"><span data-stu-id="924b0-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="924b0-122"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="924b0-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="924b0-123">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="924b0-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="924b0-124">備註</span><span class="sxs-lookup"><span data-stu-id="924b0-124">Remarks</span></span>

<span data-ttu-id="924b0-125">此方法有兩個版本。</span><span class="sxs-lookup"><span data-stu-id="924b0-125">There are two versions of this method.</span></span> <span data-ttu-id="924b0-126">其中一個版本會覆寫 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法，並接受索引值做為參數。</span><span class="sxs-lookup"><span data-stu-id="924b0-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="924b0-127">另一個版本是設計來取得單一媒體類型，因此它缺少索引參數。</span><span class="sxs-lookup"><span data-stu-id="924b0-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="924b0-128">單一參數方法會傳回 E 未 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="924b0-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="924b0-129">雙參數方法會驗證 *ipositionsummaryview* 參數是否為零，然後呼叫單一參數版本。</span><span class="sxs-lookup"><span data-stu-id="924b0-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="924b0-130">根據 pin 所支援的媒體類型數目，您必須覆寫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="924b0-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="924b0-131">如果 pin 只支援一種媒體類型，請覆寫單一參數版本。</span><span class="sxs-lookup"><span data-stu-id="924b0-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="924b0-132">填入釘選支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="924b0-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="924b0-133">如果 pin 支援一個以上的媒體類型，請覆寫兩個參數的版本。</span><span class="sxs-lookup"><span data-stu-id="924b0-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="924b0-134">也覆寫 [**CSourceStream：： CheckMediaType**](csourcestream-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="924b0-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="924b0-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="924b0-135">Requirements</span></span>



| <span data-ttu-id="924b0-136">需求</span><span class="sxs-lookup"><span data-stu-id="924b0-136">Requirement</span></span> | <span data-ttu-id="924b0-137">值</span><span class="sxs-lookup"><span data-stu-id="924b0-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="924b0-138">標頭</span><span class="sxs-lookup"><span data-stu-id="924b0-138">Header</span></span>  | <span data-ttu-id="924b0-139">來源 .h (包含) 的資料流程</span><span class="sxs-lookup"><span data-stu-id="924b0-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="924b0-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="924b0-140">Library</span></span> | <span data-ttu-id="924b0-141"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="924b0-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="924b0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="924b0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="924b0-143">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="924b0-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




