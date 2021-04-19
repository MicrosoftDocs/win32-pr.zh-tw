---
description: CAMEvent 類別是手動重設和自動重設事件的包裝函式。
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: 'CAMEvent 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978654"
---
# <a name="camevent-class"></a><span data-ttu-id="0aabd-103">CAMEvent 類別</span><span class="sxs-lookup"><span data-stu-id="0aabd-103">CAMEvent class</span></span>

![camevent 類別階層](images/util06.png)

<span data-ttu-id="0aabd-105">**CAMEvent** 類別是手動重設和自動重設事件的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="0aabd-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="0aabd-106">此類別提供便利的方式來管理事件，而不是呼叫像是 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)、 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)和 [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent)等函數。</span><span class="sxs-lookup"><span data-stu-id="0aabd-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="0aabd-107">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="0aabd-107">Protected Member Variables</span></span>                          | <span data-ttu-id="0aabd-108">Description</span><span class="sxs-lookup"><span data-stu-id="0aabd-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="0aabd-109">**m \_ hEvent**</span><span class="sxs-lookup"><span data-stu-id="0aabd-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="0aabd-110">事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0aabd-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="0aabd-111">公用方法</span><span class="sxs-lookup"><span data-stu-id="0aabd-111">Public Methods</span></span>                                      | <span data-ttu-id="0aabd-112">Description</span><span class="sxs-lookup"><span data-stu-id="0aabd-112">Description</span></span>                                                     |
| [<span data-ttu-id="0aabd-113">**CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="0aabd-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="0aabd-114">函式方法。</span><span class="sxs-lookup"><span data-stu-id="0aabd-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="0aabd-115">**~ CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="0aabd-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="0aabd-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="0aabd-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="0aabd-117">**勾選**</span><span class="sxs-lookup"><span data-stu-id="0aabd-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="0aabd-118">檢查是否已設定事件，而不封鎖。</span><span class="sxs-lookup"><span data-stu-id="0aabd-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="0aabd-119">**重設**</span><span class="sxs-lookup"><span data-stu-id="0aabd-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="0aabd-120">將事件的狀態設定為未收到信號。</span><span class="sxs-lookup"><span data-stu-id="0aabd-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="0aabd-121">**設定**</span><span class="sxs-lookup"><span data-stu-id="0aabd-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="0aabd-122">通知事件。</span><span class="sxs-lookup"><span data-stu-id="0aabd-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="0aabd-123">**等候**</span><span class="sxs-lookup"><span data-stu-id="0aabd-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="0aabd-124">封鎖直到事件收到信號，或直到發生超時為止。</span><span class="sxs-lookup"><span data-stu-id="0aabd-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="0aabd-125">運算子</span><span class="sxs-lookup"><span data-stu-id="0aabd-125">Operators</span></span>                                           | <span data-ttu-id="0aabd-126">說明</span><span class="sxs-lookup"><span data-stu-id="0aabd-126">Description</span></span>                                                     |
| [<span data-ttu-id="0aabd-127">**運算子控制碼**</span><span class="sxs-lookup"><span data-stu-id="0aabd-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="0aabd-128">捕獲事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0aabd-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="0aabd-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aabd-129">Requirements</span></span>



| <span data-ttu-id="0aabd-130">需求</span><span class="sxs-lookup"><span data-stu-id="0aabd-130">Requirement</span></span> | <span data-ttu-id="0aabd-131">值</span><span class="sxs-lookup"><span data-stu-id="0aabd-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aabd-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0aabd-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0aabd-133"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0aabd-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0aabd-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="0aabd-134">Library</span></span><br/> | <dl> <span data-ttu-id="0aabd-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0aabd-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

