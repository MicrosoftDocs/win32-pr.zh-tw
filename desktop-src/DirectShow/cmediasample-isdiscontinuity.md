---
description: IsDiscontinuity 方法會判斷此範例是否表示資料流程中的中斷。 這個方法會實 IMediaSample：： IsDiscontinuity 方法。
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: 'CMediaSample. IsDiscontinuity 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982923"
---
# <a name="cmediasampleisdiscontinuity-method"></a><span data-ttu-id="c8dfc-104">CMediaSample. IsDiscontinuity 方法</span><span class="sxs-lookup"><span data-stu-id="c8dfc-104">CMediaSample.IsDiscontinuity method</span></span>

<span data-ttu-id="c8dfc-105">`IsDiscontinuity`方法會判斷此範例是否代表資料流程中的中斷點。</span><span class="sxs-lookup"><span data-stu-id="c8dfc-105">The `IsDiscontinuity` method determines if this sample represents a break in the data stream.</span></span> <span data-ttu-id="c8dfc-106">這個方法會實 [**IMediaSample：： IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) 方法。</span><span class="sxs-lookup"><span data-stu-id="c8dfc-106">This method implements the [**IMediaSample::IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8dfc-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8dfc-107">Syntax</span></span>


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a><span data-ttu-id="c8dfc-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8dfc-108">Parameters</span></span>

<span data-ttu-id="c8dfc-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c8dfc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8dfc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8dfc-110">Return value</span></span>

<span data-ttu-id="c8dfc-111">\_如果範例是資料流程中的中斷，則傳回 s OK， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="c8dfc-111">Returns S\_OK if the sample is a break in the data stream, and S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8dfc-112">備註</span><span class="sxs-lookup"><span data-stu-id="c8dfc-112">Remarks</span></span>

<span data-ttu-id="c8dfc-113">[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c8dfc-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8dfc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8dfc-114">Requirements</span></span>



| <span data-ttu-id="c8dfc-115">需求</span><span class="sxs-lookup"><span data-stu-id="c8dfc-115">Requirement</span></span> | <span data-ttu-id="c8dfc-116">值</span><span class="sxs-lookup"><span data-stu-id="c8dfc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8dfc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="c8dfc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c8dfc-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c8dfc-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c8dfc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8dfc-119">Library</span></span><br/> | <dl> <span data-ttu-id="c8dfc-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c8dfc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8dfc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8dfc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8dfc-122">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="c8dfc-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




