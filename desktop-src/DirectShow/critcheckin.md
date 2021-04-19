---
description: 如果目前的執行緒是指定之重要區段的擁有者，則傳回 TRUE。
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: 'CritCheckIn 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989782"
---
# <a name="critcheckin-function"></a><span data-ttu-id="ce23b-103">CritCheckIn 函式</span><span class="sxs-lookup"><span data-stu-id="ce23b-103">CritCheckIn function</span></span>

<span data-ttu-id="ce23b-104">如果目前的執行緒是指定之重要區段的擁有者，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ce23b-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce23b-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce23b-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="ce23b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ce23b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce23b-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="ce23b-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="ce23b-108">[**CCritSec**](ccritsec.md)重要區段的指標。</span><span class="sxs-lookup"><span data-stu-id="ce23b-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce23b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce23b-109">Return value</span></span>

<span data-ttu-id="ce23b-110">在 debug 組建中，如果目前的執行緒是此重要區段的擁有者， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ce23b-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="ce23b-111">在零售組建中，一律會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ce23b-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce23b-112">備註</span><span class="sxs-lookup"><span data-stu-id="ce23b-112">Remarks</span></span>

<span data-ttu-id="ce23b-113">這個函式在 [**ASSERT**](assert.md) 宏內特別有用，可測試執行緒是否擁有指定的鎖定。</span><span class="sxs-lookup"><span data-stu-id="ce23b-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="ce23b-114">範例</span><span class="sxs-lookup"><span data-stu-id="ce23b-114">Examples</span></span>

<span data-ttu-id="ce23b-115">下列程式碼範例示範如何使用此函式：</span><span class="sxs-lookup"><span data-stu-id="ce23b-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="ce23b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce23b-116">Requirements</span></span>



| <span data-ttu-id="ce23b-117">需求</span><span class="sxs-lookup"><span data-stu-id="ce23b-117">Requirement</span></span> | <span data-ttu-id="ce23b-118">值</span><span class="sxs-lookup"><span data-stu-id="ce23b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce23b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ce23b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ce23b-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ce23b-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ce23b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce23b-121">Library</span></span><br/> | <dl> <span data-ttu-id="ce23b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ce23b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce23b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce23b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce23b-124">重要區段調試函數</span><span class="sxs-lookup"><span data-stu-id="ce23b-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




