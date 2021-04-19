---
description: TimerCallback 方法是結束資料流程計時器事件的回呼方法。
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: 'CBaseRenderer. TimerCallback 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000985"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="30850-103">CBaseRenderer. TimerCallback 方法</span><span class="sxs-lookup"><span data-stu-id="30850-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="30850-104">`TimerCallback`方法是結束資料流程計時器事件的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="30850-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="30850-105">語法</span><span class="sxs-lookup"><span data-stu-id="30850-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="30850-106">參數</span><span class="sxs-lookup"><span data-stu-id="30850-106">Parameters</span></span>

<span data-ttu-id="30850-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="30850-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30850-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="30850-108">Return value</span></span>

<span data-ttu-id="30850-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="30850-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30850-110">備註</span><span class="sxs-lookup"><span data-stu-id="30850-110">Remarks</span></span>

<span data-ttu-id="30850-111">[**CBaseRenderer：： SendEndOfStream**](cbaserenderer-sendendofstream.md)方法會使用計時器事件來排程 EC \_ 完成的通知。</span><span class="sxs-lookup"><span data-stu-id="30850-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="30850-112">**CBaseRenderer：： TimerCallback** 方法是計時器事件的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="30850-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="30850-113">`TimerCallback`方法會再次呼叫 **SendEndOfStream** ，而 **SendEndOfStream** 會決定是要傳送 EC \_ 完成通知或設定另一個計時器。</span><span class="sxs-lookup"><span data-stu-id="30850-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="30850-114">[**CBaseRenderer：： ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)方法會取消計時器事件。</span><span class="sxs-lookup"><span data-stu-id="30850-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="30850-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="30850-115">Requirements</span></span>



| <span data-ttu-id="30850-116">需求</span><span class="sxs-lookup"><span data-stu-id="30850-116">Requirement</span></span> | <span data-ttu-id="30850-117">值</span><span class="sxs-lookup"><span data-stu-id="30850-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30850-118">標頭</span><span class="sxs-lookup"><span data-stu-id="30850-118">Header</span></span><br/>  | <dl> <span data-ttu-id="30850-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="30850-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30850-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="30850-120">Library</span></span><br/> | <dl> <span data-ttu-id="30850-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="30850-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30850-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30850-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30850-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="30850-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




