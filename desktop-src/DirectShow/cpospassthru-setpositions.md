---
description: SetPositions 方法會設定目前的位置和停止位置。 這個方法會實 IMediaSeeking：： SetPositions 方法。
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: 'CPosPassThru. SetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991237"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="49430-104">CPosPassThru. SetPositions 方法</span><span class="sxs-lookup"><span data-stu-id="49430-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="49430-105">`SetPositions`方法會設定目前的位置和停止位置。</span><span class="sxs-lookup"><span data-stu-id="49430-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="49430-106">這個方法會實 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法。</span><span class="sxs-lookup"><span data-stu-id="49430-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49430-107">語法</span><span class="sxs-lookup"><span data-stu-id="49430-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="49430-108">參數</span><span class="sxs-lookup"><span data-stu-id="49430-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49430-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="49430-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="49430-110">變數的指標，該變數會指定目前的位置，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="49430-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="49430-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="49430-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="49430-112">旗標的位組合。</span><span class="sxs-lookup"><span data-stu-id="49430-112">Bitwise combination of flags.</span></span> <span data-ttu-id="49430-113">如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 。</span><span class="sxs-lookup"><span data-stu-id="49430-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="49430-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="49430-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="49430-115">指定停止時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="49430-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="49430-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="49430-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="49430-117">旗標的位組合。</span><span class="sxs-lookup"><span data-stu-id="49430-117">Bitwise combination of flags.</span></span> <span data-ttu-id="49430-118">如需詳細資訊，請參閱 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 。</span><span class="sxs-lookup"><span data-stu-id="49430-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49430-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="49430-119">Return value</span></span>

<span data-ttu-id="49430-120">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="49430-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="49430-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="49430-121">Requirements</span></span>



| <span data-ttu-id="49430-122">需求</span><span class="sxs-lookup"><span data-stu-id="49430-122">Requirement</span></span> | <span data-ttu-id="49430-123">值</span><span class="sxs-lookup"><span data-stu-id="49430-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49430-124">標頭</span><span class="sxs-lookup"><span data-stu-id="49430-124">Header</span></span><br/>  | <dl> <span data-ttu-id="49430-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="49430-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49430-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="49430-126">Library</span></span><br/> | <dl> <span data-ttu-id="49430-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="49430-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49430-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49430-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49430-129">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="49430-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




