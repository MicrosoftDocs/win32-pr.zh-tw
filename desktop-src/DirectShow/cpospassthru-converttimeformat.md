---
description: CPosPassThru. ConvertTimeFormat 方法-ConvertTimeFormat 方法會將一段時間格式轉換成另一種格式。 這個方法會實 IMediaSeeking：： ConvertTimeFormat 方法。
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: 'CPosPassThru. ConvertTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098956"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="cf97d-104">CPosPassThru. ConvertTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="cf97d-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="cf97d-105">`ConvertTimeFormat`方法會從一種時間格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="cf97d-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="cf97d-106">這個方法會實 [**IMediaSeeking：： ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="cf97d-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf97d-107">語法</span><span class="sxs-lookup"><span data-stu-id="cf97d-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="cf97d-108">參數</span><span class="sxs-lookup"><span data-stu-id="cf97d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf97d-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="cf97d-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="cf97d-110">接收轉換時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="cf97d-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="cf97d-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="cf97d-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="cf97d-112">目標格式之時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="cf97d-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="cf97d-113">如果是 **Null**，則會使用目前的格式。</span><span class="sxs-lookup"><span data-stu-id="cf97d-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="cf97d-114">*來源*</span><span class="sxs-lookup"><span data-stu-id="cf97d-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="cf97d-115">要轉換的時間值。</span><span class="sxs-lookup"><span data-stu-id="cf97d-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="cf97d-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="cf97d-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="cf97d-117">要轉換之格式的時間格式 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="cf97d-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="cf97d-118">如果是 **Null**，則會使用目前的格式。</span><span class="sxs-lookup"><span data-stu-id="cf97d-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf97d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf97d-119">Return value</span></span>

<span data-ttu-id="cf97d-120">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cf97d-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf97d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf97d-121">Requirements</span></span>



| <span data-ttu-id="cf97d-122">需求</span><span class="sxs-lookup"><span data-stu-id="cf97d-122">Requirement</span></span> | <span data-ttu-id="cf97d-123">值</span><span class="sxs-lookup"><span data-stu-id="cf97d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf97d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cf97d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cf97d-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cf97d-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf97d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf97d-126">Library</span></span><br/> | <dl> <span data-ttu-id="cf97d-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cf97d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf97d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf97d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf97d-129">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="cf97d-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="cf97d-130">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="cf97d-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




