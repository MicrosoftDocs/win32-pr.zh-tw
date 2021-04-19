---
description: 用來序列化狀態變更的重要區段指標。
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'CBaseFilter：： m_pLock 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984029"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="8f97c-103">CBaseFilter：： m \_ pLock 成員</span><span class="sxs-lookup"><span data-stu-id="8f97c-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="8f97c-104">用來序列化狀態變更的重要區段指標。</span><span class="sxs-lookup"><span data-stu-id="8f97c-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f97c-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f97c-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="8f97c-106">備註</span><span class="sxs-lookup"><span data-stu-id="8f97c-106">Remarks</span></span>

<span data-ttu-id="8f97c-107">這個變數會在類別的函式中初始化;請參閱 [**CBaseFilter：： CBaseFilter**](cbasefilter-cbasefilter.md)。</span><span class="sxs-lookup"><span data-stu-id="8f97c-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="8f97c-108">在狀態轉換期間，或當方法存取數個作業的狀態時，請保留此重要區段。</span><span class="sxs-lookup"><span data-stu-id="8f97c-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="8f97c-109">基底類別會保存下列方法中的重要區段：</span><span class="sxs-lookup"><span data-stu-id="8f97c-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="8f97c-110">**CBaseFilter::FindPin**</span><span class="sxs-lookup"><span data-stu-id="8f97c-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="8f97c-111">**CBaseFilter::GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="8f97c-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="8f97c-112">**CBaseFilter::JoinFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="8f97c-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="8f97c-113">**CBaseFilter：： IsActive**</span><span class="sxs-lookup"><span data-stu-id="8f97c-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="8f97c-114">**CBaseFilter::SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="8f97c-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="8f97c-115">**CBaseFilter：:P ause**</span><span class="sxs-lookup"><span data-stu-id="8f97c-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="8f97c-116">**CBaseFilter：： Run**</span><span class="sxs-lookup"><span data-stu-id="8f97c-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="8f97c-117">**CBaseFilter：： Stop**</span><span class="sxs-lookup"><span data-stu-id="8f97c-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="8f97c-118">請勿在串流作業期間保留此重要區段， (也就是將範例傳遞給下游篩選) 時。</span><span class="sxs-lookup"><span data-stu-id="8f97c-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="8f97c-119">使用不同的重要區段序列化串流作業。</span><span class="sxs-lookup"><span data-stu-id="8f97c-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="8f97c-120">否則，它可能會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="8f97c-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f97c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f97c-121">Requirements</span></span>



| <span data-ttu-id="8f97c-122">需求</span><span class="sxs-lookup"><span data-stu-id="8f97c-122">Requirement</span></span> | <span data-ttu-id="8f97c-123">值</span><span class="sxs-lookup"><span data-stu-id="8f97c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f97c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8f97c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8f97c-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8f97c-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f97c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f97c-126">Library</span></span><br/> | <dl> <span data-ttu-id="8f97c-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8f97c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f97c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f97c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f97c-129">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="8f97c-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="8f97c-130">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="8f97c-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




