---
description: OnStopStreaming 方法會在串流結束時呼叫，以修正屬性頁報表的時間。
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: 'CBaseVideoRenderer. OnStopStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990110"
---
# <a name="cbasevideorendereronstopstreaming-method"></a><span data-ttu-id="ff4ba-103">CBaseVideoRenderer. OnStopStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="ff4ba-103">CBaseVideoRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="ff4ba-104">在 `OnStopStreaming` 串流結束時呼叫方法，以修正屬性頁報表的時間。</span><span class="sxs-lookup"><span data-stu-id="ff4ba-104">The `OnStopStreaming` method is called at the end of streaming to fix times for the property page report.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff4ba-105">Syntax</span></span>


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="ff4ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff4ba-106">Parameters</span></span>

<span data-ttu-id="ff4ba-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ff4ba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff4ba-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff4ba-108">Return value</span></span>

<span data-ttu-id="ff4ba-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ff4ba-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff4ba-110">備註</span><span class="sxs-lookup"><span data-stu-id="ff4ba-110">Remarks</span></span>

<span data-ttu-id="ff4ba-111">這個成員函式會被呼叫兩次，一次在暫停時，當資料流程實際上停止時。</span><span class="sxs-lookup"><span data-stu-id="ff4ba-111">This member function is called twice, once when pausing and again when the stream is actually stopped.</span></span>

<span data-ttu-id="ff4ba-112">此成員函式會覆寫 [**CBaseRenderer：： OnStopStreaming**](cbaserenderer-onstopstreaming.md)。</span><span class="sxs-lookup"><span data-stu-id="ff4ba-112">This member function overrides [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4ba-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff4ba-113">Requirements</span></span>



| <span data-ttu-id="ff4ba-114">需求</span><span class="sxs-lookup"><span data-stu-id="ff4ba-114">Requirement</span></span> | <span data-ttu-id="ff4ba-115">值</span><span class="sxs-lookup"><span data-stu-id="ff4ba-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4ba-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ff4ba-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ff4ba-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ff4ba-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff4ba-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff4ba-118">Library</span></span><br/> | <dl> <span data-ttu-id="ff4ba-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ff4ba-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff4ba-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff4ba-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff4ba-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="ff4ba-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




