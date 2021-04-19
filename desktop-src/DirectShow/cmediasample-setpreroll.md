---
description: SetPreroll 方法會指定此範例是否為可提前取樣。 不應顯示預先提供的範例。 這個方法會實 IMediaSample：： SetPreroll 方法。
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: 'CMediaSample. SetPreroll 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977428"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="f3b06-105">CMediaSample. SetPreroll 方法</span><span class="sxs-lookup"><span data-stu-id="f3b06-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="f3b06-106">`SetPreroll`方法會指定此範例是否為可提前取樣。</span><span class="sxs-lookup"><span data-stu-id="f3b06-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="f3b06-107">不應顯示預先提供的範例。</span><span class="sxs-lookup"><span data-stu-id="f3b06-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="f3b06-108">這個方法會實 [**IMediaSample：： SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) 方法。</span><span class="sxs-lookup"><span data-stu-id="f3b06-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b06-109">語法</span><span class="sxs-lookup"><span data-stu-id="f3b06-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="f3b06-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3b06-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b06-111">*bIsPreroll*</span><span class="sxs-lookup"><span data-stu-id="f3b06-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b06-112">布林值，指定這是否為可提前取樣。</span><span class="sxs-lookup"><span data-stu-id="f3b06-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="f3b06-113">若 **為 TRUE**，表示此為預先設置的範例。</span><span class="sxs-lookup"><span data-stu-id="f3b06-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b06-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3b06-114">Return value</span></span>

<span data-ttu-id="f3b06-115">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f3b06-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b06-116">備註</span><span class="sxs-lookup"><span data-stu-id="f3b06-116">Remarks</span></span>

<span data-ttu-id="f3b06-117">這個方法會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定預先執行的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3b06-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b06-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3b06-118">Requirements</span></span>



| <span data-ttu-id="f3b06-119">需求</span><span class="sxs-lookup"><span data-stu-id="f3b06-119">Requirement</span></span> | <span data-ttu-id="f3b06-120">值</span><span class="sxs-lookup"><span data-stu-id="f3b06-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b06-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f3b06-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f3b06-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f3b06-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f3b06-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3b06-123">Library</span></span><br/> | <dl> <span data-ttu-id="f3b06-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f3b06-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b06-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3b06-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b06-126">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="f3b06-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




