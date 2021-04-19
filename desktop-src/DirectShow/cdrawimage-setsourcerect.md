---
description: SetSourceRect 方法會設定來源矩形。
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: 'CDrawImage. SetSourceRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990517"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="e3f10-103">CDrawImage. SetSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="e3f10-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="e3f10-104">`SetSourceRect`方法會設定來源矩形。</span><span class="sxs-lookup"><span data-stu-id="e3f10-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f10-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3f10-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="e3f10-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3f10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f10-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="e3f10-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="e3f10-108">**矩形** 結構的指標，此結構會定義新的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="e3f10-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f10-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3f10-109">Return value</span></span>

<span data-ttu-id="e3f10-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e3f10-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f10-111">備註</span><span class="sxs-lookup"><span data-stu-id="e3f10-111">Remarks</span></span>

<span data-ttu-id="e3f10-112">如果來源矩形變更，則擁有篩選應呼叫這個方法。例如，回應 [**IBasicVideo：： SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3f10-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="e3f10-113">在呼叫這個方法之前，請先驗證 *pSourceRect* 中指定的矩形，以確定它不會延伸到原生影片大小之外。</span><span class="sxs-lookup"><span data-stu-id="e3f10-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f10-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3f10-114">Requirements</span></span>



| <span data-ttu-id="e3f10-115">需求</span><span class="sxs-lookup"><span data-stu-id="e3f10-115">Requirement</span></span> | <span data-ttu-id="e3f10-116">值</span><span class="sxs-lookup"><span data-stu-id="e3f10-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f10-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e3f10-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3f10-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e3f10-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3f10-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3f10-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3f10-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e3f10-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f10-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3f10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f10-122">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="e3f10-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




