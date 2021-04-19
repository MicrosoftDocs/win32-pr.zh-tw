---
description: 轉換方法會轉換輸入範例，以產生輸出範例。
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: 'CTransformFilter 轉換方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990166"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="c131e-103">CTransformFilter 轉換方法</span><span class="sxs-lookup"><span data-stu-id="c131e-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="c131e-104">`Transform`方法會轉換輸入範例，以產生輸出範例。</span><span class="sxs-lookup"><span data-stu-id="c131e-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="c131e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c131e-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="c131e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c131e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c131e-107">*針*</span><span class="sxs-lookup"><span data-stu-id="c131e-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="c131e-108">輸入範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c131e-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c131e-109">*彆扭*</span><span class="sxs-lookup"><span data-stu-id="c131e-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="c131e-110">輸出範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c131e-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c131e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c131e-111">Return value</span></span>

<span data-ttu-id="c131e-112">基類傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="c131e-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="c131e-113">衍生類別應該會傳回 **HRESULT** 值，表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="c131e-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="c131e-114">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="c131e-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c131e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c131e-115">Return code</span></span>                                                                             | <span data-ttu-id="c131e-116">Description</span><span class="sxs-lookup"><span data-stu-id="c131e-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="c131e-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c131e-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c131e-118">請勿傳遞此範例。</span><span class="sxs-lookup"><span data-stu-id="c131e-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="c131e-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c131e-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c131e-120">成功。</span><span class="sxs-lookup"><span data-stu-id="c131e-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c131e-121">備註</span><span class="sxs-lookup"><span data-stu-id="c131e-121">Remarks</span></span>

<span data-ttu-id="c131e-122">覆寫此方法以產生輸出資料。</span><span class="sxs-lookup"><span data-stu-id="c131e-122">Override this method to produce output data.</span></span> <span data-ttu-id="c131e-123">從 *pIn* 參數所指定的範例讀取輸入資料，並將新的資料寫入 *不悅* 參數所指定的範例中。</span><span class="sxs-lookup"><span data-stu-id="c131e-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="c131e-124">在篩選準則呼叫這個方法之前，它會將屬性從輸入範例複製到輸出範例。</span><span class="sxs-lookup"><span data-stu-id="c131e-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="c131e-125">`Transform`方法應該使用 **IMediaSample** 方法或 [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)介面 (（如果有) 的話），來設定兩個範例之間有差異的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c131e-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="c131e-126">如果篩選器不應該傳遞此範例 (例如，為了支援品質控制) ，此方法應該會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="c131e-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c131e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c131e-127">Requirements</span></span>



| <span data-ttu-id="c131e-128">需求</span><span class="sxs-lookup"><span data-stu-id="c131e-128">Requirement</span></span> | <span data-ttu-id="c131e-129">值</span><span class="sxs-lookup"><span data-stu-id="c131e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c131e-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c131e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c131e-131"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c131e-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c131e-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="c131e-132">Library</span></span><br/> | <dl> <span data-ttu-id="c131e-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c131e-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c131e-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c131e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c131e-135">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c131e-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




