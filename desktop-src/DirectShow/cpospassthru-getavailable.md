---
description: CPosPassThru. GetAvailable 方法-GetAvailable 方法會捕獲搜尋效率的範圍。 這個方法會實 IMediaSeeking：： GetAvailable 方法。
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: 'CPosPassThru. GetAvailable 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d56827a68f4c287e5808f0d8f64b8142c31b1f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095286"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="d2e0e-104">CPosPassThru. GetAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="d2e0e-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="d2e0e-105">`GetAvailable`方法會捕獲搜尋效率的範圍。</span><span class="sxs-lookup"><span data-stu-id="d2e0e-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="d2e0e-106">這個方法會實 [**IMediaSeeking：： GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) 方法。</span><span class="sxs-lookup"><span data-stu-id="d2e0e-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e0e-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2e0e-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="d2e0e-108">參數</span><span class="sxs-lookup"><span data-stu-id="d2e0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e0e-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="d2e0e-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="d2e0e-110">變數的指標，此變數會接收有效率搜尋的最早時間。</span><span class="sxs-lookup"><span data-stu-id="d2e0e-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="d2e0e-111">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="d2e0e-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="d2e0e-112">變數的指標，此變數會接收有效率搜尋的最新時間。</span><span class="sxs-lookup"><span data-stu-id="d2e0e-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e0e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2e0e-113">Return value</span></span>

<span data-ttu-id="d2e0e-114">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d2e0e-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e0e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2e0e-115">Requirements</span></span>



| <span data-ttu-id="d2e0e-116">需求</span><span class="sxs-lookup"><span data-stu-id="d2e0e-116">Requirement</span></span> | <span data-ttu-id="d2e0e-117">值</span><span class="sxs-lookup"><span data-stu-id="d2e0e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e0e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d2e0e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d2e0e-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d2e0e-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2e0e-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2e0e-120">Library</span></span><br/> | <dl> <span data-ttu-id="d2e0e-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d2e0e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2e0e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2e0e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e0e-123">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="d2e0e-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




