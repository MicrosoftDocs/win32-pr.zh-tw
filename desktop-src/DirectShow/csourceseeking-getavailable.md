---
description: GetAvailable 方法會捕獲搜尋效率的範圍。 這個方法會實 IMediaSeeking：： GetAvailable 方法。
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: 'CSourceSeeking. GetAvailable 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977754"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="d50e5-104">CSourceSeeking. GetAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="d50e5-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="d50e5-105">`GetAvailable`方法會捕獲搜尋效率的範圍。</span><span class="sxs-lookup"><span data-stu-id="d50e5-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="d50e5-106">這個方法會實 [**IMediaSeeking：： GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) 方法。</span><span class="sxs-lookup"><span data-stu-id="d50e5-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d50e5-107">語法</span><span class="sxs-lookup"><span data-stu-id="d50e5-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="d50e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="d50e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50e5-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="d50e5-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="d50e5-110">變數的指標，此變數會接收有效率搜尋的最早時間。</span><span class="sxs-lookup"><span data-stu-id="d50e5-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="d50e5-111">變數設定為零。</span><span class="sxs-lookup"><span data-stu-id="d50e5-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d50e5-112">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="d50e5-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="d50e5-113">變數的指標，此變數會接收有效率搜尋的最新時間。</span><span class="sxs-lookup"><span data-stu-id="d50e5-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="d50e5-114">變數會設定為 [**CSourceSeeking：： m \_ rtDuration**](csourceseeking-m-rtduration.md) 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="d50e5-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d50e5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d50e5-115">Return value</span></span>

<span data-ttu-id="d50e5-116">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d50e5-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d50e5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d50e5-117">Requirements</span></span>



| <span data-ttu-id="d50e5-118">需求</span><span class="sxs-lookup"><span data-stu-id="d50e5-118">Requirement</span></span> | <span data-ttu-id="d50e5-119">值</span><span class="sxs-lookup"><span data-stu-id="d50e5-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50e5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d50e5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d50e5-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d50e5-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d50e5-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="d50e5-122">Library</span></span><br/> | <dl> <span data-ttu-id="d50e5-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d50e5-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d50e5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d50e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50e5-125">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="d50e5-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




