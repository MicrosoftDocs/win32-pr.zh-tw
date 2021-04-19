---
description: GetDuration 方法會捕獲資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetDuration 方法。
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: 'CSourceSeeking. GetDuration 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978766"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="78a46-104">CSourceSeeking. GetDuration 方法</span><span class="sxs-lookup"><span data-stu-id="78a46-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="78a46-105">`GetDuration`方法會捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="78a46-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="78a46-106">這個方法會實 [**IMediaSeeking：： GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) 方法。</span><span class="sxs-lookup"><span data-stu-id="78a46-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a46-107">語法</span><span class="sxs-lookup"><span data-stu-id="78a46-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="78a46-108">參數</span><span class="sxs-lookup"><span data-stu-id="78a46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78a46-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="78a46-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="78a46-110">接收持續時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="78a46-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78a46-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="78a46-111">Return value</span></span>

<span data-ttu-id="78a46-112">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="78a46-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="78a46-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="78a46-113">Return code</span></span>                                                                               | <span data-ttu-id="78a46-114">Description</span><span class="sxs-lookup"><span data-stu-id="78a46-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="78a46-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="78a46-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="78a46-116">Success</span><span class="sxs-lookup"><span data-stu-id="78a46-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="78a46-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="78a46-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="78a46-118">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="78a46-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78a46-119">備註</span><span class="sxs-lookup"><span data-stu-id="78a46-119">Remarks</span></span>

<span data-ttu-id="78a46-120">持續期間是由 [**CSourceSeeking：： m \_ rtDuration**](csourceseeking-m-rtduration.md) 成員變數所指定。</span><span class="sxs-lookup"><span data-stu-id="78a46-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="78a46-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="78a46-121">Requirements</span></span>



| <span data-ttu-id="78a46-122">需求</span><span class="sxs-lookup"><span data-stu-id="78a46-122">Requirement</span></span> | <span data-ttu-id="78a46-123">值</span><span class="sxs-lookup"><span data-stu-id="78a46-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a46-124">標頭</span><span class="sxs-lookup"><span data-stu-id="78a46-124">Header</span></span><br/>  | <dl> <span data-ttu-id="78a46-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="78a46-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78a46-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="78a46-126">Library</span></span><br/> | <dl> <span data-ttu-id="78a46-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="78a46-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a46-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78a46-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a46-129">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="78a46-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




