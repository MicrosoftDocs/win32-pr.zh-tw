---
description: QueryPreferredFormat 方法會抓取物件的慣用時間格式。 這個方法會實 IMediaSeeking：： QueryPreferredFormat 方法。
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: 'CSourceSeeking. QueryPreferredFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993359"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="21134-104">CSourceSeeking. QueryPreferredFormat 方法</span><span class="sxs-lookup"><span data-stu-id="21134-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="21134-105">方法會抓取 `QueryPreferredFormat` 物件的慣用時間格式。</span><span class="sxs-lookup"><span data-stu-id="21134-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="21134-106">這個方法會實 [**IMediaSeeking：： QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="21134-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="21134-107">語法</span><span class="sxs-lookup"><span data-stu-id="21134-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="21134-108">參數</span><span class="sxs-lookup"><span data-stu-id="21134-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21134-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="21134-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="21134-110">接收時間格式 GUID 之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="21134-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="21134-111">請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="21134-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21134-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="21134-112">Return value</span></span>

<span data-ttu-id="21134-113">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="21134-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="21134-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="21134-114">Return code</span></span>                                                                               | <span data-ttu-id="21134-115">Description</span><span class="sxs-lookup"><span data-stu-id="21134-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="21134-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="21134-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="21134-117">Success</span><span class="sxs-lookup"><span data-stu-id="21134-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="21134-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="21134-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="21134-119">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="21134-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21134-120">備註</span><span class="sxs-lookup"><span data-stu-id="21134-120">Remarks</span></span>

<span data-ttu-id="21134-121">基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="21134-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="21134-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="21134-122">Requirements</span></span>



| <span data-ttu-id="21134-123">需求</span><span class="sxs-lookup"><span data-stu-id="21134-123">Requirement</span></span> | <span data-ttu-id="21134-124">值</span><span class="sxs-lookup"><span data-stu-id="21134-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21134-125">標頭</span><span class="sxs-lookup"><span data-stu-id="21134-125">Header</span></span><br/>  | <dl> <span data-ttu-id="21134-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="21134-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21134-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="21134-127">Library</span></span><br/> | <dl> <span data-ttu-id="21134-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="21134-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21134-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21134-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21134-130">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="21134-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




