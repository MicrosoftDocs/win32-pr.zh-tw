---
description: 暫停物件。 實 IMediaFilter：:P ause 方法。
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: 'CBaseMediaFilter： Pause 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992802"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="e396b-104">CBaseMediaFilter. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="e396b-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="e396b-105">暫停物件。</span><span class="sxs-lookup"><span data-stu-id="e396b-105">Pauses the object.</span></span> <span data-ttu-id="e396b-106">實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。</span><span class="sxs-lookup"><span data-stu-id="e396b-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e396b-107">語法</span><span class="sxs-lookup"><span data-stu-id="e396b-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="e396b-108">參數</span><span class="sxs-lookup"><span data-stu-id="e396b-108">Parameters</span></span>

<span data-ttu-id="e396b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e396b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e396b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e396b-110">Return value</span></span>

<span data-ttu-id="e396b-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e396b-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e396b-112">備註</span><span class="sxs-lookup"><span data-stu-id="e396b-112">Remarks</span></span>

<span data-ttu-id="e396b-113">在基類中，這個方法會將 [**CBaseMediaFilter：： m \_ state**](cbasemediafilter-m-state.md) 成員變數設定為暫停狀態， \_ 但不會執行任何其他動作。</span><span class="sxs-lookup"><span data-stu-id="e396b-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="e396b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e396b-114">Requirements</span></span>



| <span data-ttu-id="e396b-115">需求</span><span class="sxs-lookup"><span data-stu-id="e396b-115">Requirement</span></span> | <span data-ttu-id="e396b-116">值</span><span class="sxs-lookup"><span data-stu-id="e396b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e396b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e396b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e396b-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e396b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e396b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e396b-119">Library</span></span><br/> | <dl> <span data-ttu-id="e396b-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e396b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e396b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e396b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e396b-122">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="e396b-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




