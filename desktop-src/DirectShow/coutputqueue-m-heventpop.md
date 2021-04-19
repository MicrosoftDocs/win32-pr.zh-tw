---
description: 當物件從佇列中移除範例時，所發出的選擇性事件。 值最初是 Null。 呼叫 COutputQueue：： SetPopEvent 方法以指定事件處理常式。
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'COutputQueue：： m_hEventPop 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987089"
---
# <a name="coutputqueuem_heventpop-member"></a><span data-ttu-id="f7dfb-105">COutputQueue：： m \_ hEventPop 成員</span><span class="sxs-lookup"><span data-stu-id="f7dfb-105">COutputQueue::m\_hEventPop member</span></span>

<span data-ttu-id="f7dfb-106">當物件從佇列中移除範例時，所發出的選擇性事件。</span><span class="sxs-lookup"><span data-stu-id="f7dfb-106">Optional event that is signaled whenever the object removes a sample from the queue.</span></span> <span data-ttu-id="f7dfb-107">值最初是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f7dfb-107">The value is initially **NULL**.</span></span> <span data-ttu-id="f7dfb-108">呼叫 [**COutputQueue：： SetPopEvent**](coutputqueue-setpopevent.md) 方法以指定事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f7dfb-108">Call the [**COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) method to specify an event handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7dfb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7dfb-109">Syntax</span></span>


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a><span data-ttu-id="f7dfb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7dfb-110">Requirements</span></span>



| <span data-ttu-id="f7dfb-111">需求</span><span class="sxs-lookup"><span data-stu-id="f7dfb-111">Requirement</span></span> | <span data-ttu-id="f7dfb-112">值</span><span class="sxs-lookup"><span data-stu-id="f7dfb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7dfb-113">標頭</span><span class="sxs-lookup"><span data-stu-id="f7dfb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f7dfb-114"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f7dfb-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7dfb-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7dfb-115">Library</span></span><br/> | <dl> <span data-ttu-id="f7dfb-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f7dfb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7dfb-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7dfb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7dfb-118">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="f7dfb-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




