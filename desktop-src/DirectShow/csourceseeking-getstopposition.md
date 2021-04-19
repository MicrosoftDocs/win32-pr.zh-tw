---
description: GetStopPosition 方法會捕獲播放將會停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetStopPosition 方法。
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: 'CSourceSeeking. GetStopPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998626"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="dc6fb-104">CSourceSeeking. GetStopPosition 方法</span><span class="sxs-lookup"><span data-stu-id="dc6fb-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="dc6fb-105">此 `GetStopPosition` 方法會抓取播放將停止的時間（相對於資料流程的持續時間）。</span><span class="sxs-lookup"><span data-stu-id="dc6fb-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="dc6fb-106">這個方法會實 [**IMediaSeeking：： GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="dc6fb-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc6fb-107">語法</span><span class="sxs-lookup"><span data-stu-id="dc6fb-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="dc6fb-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc6fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc6fb-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="dc6fb-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="dc6fb-110">接收停止時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="dc6fb-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc6fb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc6fb-111">Return value</span></span>

<span data-ttu-id="dc6fb-112">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dc6fb-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="dc6fb-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dc6fb-113">Return code</span></span>                                                                               | <span data-ttu-id="dc6fb-114">Description</span><span class="sxs-lookup"><span data-stu-id="dc6fb-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="dc6fb-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dc6fb-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="dc6fb-116">Success</span><span class="sxs-lookup"><span data-stu-id="dc6fb-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="dc6fb-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="dc6fb-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="dc6fb-118">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="dc6fb-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc6fb-119">備註</span><span class="sxs-lookup"><span data-stu-id="dc6fb-119">Remarks</span></span>

<span data-ttu-id="dc6fb-120">停止時間是由 [**CSourceSeeking：： m \_ rtStop**](csourceseeking-m-rtstop.md) 成員變數所指定。</span><span class="sxs-lookup"><span data-stu-id="dc6fb-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc6fb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc6fb-121">Requirements</span></span>



| <span data-ttu-id="dc6fb-122">需求</span><span class="sxs-lookup"><span data-stu-id="dc6fb-122">Requirement</span></span> | <span data-ttu-id="dc6fb-123">值</span><span class="sxs-lookup"><span data-stu-id="dc6fb-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6fb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dc6fb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dc6fb-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dc6fb-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc6fb-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="dc6fb-126">Library</span></span><br/> | <dl> <span data-ttu-id="dc6fb-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dc6fb-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc6fb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc6fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc6fb-129">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="dc6fb-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




