---
description: DoRenderSample 方法會呈現範例。
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: 'CBaseRenderer. DoRenderSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983082"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="ed186-103">CBaseRenderer. DoRenderSample 方法</span><span class="sxs-lookup"><span data-stu-id="ed186-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="ed186-104">`DoRenderSample`方法會呈現範例。</span><span class="sxs-lookup"><span data-stu-id="ed186-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed186-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed186-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="ed186-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed186-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed186-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="ed186-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ed186-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ed186-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed186-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed186-109">Return value</span></span>

<span data-ttu-id="ed186-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ed186-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed186-111">備註</span><span class="sxs-lookup"><span data-stu-id="ed186-111">Remarks</span></span>

<span data-ttu-id="ed186-112">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="ed186-112">The derived class must implement this method.</span></span> <span data-ttu-id="ed186-113">行為完全取決於所要執行之篩選的類型。</span><span class="sxs-lookup"><span data-stu-id="ed186-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="ed186-114">例如，影片轉譯器會繪製範例中所包含的影片影像。</span><span class="sxs-lookup"><span data-stu-id="ed186-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed186-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed186-115">Requirements</span></span>



| <span data-ttu-id="ed186-116">需求</span><span class="sxs-lookup"><span data-stu-id="ed186-116">Requirement</span></span> | <span data-ttu-id="ed186-117">值</span><span class="sxs-lookup"><span data-stu-id="ed186-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed186-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ed186-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ed186-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ed186-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed186-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed186-120">Library</span></span><br/> | <dl> <span data-ttu-id="ed186-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed186-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed186-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed186-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed186-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="ed186-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




