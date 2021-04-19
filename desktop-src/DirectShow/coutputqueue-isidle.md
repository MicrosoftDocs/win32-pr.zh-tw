---
description: IsIdle 方法會判斷物件是否正在等候資料。
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: 'COutputQueue. IsIdle 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999638"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="0c10f-103">COutputQueue. IsIdle 方法</span><span class="sxs-lookup"><span data-stu-id="0c10f-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="0c10f-104">`IsIdle`方法會判斷物件是否正在等候資料。</span><span class="sxs-lookup"><span data-stu-id="0c10f-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c10f-105">語法</span><span class="sxs-lookup"><span data-stu-id="0c10f-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="0c10f-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c10f-106">Parameters</span></span>

<span data-ttu-id="0c10f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0c10f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c10f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c10f-108">Return value</span></span>

<span data-ttu-id="0c10f-109">如果執行緒正在等候且範例陣列是空的，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0c10f-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="0c10f-110">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0c10f-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c10f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c10f-111">Requirements</span></span>



| <span data-ttu-id="0c10f-112">需求</span><span class="sxs-lookup"><span data-stu-id="0c10f-112">Requirement</span></span> | <span data-ttu-id="0c10f-113">值</span><span class="sxs-lookup"><span data-stu-id="0c10f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c10f-114">標頭</span><span class="sxs-lookup"><span data-stu-id="0c10f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0c10f-115"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0c10f-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c10f-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c10f-116">Library</span></span><br/> | <dl> <span data-ttu-id="0c10f-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0c10f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c10f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c10f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c10f-119">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="0c10f-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




