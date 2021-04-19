---
description: 等候指定物件的任何 (或所有) 都收到信號。
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: 'DbgWaitForMultipleObjects 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990834"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="bcbcb-103">DbgWaitForMultipleObjects 函式</span><span class="sxs-lookup"><span data-stu-id="bcbcb-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="bcbcb-104">等候指定物件的任何 (或所有) 都收到信號。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="bcbcb-105">在 debug 組建中，如果逾時間隔在物件收到信號之前過期，此函式就會觸發判斷提示。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="bcbcb-106">若要設定逾時間隔，請呼叫 [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="bcbcb-107">在零售組建中，此函式相當於具有無限逾時間隔的 **WaitForMultipleObjects** 函數。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbcb-108">語法</span><span class="sxs-lookup"><span data-stu-id="bcbcb-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="bcbcb-109">參數</span><span class="sxs-lookup"><span data-stu-id="bcbcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbcb-110">*nCount*</span><span class="sxs-lookup"><span data-stu-id="bcbcb-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbcb-111">物件數目。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="bcbcb-112">*lpHandles*</span><span class="sxs-lookup"><span data-stu-id="bcbcb-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbcb-113">物件之控制碼的陣列，大小為 *nCount*。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="bcbcb-114">*bWaitAll*</span><span class="sxs-lookup"><span data-stu-id="bcbcb-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbcb-115">指定是否等候所有物件的布林值。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="bcbcb-116">若為 **TRUE**，則函式會等候所有物件收到信號。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="bcbcb-117">否則，它會等候至少一個物件收到信號。</span><span class="sxs-lookup"><span data-stu-id="bcbcb-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcbcb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcbcb-118">Requirements</span></span>



| <span data-ttu-id="bcbcb-119">需求</span><span class="sxs-lookup"><span data-stu-id="bcbcb-119">Requirement</span></span> | <span data-ttu-id="bcbcb-120">值</span><span class="sxs-lookup"><span data-stu-id="bcbcb-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbcb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bcbcb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bcbcb-122"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bcbcb-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bcbcb-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="bcbcb-123">Library</span></span><br/> | <dl> <span data-ttu-id="bcbcb-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bcbcb-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbcb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcbcb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbcb-126">等候調試函式</span><span class="sxs-lookup"><span data-stu-id="bcbcb-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




