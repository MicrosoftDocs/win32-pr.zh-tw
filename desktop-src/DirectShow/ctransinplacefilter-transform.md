---
description: 轉換方法會就地轉換範例。
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: 'CTransInPlaceFilter 轉換方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991357"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="a8d69-103">CTransInPlaceFilter 轉換方法</span><span class="sxs-lookup"><span data-stu-id="a8d69-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="a8d69-104">`Transform`方法會就地轉換範例。</span><span class="sxs-lookup"><span data-stu-id="a8d69-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d69-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8d69-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a8d69-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8d69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d69-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="a8d69-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d69-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a8d69-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d69-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8d69-109">Return value</span></span>

<span data-ttu-id="a8d69-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a8d69-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a8d69-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="a8d69-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a8d69-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a8d69-112">Return code</span></span>                                                                             | <span data-ttu-id="a8d69-113">Description</span><span class="sxs-lookup"><span data-stu-id="a8d69-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="a8d69-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a8d69-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a8d69-115">請勿傳遞此範例。</span><span class="sxs-lookup"><span data-stu-id="a8d69-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="a8d69-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a8d69-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a8d69-117">成功。</span><span class="sxs-lookup"><span data-stu-id="a8d69-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a8d69-118">備註</span><span class="sxs-lookup"><span data-stu-id="a8d69-118">Remarks</span></span>

<span data-ttu-id="a8d69-119">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="a8d69-119">The derived class must implement this method.</span></span> <span data-ttu-id="a8d69-120">就地轉換範例資料。</span><span class="sxs-lookup"><span data-stu-id="a8d69-120">Transform the sample data in place.</span></span> <span data-ttu-id="a8d69-121">如果篩選準則使用兩個配置器，它會將輸入範例中的資料複製到新的範例，並將該複本傳遞給這個方法。</span><span class="sxs-lookup"><span data-stu-id="a8d69-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="a8d69-122">如果篩選器不應該傳遞此範例 (例如，為了支援品質控制) ，此方法應該會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="a8d69-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d69-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8d69-123">Requirements</span></span>



| <span data-ttu-id="a8d69-124">需求</span><span class="sxs-lookup"><span data-stu-id="a8d69-124">Requirement</span></span> | <span data-ttu-id="a8d69-125">值</span><span class="sxs-lookup"><span data-stu-id="a8d69-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d69-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a8d69-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a8d69-127"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a8d69-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8d69-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8d69-128">Library</span></span><br/> | <dl> <span data-ttu-id="a8d69-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a8d69-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d69-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8d69-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d69-131">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="a8d69-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




