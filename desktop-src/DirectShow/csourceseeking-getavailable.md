---
description: CSourceSeeking. GetAvailable 方法-GetAvailable 方法會捕獲搜尋效率的範圍。 這個方法會實 IMediaSeeking：： GetAvailable 方法。
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
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085236"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="62b6e-104">CSourceSeeking. GetAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="62b6e-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="62b6e-105">`GetAvailable`方法會捕獲搜尋效率的範圍。</span><span class="sxs-lookup"><span data-stu-id="62b6e-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="62b6e-106">這個方法會實 [**IMediaSeeking：： GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) 方法。</span><span class="sxs-lookup"><span data-stu-id="62b6e-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b6e-107">語法</span><span class="sxs-lookup"><span data-stu-id="62b6e-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="62b6e-108">參數</span><span class="sxs-lookup"><span data-stu-id="62b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b6e-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="62b6e-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="62b6e-110">變數的指標，此變數會接收有效率搜尋的最早時間。</span><span class="sxs-lookup"><span data-stu-id="62b6e-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="62b6e-111">變數設定為零。</span><span class="sxs-lookup"><span data-stu-id="62b6e-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="62b6e-112">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="62b6e-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="62b6e-113">變數的指標，此變數會接收有效率搜尋的最新時間。</span><span class="sxs-lookup"><span data-stu-id="62b6e-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="62b6e-114">變數會設定為 [**CSourceSeeking：： m \_ rtDuration**](csourceseeking-m-rtduration.md) 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="62b6e-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b6e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="62b6e-115">Return value</span></span>

<span data-ttu-id="62b6e-116">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="62b6e-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b6e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="62b6e-117">Requirements</span></span>



| <span data-ttu-id="62b6e-118">需求</span><span class="sxs-lookup"><span data-stu-id="62b6e-118">Requirement</span></span> | <span data-ttu-id="62b6e-119">值</span><span class="sxs-lookup"><span data-stu-id="62b6e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b6e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="62b6e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="62b6e-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="62b6e-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62b6e-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="62b6e-122">Library</span></span><br/> | <dl> <span data-ttu-id="62b6e-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="62b6e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b6e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62b6e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b6e-125">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="62b6e-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




