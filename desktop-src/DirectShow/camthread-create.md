---
description: Create 方法會建立執行緒。
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: 'CAMThread：建立方法 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994788"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="4e0a1-103">CAMThread. Create 方法</span><span class="sxs-lookup"><span data-stu-id="4e0a1-103">CAMThread.Create method</span></span>

<span data-ttu-id="4e0a1-104">`Create`方法會建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="4e0a1-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e0a1-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="4e0a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e0a1-106">Parameters</span></span>

<span data-ttu-id="4e0a1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4e0a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e0a1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e0a1-108">Return value</span></span>

<span data-ttu-id="4e0a1-109">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4e0a1-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e0a1-110">備註</span><span class="sxs-lookup"><span data-stu-id="4e0a1-110">Remarks</span></span>

<span data-ttu-id="4e0a1-111">這個方法會使用執行緒程式和執行緒引數的 [**CAMThread：： InitialThreadProc**](camthread-initialthreadproc.md) 方法，來建立執行緒 `this` 。</span><span class="sxs-lookup"><span data-stu-id="4e0a1-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="4e0a1-112">如果執行緒已經存在，方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="4e0a1-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e0a1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e0a1-113">Requirements</span></span>



| <span data-ttu-id="4e0a1-114">需求</span><span class="sxs-lookup"><span data-stu-id="4e0a1-114">Requirement</span></span> | <span data-ttu-id="4e0a1-115">值</span><span class="sxs-lookup"><span data-stu-id="4e0a1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e0a1-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4e0a1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4e0a1-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4e0a1-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4e0a1-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e0a1-118">Library</span></span><br/> | <dl> <span data-ttu-id="4e0a1-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4e0a1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e0a1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e0a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e0a1-121">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="4e0a1-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




