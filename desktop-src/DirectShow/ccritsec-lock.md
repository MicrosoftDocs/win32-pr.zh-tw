---
description: 鎖定方法會鎖定重要區段物件。
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: 'CCritSec： Lock 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996521"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="dba25-103">CCritSec Lock 方法</span><span class="sxs-lookup"><span data-stu-id="dba25-103">CCritSec.Lock method</span></span>

<span data-ttu-id="dba25-104">**鎖定** 方法會鎖定重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="dba25-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba25-105">語法</span><span class="sxs-lookup"><span data-stu-id="dba25-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="dba25-106">參數</span><span class="sxs-lookup"><span data-stu-id="dba25-106">Parameters</span></span>

<span data-ttu-id="dba25-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dba25-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dba25-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dba25-108">Return value</span></span>

<span data-ttu-id="dba25-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dba25-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba25-110">備註</span><span class="sxs-lookup"><span data-stu-id="dba25-110">Remarks</span></span>

<span data-ttu-id="dba25-111">這個方法會呼叫 [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) 函數。</span><span class="sxs-lookup"><span data-stu-id="dba25-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="dba25-112">呼叫 [**CCritSec：： unlock**](ccritsec-unlock.md) 成員函式，以將重要區段解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="dba25-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="dba25-113">您可以對相同執行緒上的 **鎖定** 方法進行多次呼叫;請務必呼叫 **解除鎖定** 對應的次數。</span><span class="sxs-lookup"><span data-stu-id="dba25-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="dba25-114">如果物件已經由另一個執行緒鎖定， **CCritSec：： Lock** 方法會封鎖，直到釋放物件為止，或直到發生可能的鎖死例外狀況為止。</span><span class="sxs-lookup"><span data-stu-id="dba25-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba25-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="dba25-115">Requirements</span></span>



| <span data-ttu-id="dba25-116">需求</span><span class="sxs-lookup"><span data-stu-id="dba25-116">Requirement</span></span> | <span data-ttu-id="dba25-117">值</span><span class="sxs-lookup"><span data-stu-id="dba25-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dba25-118">標頭</span><span class="sxs-lookup"><span data-stu-id="dba25-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dba25-119"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dba25-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dba25-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="dba25-120">Library</span></span><br/> | <dl> <span data-ttu-id="dba25-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dba25-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dba25-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dba25-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba25-123">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="dba25-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

