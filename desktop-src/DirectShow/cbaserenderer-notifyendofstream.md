---
description: NotifyEndOfStream 方法會將 EC \_ 完成事件張貼至篩選圖形管理員。
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: 'CBaseRenderer. NotifyEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1187705bfa678252237bd95d9a4cb21a0f97d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990711"
---
# <a name="cbaserenderernotifyendofstream-method"></a><span data-ttu-id="c0e62-103">CBaseRenderer. NotifyEndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="c0e62-103">CBaseRenderer.NotifyEndOfStream method</span></span>

<span data-ttu-id="c0e62-104">方法會將 `NotifyEndOfStream` [**EC \_ 完成**](ec-complete.md) 事件張貼至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="c0e62-104">The `NotifyEndOfStream` method posts an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e62-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0e62-105">Syntax</span></span>


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="c0e62-106">參數</span><span class="sxs-lookup"><span data-stu-id="c0e62-106">Parameters</span></span>

<span data-ttu-id="c0e62-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0e62-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0e62-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0e62-108">Return value</span></span>

<span data-ttu-id="c0e62-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c0e62-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0e62-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0e62-110">Requirements</span></span>



| <span data-ttu-id="c0e62-111">需求</span><span class="sxs-lookup"><span data-stu-id="c0e62-111">Requirement</span></span> | <span data-ttu-id="c0e62-112">值</span><span class="sxs-lookup"><span data-stu-id="c0e62-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e62-113">標頭</span><span class="sxs-lookup"><span data-stu-id="c0e62-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c0e62-114"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c0e62-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0e62-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="c0e62-115">Library</span></span><br/> | <dl> <span data-ttu-id="c0e62-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c0e62-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0e62-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0e62-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e62-118">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="c0e62-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="c0e62-119">**CBaseRenderer::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="c0e62-119">**CBaseRenderer::EndOfStream**</span></span>](cbaserenderer-endofstream.md)
</dt> <dt>

[<span data-ttu-id="c0e62-120">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="c0e62-120">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




