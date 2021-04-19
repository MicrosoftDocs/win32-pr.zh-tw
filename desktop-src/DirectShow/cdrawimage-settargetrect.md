---
description: SetTargetRect 方法會設定目標矩形。
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: 'CDrawImage. SetTargetRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000774"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="0f698-103">CDrawImage. SetTargetRect 方法</span><span class="sxs-lookup"><span data-stu-id="0f698-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="0f698-104">`SetTargetRect`方法會設定目標矩形。</span><span class="sxs-lookup"><span data-stu-id="0f698-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f698-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f698-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="0f698-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f698-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f698-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="0f698-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="0f698-108">**矩形** 結構的指標，此結構會定義新的目標矩形。</span><span class="sxs-lookup"><span data-stu-id="0f698-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f698-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f698-109">Return value</span></span>

<span data-ttu-id="0f698-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0f698-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f698-111">備註</span><span class="sxs-lookup"><span data-stu-id="0f698-111">Remarks</span></span>

<span data-ttu-id="0f698-112">如果來源矩形變更，則擁有篩選應呼叫這個方法。例如，回應 [**IBasicVideo：： SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f698-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="0f698-113">在呼叫這個方法之前，請先驗證 *pTargetRect*（相對於影片視窗）中所指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="0f698-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f698-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f698-114">Requirements</span></span>



| <span data-ttu-id="0f698-115">需求</span><span class="sxs-lookup"><span data-stu-id="0f698-115">Requirement</span></span> | <span data-ttu-id="0f698-116">值</span><span class="sxs-lookup"><span data-stu-id="0f698-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f698-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0f698-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f698-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0f698-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f698-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f698-119">Library</span></span><br/> | <dl> <span data-ttu-id="0f698-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0f698-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f698-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f698-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f698-122">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="0f698-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




