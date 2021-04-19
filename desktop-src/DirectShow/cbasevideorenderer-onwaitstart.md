---
description: OnWaitStart 方法會更新花費在等候和不等候的時間。
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: 'CBaseVideoRenderer. OnWaitStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998718"
---
# <a name="cbasevideorendereronwaitstart-method"></a><span data-ttu-id="3541b-103">CBaseVideoRenderer. OnWaitStart 方法</span><span class="sxs-lookup"><span data-stu-id="3541b-103">CBaseVideoRenderer.OnWaitStart method</span></span>

<span data-ttu-id="3541b-104">`OnWaitStart`方法會更新花費在等候和不等待的時間。</span><span class="sxs-lookup"><span data-stu-id="3541b-104">The `OnWaitStart` method updates times spent waiting and not waiting.</span></span>

## <a name="syntax"></a><span data-ttu-id="3541b-105">語法</span><span class="sxs-lookup"><span data-stu-id="3541b-105">Syntax</span></span>


```C++
void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="3541b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3541b-106">Parameters</span></span>

<span data-ttu-id="3541b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3541b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3541b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3541b-108">Return value</span></span>

<span data-ttu-id="3541b-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3541b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3541b-110">備註</span><span class="sxs-lookup"><span data-stu-id="3541b-110">Remarks</span></span>

<span data-ttu-id="3541b-111">開始等候轉譯事件時，會呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="3541b-111">This member function is called when starting to wait for a rendering event.</span></span> <span data-ttu-id="3541b-112">它僅用於效能度量。</span><span class="sxs-lookup"><span data-stu-id="3541b-112">It is used only for performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="3541b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3541b-113">Requirements</span></span>



| <span data-ttu-id="3541b-114">需求</span><span class="sxs-lookup"><span data-stu-id="3541b-114">Requirement</span></span> | <span data-ttu-id="3541b-115">值</span><span class="sxs-lookup"><span data-stu-id="3541b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3541b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3541b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3541b-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3541b-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3541b-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3541b-118">Library</span></span><br/> | <dl> <span data-ttu-id="3541b-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3541b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3541b-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3541b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3541b-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="3541b-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




