---
description: 當篩選開始進行串流處理時，會呼叫 OnStartStreaming 方法。
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: 'CBaseRenderer. OnStartStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994692"
---
# <a name="cbaserendereronstartstreaming-method"></a><span data-ttu-id="e1d03-103">CBaseRenderer. OnStartStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="e1d03-103">CBaseRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="e1d03-104">`OnStartStreaming`當篩選開始進行串流處理時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="e1d03-104">The `OnStartStreaming` method is called when the filter begins streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d03-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1d03-105">Syntax</span></span>


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="e1d03-106">參數</span><span class="sxs-lookup"><span data-stu-id="e1d03-106">Parameters</span></span>

<span data-ttu-id="e1d03-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e1d03-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1d03-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1d03-108">Return value</span></span>

<span data-ttu-id="e1d03-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e1d03-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d03-110">備註</span><span class="sxs-lookup"><span data-stu-id="e1d03-110">Remarks</span></span>

<span data-ttu-id="e1d03-111">[**CBaseRenderer：： StartStreaming**](cbaserenderer-startstreaming.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e1d03-111">The [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method calls this method.</span></span> <span data-ttu-id="e1d03-112">它不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="e1d03-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d03-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1d03-113">Requirements</span></span>



| <span data-ttu-id="e1d03-114">需求</span><span class="sxs-lookup"><span data-stu-id="e1d03-114">Requirement</span></span> | <span data-ttu-id="e1d03-115">值</span><span class="sxs-lookup"><span data-stu-id="e1d03-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d03-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e1d03-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d03-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d03-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1d03-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1d03-118">Library</span></span><br/> | <dl> <span data-ttu-id="e1d03-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d03-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d03-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1d03-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d03-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="e1d03-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




