---
description: 啟用或停用指定之重要區段的偵錯工具記錄。
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: 'DbgLockTrace 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993493"
---
# <a name="dbglocktrace-function"></a><span data-ttu-id="712f2-103">DbgLockTrace 函式</span><span class="sxs-lookup"><span data-stu-id="712f2-103">DbgLockTrace function</span></span>

<span data-ttu-id="712f2-104">啟用或停用指定之重要區段的偵錯工具記錄。</span><span class="sxs-lookup"><span data-stu-id="712f2-104">Enables or disables debug logging of a given critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="712f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="712f2-105">Syntax</span></span>


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a><span data-ttu-id="712f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="712f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712f2-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="712f2-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="712f2-108">[**CCritSec**](ccritsec.md)重要區段的指標。</span><span class="sxs-lookup"><span data-stu-id="712f2-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> <dt>

<span data-ttu-id="712f2-109">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="712f2-109">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="712f2-110">指定是否啟用記錄的值。</span><span class="sxs-lookup"><span data-stu-id="712f2-110">Value specifying whether logging is enabled.</span></span> <span data-ttu-id="712f2-111">使用 **TRUE** 來啟用記錄，或使用 **FALSE** 來停用它。</span><span class="sxs-lookup"><span data-stu-id="712f2-111">Use **TRUE** to enable logging or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="712f2-112">Return value</span></span>

<span data-ttu-id="712f2-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="712f2-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="712f2-114">備註</span><span class="sxs-lookup"><span data-stu-id="712f2-114">Remarks</span></span>

<span data-ttu-id="712f2-115">您可以使用此函數來追蹤特定的重要區段。</span><span class="sxs-lookup"><span data-stu-id="712f2-115">Use this function to trace a specific critical section.</span></span> <span data-ttu-id="712f2-116">根據預設，重要區段的 debug 記錄已停用，因為很多重要區段。</span><span class="sxs-lookup"><span data-stu-id="712f2-116">By default, debug logging of critical sections is disabled, because of the large number of critical sections.</span></span>

<span data-ttu-id="712f2-117">若要追蹤重要區段，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="712f2-117">To trace a critical section, perform the following steps:</span></span>

1.  <span data-ttu-id="712f2-118">\_在您包含 DirectShow 標頭之前，請先定義 debug 或 debug。</span><span class="sxs-lookup"><span data-stu-id="712f2-118">Define DEBUG or \_DEBUG before you include the DirectShow headers.</span></span>
2.  <span data-ttu-id="712f2-119">藉由使用記錄鎖定旗標呼叫 [**DbgSetModuleLevel**](dbgsetmodulelevel.md) ，啟用重要區段的 debug 記錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="712f2-119">Enable debug logging for critical sections, by calling [**DbgSetModuleLevel**](dbgsetmodulelevel.md) with the LOG\_LOCKING flag.</span></span>
3.  <span data-ttu-id="712f2-120">在您想要追蹤的重要區段上呼叫 **DbgLockTrace** 。</span><span class="sxs-lookup"><span data-stu-id="712f2-120">Call **DbgLockTrace** on the critical section you want to trace.</span></span>

<span data-ttu-id="712f2-121">在零售組建中， **DbgLockTrace** 函數沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="712f2-121">In retail builds, the **DbgLockTrace** function has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="712f2-122">範例</span><span class="sxs-lookup"><span data-stu-id="712f2-122">Examples</span></span>

<span data-ttu-id="712f2-123">下列程式碼範例顯示如何追蹤重要區段。</span><span class="sxs-lookup"><span data-stu-id="712f2-123">The following code example shows how to trace a critical section.</span></span>


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a><span data-ttu-id="712f2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="712f2-124">Requirements</span></span>



| <span data-ttu-id="712f2-125">需求</span><span class="sxs-lookup"><span data-stu-id="712f2-125">Requirement</span></span> | <span data-ttu-id="712f2-126">值</span><span class="sxs-lookup"><span data-stu-id="712f2-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="712f2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="712f2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="712f2-128"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="712f2-128"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="712f2-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="712f2-129">Library</span></span><br/> | <dl> <span data-ttu-id="712f2-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="712f2-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="712f2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="712f2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="712f2-132">重要區段調試函數</span><span class="sxs-lookup"><span data-stu-id="712f2-132">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




