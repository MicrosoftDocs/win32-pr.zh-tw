---
description: 建立執行緒時，InitialThreadProc 方法會呼叫 COutputQueue：： ThreadProc 方法。
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: " (Outputq 的 COutputQueue.InitialThreadProc 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001145"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="a9d1a-103">COutputQueue.InitialThreadProc 方法</span><span class="sxs-lookup"><span data-stu-id="a9d1a-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="a9d1a-104">`InitialThreadProc`當建立執行緒時，此方法會呼叫 [**COutputQueue：： ThreadProc**](coutputqueue-threadproc.md)方法。</span><span class="sxs-lookup"><span data-stu-id="a9d1a-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d1a-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9d1a-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="a9d1a-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9d1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d1a-107">*光伏*</span><span class="sxs-lookup"><span data-stu-id="a9d1a-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d1a-108">`this` 指標。</span><span class="sxs-lookup"><span data-stu-id="a9d1a-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d1a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9d1a-109">Return value</span></span>

<span data-ttu-id="a9d1a-110">傳回 [**COutputQueue：： ThreadProc**](coutputqueue-threadproc.md) 方法所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="a9d1a-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d1a-111">備註</span><span class="sxs-lookup"><span data-stu-id="a9d1a-111">Remarks</span></span>

<span data-ttu-id="a9d1a-112">這個方法是物件的背景工作執行緒的執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="a9d1a-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="a9d1a-113">物件的 `this` 指標是執行緒參數。</span><span class="sxs-lookup"><span data-stu-id="a9d1a-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="a9d1a-114">方法會將此方法取值為呼叫 **ThreadProc**。</span><span class="sxs-lookup"><span data-stu-id="a9d1a-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d1a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9d1a-115">Requirements</span></span>



| <span data-ttu-id="a9d1a-116">需求</span><span class="sxs-lookup"><span data-stu-id="a9d1a-116">Requirement</span></span> | <span data-ttu-id="a9d1a-117">值</span><span class="sxs-lookup"><span data-stu-id="a9d1a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d1a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a9d1a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a9d1a-119"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a9d1a-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a9d1a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9d1a-120">Library</span></span><br/> | <dl> <span data-ttu-id="a9d1a-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a9d1a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d1a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9d1a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d1a-123">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="a9d1a-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




