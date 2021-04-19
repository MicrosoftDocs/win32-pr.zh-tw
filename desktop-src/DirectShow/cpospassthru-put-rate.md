---
description: Put \_ rate 方法會設定播放速率。 這個方法會實 IMediaPosition：:p 的等比 \_ 特率方法。
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: 'CPosPassThru.put_Rate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991517"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="23c21-104">CPosPassThru，put \_ Rate 方法</span><span class="sxs-lookup"><span data-stu-id="23c21-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="23c21-105">`put_Rate`方法會設定播放速率。</span><span class="sxs-lookup"><span data-stu-id="23c21-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="23c21-106">這個方法會實 [**IMediaPosition：:p 的 \_**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) 等位元速率方法。</span><span class="sxs-lookup"><span data-stu-id="23c21-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c21-107">語法</span><span class="sxs-lookup"><span data-stu-id="23c21-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="23c21-108">參數</span><span class="sxs-lookup"><span data-stu-id="23c21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c21-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="23c21-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="23c21-110">播放速率。</span><span class="sxs-lookup"><span data-stu-id="23c21-110">Playback rate.</span></span> <span data-ttu-id="23c21-111">不得為零。</span><span class="sxs-lookup"><span data-stu-id="23c21-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c21-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="23c21-112">Return value</span></span>

<span data-ttu-id="23c21-113">\_如果 *dRate* 為零，則傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="23c21-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="23c21-114">否則，會從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="23c21-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c21-115">備註</span><span class="sxs-lookup"><span data-stu-id="23c21-115">Remarks</span></span>

<span data-ttu-id="23c21-116">負比率表示反向播放。</span><span class="sxs-lookup"><span data-stu-id="23c21-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="23c21-117">並非所有媒體都支援反向播放。</span><span class="sxs-lookup"><span data-stu-id="23c21-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="23c21-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="23c21-118">Requirements</span></span>



| <span data-ttu-id="23c21-119">需求</span><span class="sxs-lookup"><span data-stu-id="23c21-119">Requirement</span></span> | <span data-ttu-id="23c21-120">值</span><span class="sxs-lookup"><span data-stu-id="23c21-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c21-121">標頭</span><span class="sxs-lookup"><span data-stu-id="23c21-121">Header</span></span><br/>  | <dl> <span data-ttu-id="23c21-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="23c21-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23c21-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="23c21-123">Library</span></span><br/> | <dl> <span data-ttu-id="23c21-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="23c21-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c21-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23c21-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c21-126">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="23c21-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




