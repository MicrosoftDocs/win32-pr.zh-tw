---
description: IsEndOfStreamDelivered 方法會查詢是否已將 EC \_ 完成事件傳遞至篩選圖形管理員。
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: 'CBaseRenderer. IsEndOfStreamDelivered 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989687"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a><span data-ttu-id="28beb-103">CBaseRenderer. IsEndOfStreamDelivered 方法</span><span class="sxs-lookup"><span data-stu-id="28beb-103">CBaseRenderer.IsEndOfStreamDelivered method</span></span>

<span data-ttu-id="28beb-104">`IsEndOfStreamDelivered`方法會查詢是否已將 EC \_ 完成事件傳遞至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="28beb-104">The `IsEndOfStreamDelivered` method queries whether the EC\_COMPLETE event has been delivered to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="28beb-105">語法</span><span class="sxs-lookup"><span data-stu-id="28beb-105">Syntax</span></span>


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a><span data-ttu-id="28beb-106">參數</span><span class="sxs-lookup"><span data-stu-id="28beb-106">Parameters</span></span>

<span data-ttu-id="28beb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="28beb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28beb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="28beb-108">Return value</span></span>

<span data-ttu-id="28beb-109">傳回 [**CBaseRenderer：： m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="28beb-109">Returns the [**CBaseRenderer::m\_bEOSDelivered**](cbaserenderer-m-beosdelivered.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="28beb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="28beb-110">Requirements</span></span>



| <span data-ttu-id="28beb-111">需求</span><span class="sxs-lookup"><span data-stu-id="28beb-111">Requirement</span></span> | <span data-ttu-id="28beb-112">值</span><span class="sxs-lookup"><span data-stu-id="28beb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28beb-113">標頭</span><span class="sxs-lookup"><span data-stu-id="28beb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="28beb-114"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="28beb-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28beb-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="28beb-115">Library</span></span><br/> | <dl> <span data-ttu-id="28beb-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="28beb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28beb-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28beb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28beb-118">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="28beb-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




