---
description: 如果目前的執行緒是指定之重要區段的擁有者，則傳回 FALSE。
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: 'CritCheckOut 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995278"
---
# <a name="critcheckout-function"></a><span data-ttu-id="8f29c-103">CritCheckOut 函式</span><span class="sxs-lookup"><span data-stu-id="8f29c-103">CritCheckOut function</span></span>

<span data-ttu-id="8f29c-104">如果目前的執行緒是指定之重要區段的擁有者，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8f29c-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f29c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f29c-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="8f29c-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f29c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f29c-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="8f29c-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="8f29c-108">[**CCritSec**](ccritsec.md)重要區段的指標。</span><span class="sxs-lookup"><span data-stu-id="8f29c-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f29c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f29c-109">Return value</span></span>

<span data-ttu-id="8f29c-110">在偵錯工具組建中，如果目前的執行緒是此重要區段的擁有者，則傳回 **FALSE** ，否則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="8f29c-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="8f29c-111">在零售組建中，一律會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8f29c-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f29c-112">備註</span><span class="sxs-lookup"><span data-stu-id="8f29c-112">Remarks</span></span>

<span data-ttu-id="8f29c-113">此函數是 [**CritCheckIn**](critcheckin.md) 函數的反向。</span><span class="sxs-lookup"><span data-stu-id="8f29c-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="8f29c-114">如果 **CritCheckIn** 傳回 **TRUE，則** **CritCheckOut** 會傳回 **FALSE**，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8f29c-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f29c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f29c-115">Requirements</span></span>



| <span data-ttu-id="8f29c-116">需求</span><span class="sxs-lookup"><span data-stu-id="8f29c-116">Requirement</span></span> | <span data-ttu-id="8f29c-117">值</span><span class="sxs-lookup"><span data-stu-id="8f29c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f29c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8f29c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8f29c-119"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8f29c-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8f29c-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f29c-120">Library</span></span><br/> | <dl> <span data-ttu-id="8f29c-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8f29c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f29c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f29c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f29c-123">重要區段調試函數</span><span class="sxs-lookup"><span data-stu-id="8f29c-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




