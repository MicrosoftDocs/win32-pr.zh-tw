---
description: ConvertTimeFormat 方法會從一種時間格式轉換成另一種格式。 這個方法會實 IMediaSeeking：： ConvertTimeFormat 方法。
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: 'CSourceSeeking. ConvertTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990128"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="42095-104">CSourceSeeking. ConvertTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="42095-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="42095-105">`ConvertTimeFormat`方法會從一種時間格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="42095-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="42095-106">這個方法會實 [**IMediaSeeking：： ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="42095-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42095-107">語法</span><span class="sxs-lookup"><span data-stu-id="42095-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="42095-108">參數</span><span class="sxs-lookup"><span data-stu-id="42095-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42095-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="42095-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="42095-110">接收轉換時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="42095-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="42095-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="42095-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="42095-112">目標格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="42095-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="42095-113">如果是 **Null**，則會使用目前的格式。</span><span class="sxs-lookup"><span data-stu-id="42095-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="42095-114">請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="42095-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="42095-115">*來源*</span><span class="sxs-lookup"><span data-stu-id="42095-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="42095-116">要轉換的時間值。</span><span class="sxs-lookup"><span data-stu-id="42095-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="42095-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="42095-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="42095-118">要轉換之格式的時間格式 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="42095-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="42095-119">如果是 **Null**，則會使用目前的格式。</span><span class="sxs-lookup"><span data-stu-id="42095-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42095-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="42095-120">Return value</span></span>

<span data-ttu-id="42095-121">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="42095-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="42095-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42095-122">Return code</span></span>                                                                                  | <span data-ttu-id="42095-123">Description</span><span class="sxs-lookup"><span data-stu-id="42095-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="42095-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42095-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="42095-125">Success</span><span class="sxs-lookup"><span data-stu-id="42095-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="42095-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="42095-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="42095-127">引數無效</span><span class="sxs-lookup"><span data-stu-id="42095-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="42095-128"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="42095-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="42095-129">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="42095-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42095-130">備註</span><span class="sxs-lookup"><span data-stu-id="42095-130">Remarks</span></span>

<span data-ttu-id="42095-131">基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="42095-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="42095-132">這個方法會傳回 E \_ INVALIDARG，但在一般情況下， *PTargetFormat* 和 *pSourceFormat* 都指定時間 \_ 格式 \_ 媒體 \_ 時間。</span><span class="sxs-lookup"><span data-stu-id="42095-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="42095-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="42095-133">Requirements</span></span>



| <span data-ttu-id="42095-134">需求</span><span class="sxs-lookup"><span data-stu-id="42095-134">Requirement</span></span> | <span data-ttu-id="42095-135">值</span><span class="sxs-lookup"><span data-stu-id="42095-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42095-136">標頭</span><span class="sxs-lookup"><span data-stu-id="42095-136">Header</span></span><br/>  | <dl> <span data-ttu-id="42095-137"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="42095-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42095-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="42095-138">Library</span></span><br/> | <dl> <span data-ttu-id="42095-139"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="42095-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42095-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42095-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42095-141">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="42095-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




