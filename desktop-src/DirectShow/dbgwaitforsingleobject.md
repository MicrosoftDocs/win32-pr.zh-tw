---
description: 等候物件變成信號。
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: 'DbgWaitForSingleObject 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987967"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="d4eee-103">DbgWaitForSingleObject 函式</span><span class="sxs-lookup"><span data-stu-id="d4eee-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="d4eee-104">等候物件變成信號。</span><span class="sxs-lookup"><span data-stu-id="d4eee-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="d4eee-105">在 debug 組建中，如果逾時間隔在物件收到信號之前過期，此函式就會觸發判斷提示。</span><span class="sxs-lookup"><span data-stu-id="d4eee-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="d4eee-106">若要設定逾時間隔，請呼叫 [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="d4eee-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="d4eee-107">在零售組建中，此函式相當於具有無限逾時間隔的 **WaitForSingleObject** 函數。</span><span class="sxs-lookup"><span data-stu-id="d4eee-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4eee-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4eee-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="d4eee-109">參數</span><span class="sxs-lookup"><span data-stu-id="d4eee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4eee-110">*h*</span><span class="sxs-lookup"><span data-stu-id="d4eee-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="d4eee-111">物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d4eee-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4eee-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4eee-112">Requirements</span></span>



| <span data-ttu-id="d4eee-113">需求</span><span class="sxs-lookup"><span data-stu-id="d4eee-113">Requirement</span></span> | <span data-ttu-id="d4eee-114">值</span><span class="sxs-lookup"><span data-stu-id="d4eee-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4eee-115">標頭</span><span class="sxs-lookup"><span data-stu-id="d4eee-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d4eee-116"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d4eee-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4eee-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4eee-117">Library</span></span><br/> | <dl> <span data-ttu-id="d4eee-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d4eee-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4eee-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4eee-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4eee-120">等候調試函式</span><span class="sxs-lookup"><span data-stu-id="d4eee-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




