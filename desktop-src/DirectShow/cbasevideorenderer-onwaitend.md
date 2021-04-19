---
description: 等候時間結束時，會呼叫 OnWaitEnd 方法。
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: 'CBaseVideoRenderer. OnWaitEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991559"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="fdb85-103">CBaseVideoRenderer. OnWaitEnd 方法</span><span class="sxs-lookup"><span data-stu-id="fdb85-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="fdb85-104">等候時間結束時，會呼叫 OnWaitEnd 方法。</span><span class="sxs-lookup"><span data-stu-id="fdb85-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb85-105">語法</span><span class="sxs-lookup"><span data-stu-id="fdb85-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="fdb85-106">參數</span><span class="sxs-lookup"><span data-stu-id="fdb85-106">Parameters</span></span>

<span data-ttu-id="fdb85-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fdb85-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdb85-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdb85-108">Return value</span></span>

<span data-ttu-id="fdb85-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fdb85-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdb85-110">備註</span><span class="sxs-lookup"><span data-stu-id="fdb85-110">Remarks</span></span>

<span data-ttu-id="fdb85-111">此成員函式只會執行效能記錄。</span><span class="sxs-lookup"><span data-stu-id="fdb85-111">This member function does only performance logging.</span></span> <span data-ttu-id="fdb85-112">從視窗中的等候喚醒執行緒，或在下一個範例是因為呈現時，就會呼叫它。</span><span class="sxs-lookup"><span data-stu-id="fdb85-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="fdb85-113">它最後可以用來收集控制同步處理的資訊。</span><span class="sxs-lookup"><span data-stu-id="fdb85-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdb85-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdb85-114">Requirements</span></span>



| <span data-ttu-id="fdb85-115">需求</span><span class="sxs-lookup"><span data-stu-id="fdb85-115">Requirement</span></span> | <span data-ttu-id="fdb85-116">值</span><span class="sxs-lookup"><span data-stu-id="fdb85-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdb85-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fdb85-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fdb85-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fdb85-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fdb85-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdb85-119">Library</span></span><br/> | <dl> <span data-ttu-id="fdb85-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fdb85-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdb85-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdb85-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdb85-122">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="fdb85-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




