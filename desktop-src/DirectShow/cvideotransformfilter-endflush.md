---
description: EndFlush 方法會結束清除作業。 這個方法會覆寫 CTransformFilter：： EndFlush 方法。
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: 'CVideoTransformFilter. EndFlush 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993429"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="40f06-104">CVideoTransformFilter. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="40f06-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="40f06-105">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="40f06-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="40f06-106">這個方法會覆寫 [**CTransformFilter：： EndFlush**](ctransformfilter-endflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="40f06-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f06-107">語法</span><span class="sxs-lookup"><span data-stu-id="40f06-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="40f06-108">參數</span><span class="sxs-lookup"><span data-stu-id="40f06-108">Parameters</span></span>

<span data-ttu-id="40f06-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="40f06-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40f06-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="40f06-110">Return value</span></span>

<span data-ttu-id="40f06-111">\_如果成功，則傳回 [確定]，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="40f06-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f06-112">備註</span><span class="sxs-lookup"><span data-stu-id="40f06-112">Remarks</span></span>

<span data-ttu-id="40f06-113">這個方法會重設所有篩選器的內部效能度量。</span><span class="sxs-lookup"><span data-stu-id="40f06-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f06-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="40f06-114">Requirements</span></span>



| <span data-ttu-id="40f06-115">需求</span><span class="sxs-lookup"><span data-stu-id="40f06-115">Requirement</span></span> | <span data-ttu-id="40f06-116">值</span><span class="sxs-lookup"><span data-stu-id="40f06-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f06-117">標頭</span><span class="sxs-lookup"><span data-stu-id="40f06-117">Header</span></span><br/>  | <dl> <span data-ttu-id="40f06-118"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="40f06-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="40f06-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="40f06-119">Library</span></span><br/> | <dl> <span data-ttu-id="40f06-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="40f06-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f06-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40f06-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f06-122">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="40f06-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




