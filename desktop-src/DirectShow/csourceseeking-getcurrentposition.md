---
description: GetCurrentPosition 方法會抓取目前的位置，相對於資料流程的總持續時間。 未實作。
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: 'CSourceSeeking. GetCurrentPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989663"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="b6519-104">CSourceSeeking. GetCurrentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="b6519-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="b6519-105">方法會抓取 `GetCurrentPosition` 目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="b6519-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="b6519-106">未實作。</span><span class="sxs-lookup"><span data-stu-id="b6519-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6519-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6519-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="b6519-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6519-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6519-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="b6519-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="b6519-110">變數的指標，此變數會接收目前的位置，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="b6519-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6519-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6519-111">Return value</span></span>

<span data-ttu-id="b6519-112">傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="b6519-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6519-113">備註</span><span class="sxs-lookup"><span data-stu-id="b6519-113">Remarks</span></span>

<span data-ttu-id="b6519-114">來源篩選準則通常不支援此方法。</span><span class="sxs-lookup"><span data-stu-id="b6519-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="b6519-115">相反地，轉譯器篩選會透過 [**CRendererPosPassThru**](crendererpospassthru.md) 類別來報告目前的位置。</span><span class="sxs-lookup"><span data-stu-id="b6519-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6519-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6519-116">Requirements</span></span>



| <span data-ttu-id="b6519-117">需求</span><span class="sxs-lookup"><span data-stu-id="b6519-117">Requirement</span></span> | <span data-ttu-id="b6519-118">值</span><span class="sxs-lookup"><span data-stu-id="b6519-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6519-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b6519-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b6519-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b6519-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6519-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6519-121">Library</span></span><br/> | <dl> <span data-ttu-id="b6519-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b6519-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6519-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6519-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6519-124">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="b6519-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




