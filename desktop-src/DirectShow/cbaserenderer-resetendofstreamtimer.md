---
description: ResetEndOfStreamTimer 方法會取消排定 EC \_ 完成通知的計時器。
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: 'CBaseRenderer. ResetEndOfStreamTimer 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984459"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a><span data-ttu-id="be38b-103">CBaseRenderer. ResetEndOfStreamTimer 方法</span><span class="sxs-lookup"><span data-stu-id="be38b-103">CBaseRenderer.ResetEndOfStreamTimer method</span></span>

<span data-ttu-id="be38b-104">`ResetEndOfStreamTimer`方法會取消排定 [**EC \_ 完成**](ec-complete.md)通知的計時器。</span><span class="sxs-lookup"><span data-stu-id="be38b-104">The `ResetEndOfStreamTimer` method cancels the timer that schedules [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="be38b-105">語法</span><span class="sxs-lookup"><span data-stu-id="be38b-105">Syntax</span></span>


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a><span data-ttu-id="be38b-106">參數</span><span class="sxs-lookup"><span data-stu-id="be38b-106">Parameters</span></span>

<span data-ttu-id="be38b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="be38b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be38b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="be38b-108">Return value</span></span>

<span data-ttu-id="be38b-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="be38b-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be38b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="be38b-110">Requirements</span></span>



| <span data-ttu-id="be38b-111">需求</span><span class="sxs-lookup"><span data-stu-id="be38b-111">Requirement</span></span> | <span data-ttu-id="be38b-112">值</span><span class="sxs-lookup"><span data-stu-id="be38b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be38b-113">標頭</span><span class="sxs-lookup"><span data-stu-id="be38b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="be38b-114"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="be38b-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be38b-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="be38b-115">Library</span></span><br/> | <dl> <span data-ttu-id="be38b-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="be38b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be38b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be38b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be38b-118">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="be38b-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="be38b-119">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="be38b-119">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> <dt>

[<span data-ttu-id="be38b-120">**CBaseRenderer：： TimerCallback**</span><span class="sxs-lookup"><span data-stu-id="be38b-120">**CBaseRenderer::TimerCallback**</span></span>](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




