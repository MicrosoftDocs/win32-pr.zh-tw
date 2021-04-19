---
description: IsPreroll 方法會判斷此範例是否為可提前取樣。 不應顯示預先提供的範例。 這個方法會實 IMediaSample：： IsPreroll 方法。
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: 'CMediaSample. IsPreroll 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995915"
---
# <a name="cmediasampleispreroll-method"></a><span data-ttu-id="f3206-105">CMediaSample. IsPreroll 方法</span><span class="sxs-lookup"><span data-stu-id="f3206-105">CMediaSample.IsPreroll method</span></span>

<span data-ttu-id="f3206-106">`IsPreroll`方法會判斷此範例是否為可提前取樣。</span><span class="sxs-lookup"><span data-stu-id="f3206-106">The `IsPreroll` method determines if this sample is a preroll sample.</span></span> <span data-ttu-id="f3206-107">不應顯示預先提供的範例。</span><span class="sxs-lookup"><span data-stu-id="f3206-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="f3206-108">這個方法會實 [**IMediaSample：： IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) 方法。</span><span class="sxs-lookup"><span data-stu-id="f3206-108">This method implements the [**IMediaSample::IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3206-109">語法</span><span class="sxs-lookup"><span data-stu-id="f3206-109">Syntax</span></span>


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a><span data-ttu-id="f3206-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3206-110">Parameters</span></span>

<span data-ttu-id="f3206-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f3206-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3206-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3206-112">Return value</span></span>

<span data-ttu-id="f3206-113">\_如果此範例是一個預先進行的範例，則傳回 [確定]， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="f3206-113">Returns S\_OK if the sample is a preroll sample, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3206-114">備註</span><span class="sxs-lookup"><span data-stu-id="f3206-114">Remarks</span></span>

<span data-ttu-id="f3206-115">[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f3206-115">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3206-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3206-116">Requirements</span></span>



| <span data-ttu-id="f3206-117">需求</span><span class="sxs-lookup"><span data-stu-id="f3206-117">Requirement</span></span> | <span data-ttu-id="f3206-118">值</span><span class="sxs-lookup"><span data-stu-id="f3206-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3206-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f3206-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f3206-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f3206-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f3206-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3206-121">Library</span></span><br/> | <dl> <span data-ttu-id="f3206-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f3206-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3206-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3206-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3206-124">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="f3206-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




