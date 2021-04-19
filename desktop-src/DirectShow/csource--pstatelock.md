---
description: PStateLock 方法會抓取篩選準則的重要區段物件的指標。
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: 'CSource. pStateLock 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994164"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="63040-103">CSource. pStateLock 方法</span><span class="sxs-lookup"><span data-stu-id="63040-103">CSource.pStateLock method</span></span>

<span data-ttu-id="63040-104">**PStateLock** 方法會抓取篩選準則的重要區段物件的指標。</span><span class="sxs-lookup"><span data-stu-id="63040-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="63040-105">雖然命名如同成員變數，但 **pStateLock** 是一種方法。</span><span class="sxs-lookup"><span data-stu-id="63040-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="63040-106">語法</span><span class="sxs-lookup"><span data-stu-id="63040-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="63040-107">參數</span><span class="sxs-lookup"><span data-stu-id="63040-107">Parameters</span></span>

<span data-ttu-id="63040-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="63040-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="63040-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="63040-109">Return value</span></span>

<span data-ttu-id="63040-110">傳回 [**CSource：： m \_ cStateLock**](csource-m-cstatelock.md) 成員變數的指標。</span><span class="sxs-lookup"><span data-stu-id="63040-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="63040-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="63040-111">Requirements</span></span>



| <span data-ttu-id="63040-112">需求</span><span class="sxs-lookup"><span data-stu-id="63040-112">Requirement</span></span> | <span data-ttu-id="63040-113">值</span><span class="sxs-lookup"><span data-stu-id="63040-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63040-114">標頭</span><span class="sxs-lookup"><span data-stu-id="63040-114">Header</span></span><br/>  | <dl> <span data-ttu-id="63040-115"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="63040-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="63040-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="63040-116">Library</span></span><br/> | <dl> <span data-ttu-id="63040-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="63040-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63040-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63040-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63040-119">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="63040-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




