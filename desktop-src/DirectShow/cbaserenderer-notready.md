---
description: NotReady 方法會通知狀態轉換尚未完成。
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: 'CBaseRenderer. NotReady 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001216"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="a2faf-103">CBaseRenderer. NotReady 方法</span><span class="sxs-lookup"><span data-stu-id="a2faf-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="a2faf-104">`NotReady`方法會指示狀態轉換尚未完成。</span><span class="sxs-lookup"><span data-stu-id="a2faf-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2faf-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2faf-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="a2faf-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2faf-106">Parameters</span></span>

<span data-ttu-id="a2faf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a2faf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2faf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2faf-108">Return value</span></span>

<span data-ttu-id="a2faf-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a2faf-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2faf-110">備註</span><span class="sxs-lookup"><span data-stu-id="a2faf-110">Remarks</span></span>

<span data-ttu-id="a2faf-111">這個方法會使 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法傳回 VFW \_ S \_ 狀態 \_ 中繼，表示篩選仍在轉換成目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="a2faf-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="a2faf-112">每當狀態轉換暫止時，篩選準則就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a2faf-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="a2faf-113"> (當篩選準則暫停時，就會發生這種情況，直到收到範例為止 ) </span><span class="sxs-lookup"><span data-stu-id="a2faf-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="a2faf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2faf-114">Requirements</span></span>



| <span data-ttu-id="a2faf-115">需求</span><span class="sxs-lookup"><span data-stu-id="a2faf-115">Requirement</span></span> | <span data-ttu-id="a2faf-116">值</span><span class="sxs-lookup"><span data-stu-id="a2faf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2faf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a2faf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2faf-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a2faf-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2faf-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2faf-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2faf-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a2faf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2faf-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2faf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2faf-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="a2faf-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="a2faf-123">**CheckReady**</span><span class="sxs-lookup"><span data-stu-id="a2faf-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="a2faf-124">**就緒**</span><span class="sxs-lookup"><span data-stu-id="a2faf-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




