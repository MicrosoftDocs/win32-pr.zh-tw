---
description: IsFormatSupported 方法會判斷是否支援指定的時間格式。 這個方法會實 IMediaSeeking：： IsFormatSupported 方法。
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: 'CSourceSeeking. IsFormatSupported 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987183"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="c04d6-104">CSourceSeeking. IsFormatSupported 方法</span><span class="sxs-lookup"><span data-stu-id="c04d6-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="c04d6-105">`IsFormatSupported`方法會判斷是否支援指定的時間格式。</span><span class="sxs-lookup"><span data-stu-id="c04d6-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="c04d6-106">這個方法會實 [**IMediaSeeking：： IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) 方法。</span><span class="sxs-lookup"><span data-stu-id="c04d6-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04d6-107">語法</span><span class="sxs-lookup"><span data-stu-id="c04d6-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c04d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="c04d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04d6-109">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="c04d6-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c04d6-110">時間格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="c04d6-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="c04d6-111">請參閱 [**時間格式 guid**](time-format-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="c04d6-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c04d6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c04d6-112">Return value</span></span>

<span data-ttu-id="c04d6-113">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c04d6-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="c04d6-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c04d6-114">Return code</span></span>                                                                               | <span data-ttu-id="c04d6-115">Description</span><span class="sxs-lookup"><span data-stu-id="c04d6-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c04d6-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c04d6-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="c04d6-117">不支援此格式。</span><span class="sxs-lookup"><span data-stu-id="c04d6-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="c04d6-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c04d6-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c04d6-119">支援此格式。</span><span class="sxs-lookup"><span data-stu-id="c04d6-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="c04d6-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c04d6-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c04d6-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="c04d6-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="c04d6-122">備註</span><span class="sxs-lookup"><span data-stu-id="c04d6-122">Remarks</span></span>

<span data-ttu-id="c04d6-123">基類所支援的唯一時間格式是時間 \_ 格式 \_ 媒體 \_ 時間 (100-毫微秒單位) 。</span><span class="sxs-lookup"><span data-stu-id="c04d6-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="c04d6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c04d6-124">Requirements</span></span>



| <span data-ttu-id="c04d6-125">需求</span><span class="sxs-lookup"><span data-stu-id="c04d6-125">Requirement</span></span> | <span data-ttu-id="c04d6-126">值</span><span class="sxs-lookup"><span data-stu-id="c04d6-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c04d6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c04d6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c04d6-128"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c04d6-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c04d6-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="c04d6-129">Library</span></span><br/> | <dl> <span data-ttu-id="c04d6-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c04d6-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04d6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c04d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04d6-132">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="c04d6-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




