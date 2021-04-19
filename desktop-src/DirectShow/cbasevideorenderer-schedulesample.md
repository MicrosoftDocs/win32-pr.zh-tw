---
description: ScheduleSample 方法會覆寫執行主要工作的基類，以保留 IQualProp 實) 所使用 (所繪製樣本的計數。
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: 'CBaseVideoRenderer. ScheduleSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995628"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="61e38-103">CBaseVideoRenderer. ScheduleSample 方法</span><span class="sxs-lookup"><span data-stu-id="61e38-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="61e38-104">`ScheduleSample`方法會覆寫執行主要工作的基類，以保留 [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)實) 所使用 (所繪製樣本的計數。</span><span class="sxs-lookup"><span data-stu-id="61e38-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="61e38-105">語法</span><span class="sxs-lookup"><span data-stu-id="61e38-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="61e38-106">參數</span><span class="sxs-lookup"><span data-stu-id="61e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e38-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="61e38-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="61e38-108">媒體範例的指標。</span><span class="sxs-lookup"><span data-stu-id="61e38-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61e38-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="61e38-109">Return value</span></span>

<span data-ttu-id="61e38-110">如果已排程範例，則傳回 **TRUE** ;否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="61e38-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="61e38-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="61e38-111">Requirements</span></span>



| <span data-ttu-id="61e38-112">需求</span><span class="sxs-lookup"><span data-stu-id="61e38-112">Requirement</span></span> | <span data-ttu-id="61e38-113">值</span><span class="sxs-lookup"><span data-stu-id="61e38-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e38-114">標頭</span><span class="sxs-lookup"><span data-stu-id="61e38-114">Header</span></span><br/>  | <dl> <span data-ttu-id="61e38-115"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="61e38-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61e38-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="61e38-116">Library</span></span><br/> | <dl> <span data-ttu-id="61e38-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="61e38-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61e38-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61e38-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e38-119">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="61e38-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




