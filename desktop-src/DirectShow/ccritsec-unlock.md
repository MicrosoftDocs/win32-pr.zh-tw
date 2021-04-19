---
description: 解除鎖定方法會解除鎖定重要區段物件。
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: 'CCritSec 解除鎖定方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990278"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="4f920-103">CCritSec 解除鎖定方法</span><span class="sxs-lookup"><span data-stu-id="4f920-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="4f920-104">**解除鎖定** 方法會解除鎖定重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="4f920-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f920-105">語法</span><span class="sxs-lookup"><span data-stu-id="4f920-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="4f920-106">參數</span><span class="sxs-lookup"><span data-stu-id="4f920-106">Parameters</span></span>

<span data-ttu-id="4f920-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4f920-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f920-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f920-108">Return value</span></span>

<span data-ttu-id="4f920-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f920-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f920-110">備註</span><span class="sxs-lookup"><span data-stu-id="4f920-110">Remarks</span></span>

<span data-ttu-id="4f920-111">這個方法會呼叫 [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) 函數。</span><span class="sxs-lookup"><span data-stu-id="4f920-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="4f920-112">針對 [**CCritSec：： Lock**](ccritsec-lock.md) 方法的每個呼叫呼叫這個方法一次。</span><span class="sxs-lookup"><span data-stu-id="4f920-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f920-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f920-113">Requirements</span></span>



| <span data-ttu-id="4f920-114">需求</span><span class="sxs-lookup"><span data-stu-id="4f920-114">Requirement</span></span> | <span data-ttu-id="4f920-115">值</span><span class="sxs-lookup"><span data-stu-id="4f920-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f920-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4f920-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4f920-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4f920-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4f920-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="4f920-118">Library</span></span><br/> | <dl> <span data-ttu-id="4f920-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4f920-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f920-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f920-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f920-121">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="4f920-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

