---
description: GetRealState 方法會捕獲篩選狀態。
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: 'CBaseRenderer. GetRealState 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995226"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="21138-103">CBaseRenderer. GetRealState 方法</span><span class="sxs-lookup"><span data-stu-id="21138-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="21138-104">`GetRealState`方法會捕獲篩選狀態。</span><span class="sxs-lookup"><span data-stu-id="21138-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="21138-105">語法</span><span class="sxs-lookup"><span data-stu-id="21138-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="21138-106">參數</span><span class="sxs-lookup"><span data-stu-id="21138-106">Parameters</span></span>

<span data-ttu-id="21138-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="21138-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21138-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="21138-108">Return value</span></span>

<span data-ttu-id="21138-109">傳回 [**CBaseFilter：： m \_ 狀態**](cbasefilter-m-state.md)的值。</span><span class="sxs-lookup"><span data-stu-id="21138-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="21138-110">此值為 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員。</span><span class="sxs-lookup"><span data-stu-id="21138-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="21138-111">備註</span><span class="sxs-lookup"><span data-stu-id="21138-111">Remarks</span></span>

<span data-ttu-id="21138-112">此方法提供更簡單的 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法替代方式，以供內部使用。</span><span class="sxs-lookup"><span data-stu-id="21138-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="21138-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="21138-113">Requirements</span></span>



| <span data-ttu-id="21138-114">需求</span><span class="sxs-lookup"><span data-stu-id="21138-114">Requirement</span></span> | <span data-ttu-id="21138-115">值</span><span class="sxs-lookup"><span data-stu-id="21138-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21138-116">標頭</span><span class="sxs-lookup"><span data-stu-id="21138-116">Header</span></span><br/>  | <dl> <span data-ttu-id="21138-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="21138-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21138-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="21138-118">Library</span></span><br/> | <dl> <span data-ttu-id="21138-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="21138-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21138-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21138-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21138-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="21138-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




