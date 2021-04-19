---
description: IsSyncPoint 方法會判斷範例的開頭是否為同步處理點。 這個方法會實 IMediaSample：： IsSyncPoint 方法。
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: 'CMediaSample. IsSyncPoint 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8cc93c03ce3b864e1c1b0a5794d711b1b0c3d68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977608"
---
# <a name="cmediasampleissyncpoint-method"></a><span data-ttu-id="144cf-104">CMediaSample. IsSyncPoint 方法</span><span class="sxs-lookup"><span data-stu-id="144cf-104">CMediaSample.IsSyncPoint method</span></span>

<span data-ttu-id="144cf-105">`IsSyncPoint`方法會判斷範例的開頭是否為同步處理點。</span><span class="sxs-lookup"><span data-stu-id="144cf-105">The `IsSyncPoint` method determines if the beginning of the sample is a synchronization point.</span></span> <span data-ttu-id="144cf-106">這個方法會實 [**IMediaSample：： IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) 方法。</span><span class="sxs-lookup"><span data-stu-id="144cf-106">This method implements the [**IMediaSample::IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="144cf-107">語法</span><span class="sxs-lookup"><span data-stu-id="144cf-107">Syntax</span></span>


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a><span data-ttu-id="144cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="144cf-108">Parameters</span></span>

<span data-ttu-id="144cf-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="144cf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="144cf-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="144cf-110">Return value</span></span>

<span data-ttu-id="144cf-111">\_如果範例是同步處理點，則傳回 s OK， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="144cf-111">Returns S\_OK if the sample is a synchronization point, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="144cf-112">備註</span><span class="sxs-lookup"><span data-stu-id="144cf-112">Remarks</span></span>

<span data-ttu-id="144cf-113">[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="144cf-113">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="144cf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="144cf-114">Requirements</span></span>



| <span data-ttu-id="144cf-115">需求</span><span class="sxs-lookup"><span data-stu-id="144cf-115">Requirement</span></span> | <span data-ttu-id="144cf-116">值</span><span class="sxs-lookup"><span data-stu-id="144cf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="144cf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="144cf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="144cf-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="144cf-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="144cf-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="144cf-119">Library</span></span><br/> | <dl> <span data-ttu-id="144cf-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="144cf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="144cf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="144cf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="144cf-122">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="144cf-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




