---
description: SetRate 方法會設定播放速率。 這個方法會實 IMediaSeeking：： SetRate 方法。
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: 'CPosPassThru. SetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977538"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="230e8-104">CPosPassThru. SetRate 方法</span><span class="sxs-lookup"><span data-stu-id="230e8-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="230e8-105">`SetRate`方法會設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="230e8-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="230e8-106">這個方法會實 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="230e8-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="230e8-107">語法</span><span class="sxs-lookup"><span data-stu-id="230e8-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="230e8-108">參數</span><span class="sxs-lookup"><span data-stu-id="230e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="230e8-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="230e8-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="230e8-110">播放速率。</span><span class="sxs-lookup"><span data-stu-id="230e8-110">Playback rate.</span></span> <span data-ttu-id="230e8-111">不得為零。</span><span class="sxs-lookup"><span data-stu-id="230e8-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="230e8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="230e8-112">Return value</span></span>

<span data-ttu-id="230e8-113">\_如果 *dRate* 為零，則傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="230e8-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="230e8-114">否則，會從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="230e8-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="230e8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="230e8-115">Requirements</span></span>



| <span data-ttu-id="230e8-116">需求</span><span class="sxs-lookup"><span data-stu-id="230e8-116">Requirement</span></span> | <span data-ttu-id="230e8-117">值</span><span class="sxs-lookup"><span data-stu-id="230e8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="230e8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="230e8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="230e8-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="230e8-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="230e8-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="230e8-120">Library</span></span><br/> | <dl> <span data-ttu-id="230e8-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="230e8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230e8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="230e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230e8-123">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="230e8-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




