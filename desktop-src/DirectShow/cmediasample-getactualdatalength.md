---
description: GetActualDataLength 方法會擷取緩衝區中有效資料的長度。 這個方法會實 IMediaSample：： GetActualDataLength 方法。
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: 'CMediaSample. GetActualDataLength 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995057"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="e1d3f-104">CMediaSample. GetActualDataLength 方法</span><span class="sxs-lookup"><span data-stu-id="e1d3f-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="e1d3f-105">`GetActualDataLength`方法會擷取緩衝區中有效資料的長度。</span><span class="sxs-lookup"><span data-stu-id="e1d3f-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="e1d3f-106">這個方法會實 [**IMediaSample：： GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) 方法。</span><span class="sxs-lookup"><span data-stu-id="e1d3f-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d3f-107">語法</span><span class="sxs-lookup"><span data-stu-id="e1d3f-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="e1d3f-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1d3f-108">Parameters</span></span>

<span data-ttu-id="e1d3f-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e1d3f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1d3f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1d3f-110">Return value</span></span>

<span data-ttu-id="e1d3f-111">傳回有效資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e1d3f-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d3f-112">備註</span><span class="sxs-lookup"><span data-stu-id="e1d3f-112">Remarks</span></span>

<span data-ttu-id="e1d3f-113">[**CMediaSample：： m \_ lActual**](cmediasample-m-lactual.md)成員變數會指定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e1d3f-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d3f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1d3f-114">Requirements</span></span>



| <span data-ttu-id="e1d3f-115">需求</span><span class="sxs-lookup"><span data-stu-id="e1d3f-115">Requirement</span></span> | <span data-ttu-id="e1d3f-116">值</span><span class="sxs-lookup"><span data-stu-id="e1d3f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d3f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e1d3f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d3f-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d3f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1d3f-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1d3f-119">Library</span></span><br/> | <dl> <span data-ttu-id="e1d3f-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d3f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d3f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1d3f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d3f-122">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="e1d3f-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

