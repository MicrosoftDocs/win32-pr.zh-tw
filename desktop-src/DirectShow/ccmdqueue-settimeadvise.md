---
description: SetTimeAdvise 方法會使用參考時鐘來設定計時器事件。
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: 'CCmdQueue. SetTimeAdvise 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001527"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="0cc2d-103">CCmdQueue. SetTimeAdvise 方法</span><span class="sxs-lookup"><span data-stu-id="0cc2d-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="0cc2d-104">`SetTimeAdvise`方法會使用參考時鐘來設定計時器事件。</span><span class="sxs-lookup"><span data-stu-id="0cc2d-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0cc2d-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="0cc2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0cc2d-106">Parameters</span></span>

<span data-ttu-id="0cc2d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0cc2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cc2d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cc2d-108">Return value</span></span>

<span data-ttu-id="0cc2d-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0cc2d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cc2d-110">備註</span><span class="sxs-lookup"><span data-stu-id="0cc2d-110">Remarks</span></span>

<span data-ttu-id="0cc2d-111">此成員函式會呼叫 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法，以針對佇列中所需的最早時間設定通知。</span><span class="sxs-lookup"><span data-stu-id="0cc2d-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="0cc2d-112">一律會檢查延遲的呈現時間命令。</span><span class="sxs-lookup"><span data-stu-id="0cc2d-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="0cc2d-113">如果篩選圖形處於執行模式，則也會檢查使用資料流程時間的延後命令。</span><span class="sxs-lookup"><span data-stu-id="0cc2d-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc2d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cc2d-114">Requirements</span></span>



| <span data-ttu-id="0cc2d-115">需求</span><span class="sxs-lookup"><span data-stu-id="0cc2d-115">Requirement</span></span> | <span data-ttu-id="0cc2d-116">值</span><span class="sxs-lookup"><span data-stu-id="0cc2d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc2d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0cc2d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0cc2d-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0cc2d-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0cc2d-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0cc2d-119">Library</span></span><br/> | <dl> <span data-ttu-id="0cc2d-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0cc2d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc2d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cc2d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc2d-122">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="0cc2d-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




