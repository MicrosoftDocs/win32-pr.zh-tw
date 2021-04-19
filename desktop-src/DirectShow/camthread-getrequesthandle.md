---
description: GetRequestHandle 方法會抓取由 CAMThread：： CallWorker 方法所發出之事件的控制碼。
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: 'CAMThread. GetRequestHandle 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999641"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="ed70d-103">CAMThread. GetRequestHandle 方法</span><span class="sxs-lookup"><span data-stu-id="ed70d-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="ed70d-104">`GetRequestHandle`方法會抓取 [**CAMThread：： CallWorker**](camthread-callworker.md)方法所發出之事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed70d-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed70d-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed70d-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="ed70d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed70d-106">Parameters</span></span>

<span data-ttu-id="ed70d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ed70d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed70d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed70d-108">Return value</span></span>

<span data-ttu-id="ed70d-109">傳回事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed70d-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed70d-110">備註</span><span class="sxs-lookup"><span data-stu-id="ed70d-110">Remarks</span></span>

<span data-ttu-id="ed70d-111">CAMEvent 類別會保留私用手動重設事件，它是由 CallWorker 所設定，並由 [**CAMThread：： Reply**](camthread-reply.md) 方法重設。</span><span class="sxs-lookup"><span data-stu-id="ed70d-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="ed70d-112">如果您呼叫 WaitForMultipleObjects 之類的函式，請使用 GetRequestHandle 來取得事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed70d-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed70d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed70d-113">Requirements</span></span>



| <span data-ttu-id="ed70d-114">需求</span><span class="sxs-lookup"><span data-stu-id="ed70d-114">Requirement</span></span> | <span data-ttu-id="ed70d-115">值</span><span class="sxs-lookup"><span data-stu-id="ed70d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed70d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ed70d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ed70d-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ed70d-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ed70d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed70d-118">Library</span></span><br/> | <dl> <span data-ttu-id="ed70d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed70d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed70d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed70d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed70d-121">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="ed70d-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




