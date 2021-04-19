---
description: Get \_ AvgFrameRate 方法會計算並取得平均畫面播放速率。
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: 'CBaseVideoRenderer.get_AvgFrameRate 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991337"
---
# <a name="cbasevideorendererget_avgframerate-method"></a><span data-ttu-id="64d97-103">CBaseVideoRenderer. 取得 \_ AvgFrameRate 方法</span><span class="sxs-lookup"><span data-stu-id="64d97-103">CBaseVideoRenderer.get\_AvgFrameRate method</span></span>

<span data-ttu-id="64d97-104">`get_AvgFrameRate`方法會計算並取得平均畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="64d97-104">The `get_AvgFrameRate` method calculates and retrieves the average frame rate achieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d97-105">語法</span><span class="sxs-lookup"><span data-stu-id="64d97-105">Syntax</span></span>


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a><span data-ttu-id="64d97-106">參數</span><span class="sxs-lookup"><span data-stu-id="64d97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d97-107">*piAvgFrameRate*</span><span class="sxs-lookup"><span data-stu-id="64d97-107">*piAvgFrameRate*</span></span> 
</dt> <dd>

<span data-ttu-id="64d97-108">串流開始之後每秒的畫面格數指標。</span><span class="sxs-lookup"><span data-stu-id="64d97-108">Pointer to the number of frames per second since streaming began.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d97-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="64d97-109">Return value</span></span>

<span data-ttu-id="64d97-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="64d97-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d97-111">備註</span><span class="sxs-lookup"><span data-stu-id="64d97-111">Remarks</span></span>

<span data-ttu-id="64d97-112">此成員函式會實 [**IQualProp：： get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) 方法。</span><span class="sxs-lookup"><span data-stu-id="64d97-112">This member function implements the [**IQualProp::get\_AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d97-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="64d97-113">Requirements</span></span>



| <span data-ttu-id="64d97-114">需求</span><span class="sxs-lookup"><span data-stu-id="64d97-114">Requirement</span></span> | <span data-ttu-id="64d97-115">值</span><span class="sxs-lookup"><span data-stu-id="64d97-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d97-116">標頭</span><span class="sxs-lookup"><span data-stu-id="64d97-116">Header</span></span><br/>  | <dl> <span data-ttu-id="64d97-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="64d97-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="64d97-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="64d97-118">Library</span></span><br/> | <dl> <span data-ttu-id="64d97-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="64d97-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d97-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64d97-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d97-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="64d97-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




