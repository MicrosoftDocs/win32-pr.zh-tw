---
description: IsStopped 方法會判斷篩選目前是否已停止。
ms.assetid: 89358523-d8e2-4c79-9ab8-6cc2f77a277f
title: 'CBaseFilter. IsStopped 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681ceb0a8dcc6b82a2bd6845119e2ca7fe0128eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995434"
---
# <a name="cbasefilterisstopped-method"></a><span data-ttu-id="d43eb-103">CBaseFilter. IsStopped 方法</span><span class="sxs-lookup"><span data-stu-id="d43eb-103">CBaseFilter.IsStopped method</span></span>

<span data-ttu-id="d43eb-104">`IsStopped`方法會判斷篩選目前是否已停止。</span><span class="sxs-lookup"><span data-stu-id="d43eb-104">The `IsStopped` method determines whether the filter is currently stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d43eb-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="d43eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="d43eb-106">Parameters</span></span>

<span data-ttu-id="d43eb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d43eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d43eb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d43eb-108">Return value</span></span>

<span data-ttu-id="d43eb-109">如果篩選已停止，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d43eb-109">Returns **TRUE** if the filter is stopped, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43eb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d43eb-110">Requirements</span></span>



| <span data-ttu-id="d43eb-111">需求</span><span class="sxs-lookup"><span data-stu-id="d43eb-111">Requirement</span></span> | <span data-ttu-id="d43eb-112">值</span><span class="sxs-lookup"><span data-stu-id="d43eb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d43eb-113">標頭</span><span class="sxs-lookup"><span data-stu-id="d43eb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d43eb-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d43eb-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d43eb-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="d43eb-115">Library</span></span><br/> | <dl> <span data-ttu-id="d43eb-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d43eb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d43eb-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d43eb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43eb-118">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="d43eb-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




