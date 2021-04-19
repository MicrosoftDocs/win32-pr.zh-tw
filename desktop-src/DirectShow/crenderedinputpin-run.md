---
description: Run 方法會通知釘選篩選現在正在執行。 這個方法會覆寫 CBasePin：： Run 方法。
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: 'CRenderedInputPin： Run 方法 (Amextra) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987152"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="f47ff-104">CRenderedInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="f47ff-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="f47ff-105">`Run`方法會通知釘選篩選現在正在執行。</span><span class="sxs-lookup"><span data-stu-id="f47ff-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="f47ff-106">這個方法會覆寫 [**CBasePin：： Run**](cbasepin-run.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f47ff-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f47ff-107">語法</span><span class="sxs-lookup"><span data-stu-id="f47ff-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="f47ff-108">參數</span><span class="sxs-lookup"><span data-stu-id="f47ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47ff-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="f47ff-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f47ff-110">傳遞至篩選器 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f47ff-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47ff-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f47ff-111">Return value</span></span>

<span data-ttu-id="f47ff-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f47ff-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="f47ff-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f47ff-113">Requirements</span></span>



| <span data-ttu-id="f47ff-114">需求</span><span class="sxs-lookup"><span data-stu-id="f47ff-114">Requirement</span></span> | <span data-ttu-id="f47ff-115">值</span><span class="sxs-lookup"><span data-stu-id="f47ff-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f47ff-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f47ff-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f47ff-117"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f47ff-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f47ff-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f47ff-118">Library</span></span><br/> | <dl> <span data-ttu-id="f47ff-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f47ff-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f47ff-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f47ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47ff-121">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="f47ff-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




