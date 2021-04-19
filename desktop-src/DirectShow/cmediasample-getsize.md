---
description: GetSize 方法會擷取緩衝區的大小。 這個方法會實 IMediaSample：： GetSize 方法。
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: 'CMediaSample. GetSize 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986601"
---
# <a name="cmediasamplegetsize-method"></a><span data-ttu-id="2b680-104">CMediaSample. GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="2b680-104">CMediaSample.GetSize method</span></span>

<span data-ttu-id="2b680-105">`GetSize`方法會擷取緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="2b680-105">The `GetSize` method retrieves the size of the buffer.</span></span> <span data-ttu-id="2b680-106">這個方法會實 [**IMediaSample：： GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) 方法。</span><span class="sxs-lookup"><span data-stu-id="2b680-106">This method implements the [**IMediaSample::GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b680-107">語法</span><span class="sxs-lookup"><span data-stu-id="2b680-107">Syntax</span></span>


```C++
LONG GetSize();
```



## <a name="parameters"></a><span data-ttu-id="2b680-108">參數</span><span class="sxs-lookup"><span data-stu-id="2b680-108">Parameters</span></span>

<span data-ttu-id="2b680-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2b680-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b680-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b680-110">Return value</span></span>

<span data-ttu-id="2b680-111">傳回緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b680-111">Returns the size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b680-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b680-112">Requirements</span></span>



| <span data-ttu-id="2b680-113">需求</span><span class="sxs-lookup"><span data-stu-id="2b680-113">Requirement</span></span> | <span data-ttu-id="2b680-114">值</span><span class="sxs-lookup"><span data-stu-id="2b680-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b680-115">標頭</span><span class="sxs-lookup"><span data-stu-id="2b680-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2b680-116"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2b680-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2b680-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b680-117">Library</span></span><br/> | <dl> <span data-ttu-id="2b680-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2b680-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b680-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b680-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b680-120">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="2b680-120">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




