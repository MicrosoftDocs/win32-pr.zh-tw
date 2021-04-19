---
description: OnStartStreaming 方法會重設控制串流處理的所有時間。
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: 'CBaseVideoRenderer. OnStartStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403d465d4ff9fe8ae9101b13e2ec5e6c04bdddf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975980"
---
# <a name="cbasevideorendereronstartstreaming-method"></a><span data-ttu-id="45e92-103">CBaseVideoRenderer. OnStartStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="45e92-103">CBaseVideoRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="45e92-104">`OnStartStreaming`方法會重設控制串流處理的所有時間。</span><span class="sxs-lookup"><span data-stu-id="45e92-104">The `OnStartStreaming` method resets all times that control streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="45e92-105">語法</span><span class="sxs-lookup"><span data-stu-id="45e92-105">Syntax</span></span>


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="45e92-106">參數</span><span class="sxs-lookup"><span data-stu-id="45e92-106">Parameters</span></span>

<span data-ttu-id="45e92-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="45e92-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45e92-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="45e92-108">Return value</span></span>

<span data-ttu-id="45e92-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="45e92-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45e92-110">備註</span><span class="sxs-lookup"><span data-stu-id="45e92-110">Remarks</span></span>

<span data-ttu-id="45e92-111">此成員函式會覆寫 [**CBaseRenderer：： OnStartStreaming**](cbaserenderer-onstartstreaming.md)。</span><span class="sxs-lookup"><span data-stu-id="45e92-111">This member function overrides [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45e92-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="45e92-112">Requirements</span></span>



| <span data-ttu-id="45e92-113">需求</span><span class="sxs-lookup"><span data-stu-id="45e92-113">Requirement</span></span> | <span data-ttu-id="45e92-114">值</span><span class="sxs-lookup"><span data-stu-id="45e92-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e92-115">標頭</span><span class="sxs-lookup"><span data-stu-id="45e92-115">Header</span></span><br/>  | <dl> <span data-ttu-id="45e92-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="45e92-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="45e92-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="45e92-117">Library</span></span><br/> | <dl> <span data-ttu-id="45e92-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="45e92-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45e92-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45e92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45e92-120">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="45e92-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




