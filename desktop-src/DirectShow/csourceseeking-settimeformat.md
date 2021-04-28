---
description: CSourceSeeking. SetTimeFormat 方法-SetTimeFormat 方法會設定時間格式。 這個方法會實 IMediaSeeking：： SetTimeFormat 方法。
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: 'CSourceSeeking. SetTimeFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085196"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="6651c-104">CSourceSeeking. SetTimeFormat 方法</span><span class="sxs-lookup"><span data-stu-id="6651c-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="6651c-105">`SetTimeFormat`方法會設定時間格式。</span><span class="sxs-lookup"><span data-stu-id="6651c-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="6651c-106">這個方法會實 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="6651c-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6651c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6651c-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="6651c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6651c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6651c-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="6651c-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6651c-110">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="6651c-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="6651c-111">請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="6651c-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6651c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6651c-112">Return value</span></span>

<span data-ttu-id="6651c-113">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6651c-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="6651c-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6651c-114">Return code</span></span>                                                                                  | <span data-ttu-id="6651c-115">Description</span><span class="sxs-lookup"><span data-stu-id="6651c-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="6651c-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6651c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6651c-117">成功。</span><span class="sxs-lookup"><span data-stu-id="6651c-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="6651c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6651c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6651c-119">不支援指定的格式。</span><span class="sxs-lookup"><span data-stu-id="6651c-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="6651c-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6651c-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="6651c-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="6651c-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="6651c-122">備註</span><span class="sxs-lookup"><span data-stu-id="6651c-122">Remarks</span></span>

<span data-ttu-id="6651c-123">基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="6651c-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="6651c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6651c-124">Requirements</span></span>



| <span data-ttu-id="6651c-125">需求</span><span class="sxs-lookup"><span data-stu-id="6651c-125">Requirement</span></span> | <span data-ttu-id="6651c-126">值</span><span class="sxs-lookup"><span data-stu-id="6651c-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6651c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6651c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6651c-128"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6651c-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6651c-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="6651c-129">Library</span></span><br/> | <dl> <span data-ttu-id="6651c-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6651c-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6651c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6651c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6651c-132">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="6651c-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




