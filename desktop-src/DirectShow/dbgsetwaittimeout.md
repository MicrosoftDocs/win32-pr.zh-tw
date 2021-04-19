---
description: 設定調試超時值。 在零售組建中略過。
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: 'DbgSetWaitTimeout 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976021"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="1e6b8-104">DbgSetWaitTimeout 函式</span><span class="sxs-lookup"><span data-stu-id="1e6b8-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="1e6b8-105">設定調試超時值。</span><span class="sxs-lookup"><span data-stu-id="1e6b8-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="1e6b8-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="1e6b8-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="1e6b8-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="1e6b8-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e6b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e6b8-109">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="1e6b8-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="1e6b8-110">超時值（以毫秒為單位），或無限期等候無限期等候。</span><span class="sxs-lookup"><span data-stu-id="1e6b8-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e6b8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e6b8-111">Return value</span></span>

<span data-ttu-id="1e6b8-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1e6b8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6b8-113">備註</span><span class="sxs-lookup"><span data-stu-id="1e6b8-113">Remarks</span></span>

<span data-ttu-id="1e6b8-114">在 debug 組建中， [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) 和 [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) 函數會使用此值做為逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="1e6b8-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6b8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e6b8-115">Requirements</span></span>



| <span data-ttu-id="1e6b8-116">需求</span><span class="sxs-lookup"><span data-stu-id="1e6b8-116">Requirement</span></span> | <span data-ttu-id="1e6b8-117">值</span><span class="sxs-lookup"><span data-stu-id="1e6b8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6b8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1e6b8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1e6b8-119"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1e6b8-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e6b8-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e6b8-120">Library</span></span><br/> | <dl> <span data-ttu-id="1e6b8-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1e6b8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e6b8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e6b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6b8-123">等候調試函式</span><span class="sxs-lookup"><span data-stu-id="1e6b8-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




