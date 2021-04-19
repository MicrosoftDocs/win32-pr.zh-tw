---
description: ConvertTimeFormat 方法會從一種時間格式轉換成另一種格式。 這個方法會實 IMediaSeeking：： ConvertTimeFormat 方法。
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
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989864"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="a08c4-104">CPosPassThru. ConvertTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="a08c4-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="a08c4-105">`ConvertTimeFormat`方法會從一種時間格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="a08c4-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="a08c4-106">這個方法會實 [**IMediaSeeking：： ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="a08c4-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08c4-107">語法</span><span class="sxs-lookup"><span data-stu-id="a08c4-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a08c4-108">參數</span><span class="sxs-lookup"><span data-stu-id="a08c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08c4-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="a08c4-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="a08c4-110">接收轉換時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="a08c4-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="a08c4-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="a08c4-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a08c4-112">目標格式之時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="a08c4-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="a08c4-113">如果是 **Null**，則會使用目前的格式。</span><span class="sxs-lookup"><span data-stu-id="a08c4-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="a08c4-114">*來源*</span><span class="sxs-lookup"><span data-stu-id="a08c4-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="a08c4-115">要轉換的時間值。</span><span class="sxs-lookup"><span data-stu-id="a08c4-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="a08c4-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="a08c4-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a08c4-117">要轉換之格式的時間格式 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="a08c4-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="a08c4-118">如果是 **Null**，則會使用目前的格式。</span><span class="sxs-lookup"><span data-stu-id="a08c4-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08c4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a08c4-119">Return value</span></span>

<span data-ttu-id="a08c4-120">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a08c4-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a08c4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a08c4-121">Requirements</span></span>



| <span data-ttu-id="a08c4-122">需求</span><span class="sxs-lookup"><span data-stu-id="a08c4-122">Requirement</span></span> | <span data-ttu-id="a08c4-123">值</span><span class="sxs-lookup"><span data-stu-id="a08c4-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08c4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a08c4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a08c4-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a08c4-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a08c4-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a08c4-126">Library</span></span><br/> | <dl> <span data-ttu-id="a08c4-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a08c4-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08c4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a08c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08c4-129">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="a08c4-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="a08c4-130">**時間格式 Guid**</span><span class="sxs-lookup"><span data-stu-id="a08c4-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




