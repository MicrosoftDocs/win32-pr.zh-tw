---
description: GetCurrentSample 方法會抓取目前的範例。
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: 'CBaseRenderer. GetCurrentSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987175"
---
# <a name="cbaserenderergetcurrentsample-method"></a><span data-ttu-id="07172-103">CBaseRenderer. GetCurrentSample 方法</span><span class="sxs-lookup"><span data-stu-id="07172-103">CBaseRenderer.GetCurrentSample method</span></span>

<span data-ttu-id="07172-104">方法會抓取 `GetCurrentSample` 目前的範例。</span><span class="sxs-lookup"><span data-stu-id="07172-104">The `GetCurrentSample` method retrieves the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="07172-105">語法</span><span class="sxs-lookup"><span data-stu-id="07172-105">Syntax</span></span>


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a><span data-ttu-id="07172-106">參數</span><span class="sxs-lookup"><span data-stu-id="07172-106">Parameters</span></span>

<span data-ttu-id="07172-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="07172-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07172-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="07172-108">Return value</span></span>

<span data-ttu-id="07172-109">傳回範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標，如果沒有可用的範例，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="07172-109">Returns a pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface, or **NULL** if no sample is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="07172-110">備註</span><span class="sxs-lookup"><span data-stu-id="07172-110">Remarks</span></span>

<span data-ttu-id="07172-111">除非方法傳回 **Null**，否則方法會先在 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)指標上呼叫 **AddRef** ，然後再將它傳回。</span><span class="sxs-lookup"><span data-stu-id="07172-111">Unless the method returns **NULL**, the method calls **AddRef** on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer before returning it.</span></span> <span data-ttu-id="07172-112">呼叫端必須釋放指標。</span><span class="sxs-lookup"><span data-stu-id="07172-112">The caller must release the pointer.</span></span> <span data-ttu-id="07172-113">藉由隱含方式 (，您必須將傳回值指派給變數，以便您可以在稍後釋放它。 ) </span><span class="sxs-lookup"><span data-stu-id="07172-113">(By implication, you must assign the return value to a variable, so that you can release it later.)</span></span>

## <a name="requirements"></a><span data-ttu-id="07172-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="07172-114">Requirements</span></span>



| <span data-ttu-id="07172-115">需求</span><span class="sxs-lookup"><span data-stu-id="07172-115">Requirement</span></span> | <span data-ttu-id="07172-116">值</span><span class="sxs-lookup"><span data-stu-id="07172-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07172-117">標頭</span><span class="sxs-lookup"><span data-stu-id="07172-117">Header</span></span><br/>  | <dl> <span data-ttu-id="07172-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="07172-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07172-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="07172-119">Library</span></span><br/> | <dl> <span data-ttu-id="07172-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="07172-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07172-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07172-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07172-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="07172-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




