---
description: GetPositions 方法會抓取目前的位置和停止位置。 這個方法會實 IMediaSeeking：： GetPositions 方法。
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: 'CSourceSeeking. GetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994133"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="30c6a-104">CSourceSeeking. GetPositions 方法</span><span class="sxs-lookup"><span data-stu-id="30c6a-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="30c6a-105">方法會抓取 `GetPositions` 目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="30c6a-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="30c6a-106">這個方法會實 [**IMediaSeeking：： GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) 方法。</span><span class="sxs-lookup"><span data-stu-id="30c6a-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c6a-107">語法</span><span class="sxs-lookup"><span data-stu-id="30c6a-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="30c6a-108">參數</span><span class="sxs-lookup"><span data-stu-id="30c6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c6a-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="30c6a-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="30c6a-110">接收開始位置之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="30c6a-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="30c6a-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="30c6a-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="30c6a-112">接收停用位置之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="30c6a-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c6a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="30c6a-113">Return value</span></span>

<span data-ttu-id="30c6a-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="30c6a-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="30c6a-115">備註</span><span class="sxs-lookup"><span data-stu-id="30c6a-115">Remarks</span></span>

<span data-ttu-id="30c6a-116">針對 *pCurrent* 參數，這個方法會傳回 [**CSourceSeeking：： m \_ rtStart**](csourceseeking-m-rtstart.md) 成員變數的值，其代表最新的搜尋時間，而不是目前的串流位置。</span><span class="sxs-lookup"><span data-stu-id="30c6a-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="30c6a-117">不過，當應用程式透過篩選圖形管理員呼叫 **IMediaSeeking：： GetPositions** 時，這些值通常來自轉譯器篩選器，而不是來源篩選。</span><span class="sxs-lookup"><span data-stu-id="30c6a-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c6a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="30c6a-118">Requirements</span></span>



| <span data-ttu-id="30c6a-119">需求</span><span class="sxs-lookup"><span data-stu-id="30c6a-119">Requirement</span></span> | <span data-ttu-id="30c6a-120">值</span><span class="sxs-lookup"><span data-stu-id="30c6a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c6a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="30c6a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="30c6a-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="30c6a-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30c6a-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="30c6a-123">Library</span></span><br/> | <dl> <span data-ttu-id="30c6a-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="30c6a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c6a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30c6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c6a-126">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="30c6a-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




