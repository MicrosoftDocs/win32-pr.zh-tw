---
description: GetRenderEvent 方法會捕獲排程轉譯的事件。
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: 'CBaseRenderer. GetRenderEvent 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e2fd0b9cd98194129eccd2e24e6ee75577d1eec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975959"
---
# <a name="cbaserenderergetrenderevent-method"></a><span data-ttu-id="b59b5-103">CBaseRenderer. GetRenderEvent 方法</span><span class="sxs-lookup"><span data-stu-id="b59b5-103">CBaseRenderer.GetRenderEvent method</span></span>

<span data-ttu-id="b59b5-104">`GetRenderEvent`方法會捕獲排程轉譯的事件。</span><span class="sxs-lookup"><span data-stu-id="b59b5-104">The `GetRenderEvent` method retrieves the event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="b59b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="b59b5-105">Syntax</span></span>


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a><span data-ttu-id="b59b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="b59b5-106">Parameters</span></span>

<span data-ttu-id="b59b5-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b59b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b59b5-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b59b5-108">Return value</span></span>

<span data-ttu-id="b59b5-109">傳回 [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 事件的指標。</span><span class="sxs-lookup"><span data-stu-id="b59b5-109">Returns a pointer to the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b59b5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b59b5-110">Requirements</span></span>



| <span data-ttu-id="b59b5-111">需求</span><span class="sxs-lookup"><span data-stu-id="b59b5-111">Requirement</span></span> | <span data-ttu-id="b59b5-112">值</span><span class="sxs-lookup"><span data-stu-id="b59b5-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59b5-113">標頭</span><span class="sxs-lookup"><span data-stu-id="b59b5-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b59b5-114"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b59b5-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b59b5-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="b59b5-115">Library</span></span><br/> | <dl> <span data-ttu-id="b59b5-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b59b5-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59b5-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b59b5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59b5-118">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="b59b5-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




