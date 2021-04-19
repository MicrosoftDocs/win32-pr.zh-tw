---
description: GetRate 方法會捕獲播放速率。 這個方法會實 IMediaSeeking：： GetRate 方法。
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: 'CPosPassThru. GetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998725"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="46ca3-104">CPosPassThru. GetRate 方法</span><span class="sxs-lookup"><span data-stu-id="46ca3-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="46ca3-105">`GetRate`方法會捕獲播放速率。</span><span class="sxs-lookup"><span data-stu-id="46ca3-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="46ca3-106">這個方法會實 [**IMediaSeeking：： GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="46ca3-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ca3-107">語法</span><span class="sxs-lookup"><span data-stu-id="46ca3-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="46ca3-108">參數</span><span class="sxs-lookup"><span data-stu-id="46ca3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ca3-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="46ca3-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="46ca3-110">接收播放速率之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="46ca3-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ca3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="46ca3-111">Return value</span></span>

<span data-ttu-id="46ca3-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="46ca3-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ca3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="46ca3-113">Requirements</span></span>



| <span data-ttu-id="46ca3-114">需求</span><span class="sxs-lookup"><span data-stu-id="46ca3-114">Requirement</span></span> | <span data-ttu-id="46ca3-115">值</span><span class="sxs-lookup"><span data-stu-id="46ca3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ca3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="46ca3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="46ca3-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="46ca3-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46ca3-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="46ca3-118">Library</span></span><br/> | <dl> <span data-ttu-id="46ca3-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="46ca3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ca3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46ca3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ca3-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="46ca3-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




