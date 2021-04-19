---
description: SignalTimerFired 方法會清除用來排程轉譯的計時器識別碼。
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: 'CBaseRenderer. SignalTimerFired 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998642"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="81c27-103">CBaseRenderer. SignalTimerFired 方法</span><span class="sxs-lookup"><span data-stu-id="81c27-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="81c27-104">`SignalTimerFired`方法會清除用來排程轉譯的計時器識別碼。</span><span class="sxs-lookup"><span data-stu-id="81c27-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c27-105">語法</span><span class="sxs-lookup"><span data-stu-id="81c27-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="81c27-106">參數</span><span class="sxs-lookup"><span data-stu-id="81c27-106">Parameters</span></span>

<span data-ttu-id="81c27-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="81c27-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81c27-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="81c27-108">Return value</span></span>

<span data-ttu-id="81c27-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="81c27-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81c27-110">備註</span><span class="sxs-lookup"><span data-stu-id="81c27-110">Remarks</span></span>

<span data-ttu-id="81c27-111">當轉譯計時器啟動時，篩選會呼叫這個方法 (請參閱 [**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) 或當計時器取消時 (參閱 [**CBaseRenderer：： CancelNotification**](cbaserenderer-cancelnotification.md)) 。</span><span class="sxs-lookup"><span data-stu-id="81c27-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="81c27-112">方法會將 [**CBaseRenderer：： m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) 成員變數重設為零。</span><span class="sxs-lookup"><span data-stu-id="81c27-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="81c27-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="81c27-113">Requirements</span></span>



| <span data-ttu-id="81c27-114">需求</span><span class="sxs-lookup"><span data-stu-id="81c27-114">Requirement</span></span> | <span data-ttu-id="81c27-115">值</span><span class="sxs-lookup"><span data-stu-id="81c27-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81c27-116">標頭</span><span class="sxs-lookup"><span data-stu-id="81c27-116">Header</span></span><br/>  | <dl> <span data-ttu-id="81c27-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81c27-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81c27-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="81c27-118">Library</span></span><br/> | <dl> <span data-ttu-id="81c27-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81c27-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81c27-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81c27-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c27-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="81c27-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




