---
description: GetFilterGraph 方法會捕獲篩選圖形管理員的指標。
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: 'CBaseFilter. GetFilterGraph 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999255"
---
# <a name="cbasefiltergetfiltergraph-method"></a><span data-ttu-id="629ca-103">CBaseFilter. GetFilterGraph 方法</span><span class="sxs-lookup"><span data-stu-id="629ca-103">CBaseFilter.GetFilterGraph method</span></span>

<span data-ttu-id="629ca-104">`GetFilterGraph`方法會捕獲篩選圖形管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="629ca-104">The `GetFilterGraph` method retrieves a pointer to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="629ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="629ca-105">Syntax</span></span>


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a><span data-ttu-id="629ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="629ca-106">Parameters</span></span>

<span data-ttu-id="629ca-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="629ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="629ca-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="629ca-108">Return value</span></span>

<span data-ttu-id="629ca-109">傳回 [**CBaseFilter：： m \_ pGraph**](cbasefilter-m-pgraph.md)的值。</span><span class="sxs-lookup"><span data-stu-id="629ca-109">Returns the value of [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="629ca-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="629ca-110">Requirements</span></span>



| <span data-ttu-id="629ca-111">需求</span><span class="sxs-lookup"><span data-stu-id="629ca-111">Requirement</span></span> | <span data-ttu-id="629ca-112">值</span><span class="sxs-lookup"><span data-stu-id="629ca-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="629ca-113">標頭</span><span class="sxs-lookup"><span data-stu-id="629ca-113">Header</span></span><br/>  | <dl> <span data-ttu-id="629ca-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="629ca-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="629ca-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="629ca-115">Library</span></span><br/> | <dl> <span data-ttu-id="629ca-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="629ca-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629ca-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="629ca-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629ca-118">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="629ca-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




