---
description: SetPositions 方法會設定目前的位置和停止位置。 這個方法會實 IMediaSeeking：： SetPositions 方法。
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: 'CSourceSeeking. SetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977537"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="8601d-104">CSourceSeeking. SetPositions 方法</span><span class="sxs-lookup"><span data-stu-id="8601d-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="8601d-105">`SetPositions`方法會設定目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="8601d-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="8601d-106">這個方法會實 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法。</span><span class="sxs-lookup"><span data-stu-id="8601d-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8601d-107">語法</span><span class="sxs-lookup"><span data-stu-id="8601d-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8601d-108">參數</span><span class="sxs-lookup"><span data-stu-id="8601d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8601d-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="8601d-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="8601d-110">變數的指標，該變數會指定目前的位置。</span><span class="sxs-lookup"><span data-stu-id="8601d-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="8601d-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="8601d-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8601d-112">旗標的位組合。</span><span class="sxs-lookup"><span data-stu-id="8601d-112">Bitwise combination of flags.</span></span> <span data-ttu-id="8601d-113">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8601d-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8601d-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="8601d-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="8601d-115">指定停止時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="8601d-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="8601d-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="8601d-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8601d-117">旗標的位組合。</span><span class="sxs-lookup"><span data-stu-id="8601d-117">Bitwise combination of flags.</span></span> <span data-ttu-id="8601d-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8601d-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8601d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="8601d-119">Return value</span></span>

<span data-ttu-id="8601d-120">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8601d-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8601d-121">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="8601d-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="8601d-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8601d-122">Return code</span></span>                                                                                  | <span data-ttu-id="8601d-123">Description</span><span class="sxs-lookup"><span data-stu-id="8601d-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="8601d-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8601d-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8601d-125">Success</span><span class="sxs-lookup"><span data-stu-id="8601d-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="8601d-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8601d-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8601d-127">不正確旗標</span><span class="sxs-lookup"><span data-stu-id="8601d-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="8601d-128"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8601d-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="8601d-129">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="8601d-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8601d-130">備註</span><span class="sxs-lookup"><span data-stu-id="8601d-130">Remarks</span></span>

<span data-ttu-id="8601d-131">以下是支援的旗標：</span><span class="sxs-lookup"><span data-stu-id="8601d-131">The following flags are supported:</span></span>

-   <span data-ttu-id="8601d-132">\_搜尋 \_ NoPositioning</span><span class="sxs-lookup"><span data-stu-id="8601d-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="8601d-133">\_搜尋 \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="8601d-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="8601d-134">\_搜尋 \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="8601d-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="8601d-135">正在 \_ 搜尋 \_ IncrementalPositioning (僅 *pStop*) </span><span class="sxs-lookup"><span data-stu-id="8601d-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="8601d-136">如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)。</span><span class="sxs-lookup"><span data-stu-id="8601d-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="8601d-137">這個方法會更新 [**CSourceSeeking：： m \_ RtStart**](csourceseeking-m-rtstart.md) 和 [**CSourceSeeking：： m \_ rtStop**](csourceseeking-m-rtstop.md) 成員變數的值，然後呼叫純虛擬方法 [**CSourceSeeking：： ChangeStart**](csourceseeking-changestart.md) 和 [**CSourceSeeking：： ChangeStop**](csourceseeking-changestop.md)。</span><span class="sxs-lookup"><span data-stu-id="8601d-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8601d-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8601d-138">Requirements</span></span>



| <span data-ttu-id="8601d-139">需求</span><span class="sxs-lookup"><span data-stu-id="8601d-139">Requirement</span></span> | <span data-ttu-id="8601d-140">值</span><span class="sxs-lookup"><span data-stu-id="8601d-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8601d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="8601d-141">Header</span></span><br/>  | <dl> <span data-ttu-id="8601d-142"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8601d-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8601d-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="8601d-143">Library</span></span><br/> | <dl> <span data-ttu-id="8601d-144"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8601d-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8601d-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8601d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8601d-146">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="8601d-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




