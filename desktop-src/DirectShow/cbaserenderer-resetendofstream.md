---
description: ResetEndOfStream 方法會重設資料流程結尾旗標。
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: 'CBaseRenderer. ResetEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991356"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="8d87e-103">CBaseRenderer. ResetEndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="8d87e-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="8d87e-104">`ResetEndOfStream`方法會重設資料流程結尾旗標。</span><span class="sxs-lookup"><span data-stu-id="8d87e-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d87e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8d87e-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="8d87e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8d87e-106">Parameters</span></span>

<span data-ttu-id="8d87e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8d87e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d87e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d87e-108">Return value</span></span>

<span data-ttu-id="8d87e-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8d87e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d87e-110">備註</span><span class="sxs-lookup"><span data-stu-id="8d87e-110">Remarks</span></span>

<span data-ttu-id="8d87e-111">這個方法會清除先前的資料流程結束條件。</span><span class="sxs-lookup"><span data-stu-id="8d87e-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="8d87e-112">屆時，篩選器可以接收新的資料。</span><span class="sxs-lookup"><span data-stu-id="8d87e-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="8d87e-113">[**CBaseRenderer：： Stop**](cbaserenderer-stop.md)和 [**CBaseRenderer：： BeginFlush**](cbaserenderer-beginflush.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8d87e-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d87e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d87e-114">Requirements</span></span>



| <span data-ttu-id="8d87e-115">需求</span><span class="sxs-lookup"><span data-stu-id="8d87e-115">Requirement</span></span> | <span data-ttu-id="8d87e-116">值</span><span class="sxs-lookup"><span data-stu-id="8d87e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d87e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8d87e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8d87e-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8d87e-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d87e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d87e-119">Library</span></span><br/> | <dl> <span data-ttu-id="8d87e-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8d87e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d87e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d87e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d87e-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="8d87e-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




