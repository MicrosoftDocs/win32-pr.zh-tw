---
description: 當篩選參數切換到執行中狀態時，StartStreaming 方法會啟動串流處理。
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: 'CBaseRenderer. StartStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978500"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="5ae5b-103">CBaseRenderer. StartStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="5ae5b-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="5ae5b-104">`StartStreaming`當篩選參數切換到執行中狀態時，此方法會起始資料流程處理。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae5b-105">語法</span><span class="sxs-lookup"><span data-stu-id="5ae5b-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="5ae5b-106">參數</span><span class="sxs-lookup"><span data-stu-id="5ae5b-106">Parameters</span></span>

<span data-ttu-id="5ae5b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ae5b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ae5b-108">Return value</span></span>

<span data-ttu-id="5ae5b-109">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae5b-110">備註</span><span class="sxs-lookup"><span data-stu-id="5ae5b-110">Remarks</span></span>

<span data-ttu-id="5ae5b-111">如果篩選器有範例，則會排程轉譯的範例。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="5ae5b-112">否則，如果有暫止的資料流程結束通知，篩選準則會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="5ae5b-113">這個方法會呼叫 [**CBaseRenderer：： OnStartStreaming**](cbaserenderer-onstartstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="5ae5b-114">該方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="5ae5b-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae5b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ae5b-115">Requirements</span></span>



| <span data-ttu-id="5ae5b-116">需求</span><span class="sxs-lookup"><span data-stu-id="5ae5b-116">Requirement</span></span> | <span data-ttu-id="5ae5b-117">值</span><span class="sxs-lookup"><span data-stu-id="5ae5b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae5b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5ae5b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5ae5b-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5ae5b-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ae5b-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5ae5b-120">Library</span></span><br/> | <dl> <span data-ttu-id="5ae5b-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5ae5b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae5b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ae5b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae5b-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="5ae5b-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




