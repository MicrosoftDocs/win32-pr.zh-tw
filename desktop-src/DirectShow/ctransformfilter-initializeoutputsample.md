---
description: InitializeOutputSample 方法會捕獲新的輸出範例，並將它初始化。
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: " (Transfrm 的 CTransformFilter.InitializeOutputSample 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995956"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="4755e-103">CTransformFilter.InitializeOutputSample 方法</span><span class="sxs-lookup"><span data-stu-id="4755e-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="4755e-104">`InitializeOutputSample`方法會抓取新的輸出範例，並將其初始化。</span><span class="sxs-lookup"><span data-stu-id="4755e-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4755e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4755e-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="4755e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4755e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4755e-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="4755e-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4755e-108">輸入範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4755e-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4755e-109">*ppOutSample*</span><span class="sxs-lookup"><span data-stu-id="4755e-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4755e-110">接收輸出範例 **IMediaSample** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4755e-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4755e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4755e-111">Return value</span></span>

<span data-ttu-id="4755e-112">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4755e-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4755e-113">備註</span><span class="sxs-lookup"><span data-stu-id="4755e-113">Remarks</span></span>

<span data-ttu-id="4755e-114">[**CTransformFilter：： Receive**](ctransformfilter-receive.md)方法會呼叫這個方法來準備輸出範例。</span><span class="sxs-lookup"><span data-stu-id="4755e-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="4755e-115">一般而言，您不需要在衍生類別中呼叫這個方法，除非您覆寫 **Receive** 方法。</span><span class="sxs-lookup"><span data-stu-id="4755e-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="4755e-116">這個方法會從輸出釘選配置器抓取新的範例。</span><span class="sxs-lookup"><span data-stu-id="4755e-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="4755e-117">然後，它會將範例屬性從輸入範例複製到輸出範例。</span><span class="sxs-lookup"><span data-stu-id="4755e-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="4755e-118">範例屬性是在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) 結構中定義。</span><span class="sxs-lookup"><span data-stu-id="4755e-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4755e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4755e-119">Requirements</span></span>



| <span data-ttu-id="4755e-120">需求</span><span class="sxs-lookup"><span data-stu-id="4755e-120">Requirement</span></span> | <span data-ttu-id="4755e-121">值</span><span class="sxs-lookup"><span data-stu-id="4755e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4755e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4755e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4755e-123"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4755e-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4755e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="4755e-124">Library</span></span><br/> | <dl> <span data-ttu-id="4755e-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4755e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4755e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4755e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4755e-127">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4755e-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




