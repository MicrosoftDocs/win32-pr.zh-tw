---
description: 非使用中的方法會關閉從輸出釘選資料的背景工作執行緒。 這個方法也會解除配置器。
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: 'CPullPin：非使用中方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990749"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="8fb27-104">CPullPin 方法</span><span class="sxs-lookup"><span data-stu-id="8fb27-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="8fb27-105">`Inactive`方法會關閉從輸出圖釘提取資料的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="8fb27-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="8fb27-106">這個方法也會解除配置器。</span><span class="sxs-lookup"><span data-stu-id="8fb27-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb27-107">語法</span><span class="sxs-lookup"><span data-stu-id="8fb27-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="8fb27-108">參數</span><span class="sxs-lookup"><span data-stu-id="8fb27-108">Parameters</span></span>

<span data-ttu-id="8fb27-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8fb27-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fb27-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fb27-110">Return value</span></span>

<span data-ttu-id="8fb27-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8fb27-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb27-112">備註</span><span class="sxs-lookup"><span data-stu-id="8fb27-112">Remarks</span></span>

<span data-ttu-id="8fb27-113">當擁有篩選變成非使用中時，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8fb27-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="8fb27-114"> (如果您的輸入 pin 衍生自 [**CBasePin**](cbasepin.md)，請覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。 ) </span><span class="sxs-lookup"><span data-stu-id="8fb27-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb27-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fb27-115">Requirements</span></span>



| <span data-ttu-id="8fb27-116">需求</span><span class="sxs-lookup"><span data-stu-id="8fb27-116">Requirement</span></span> | <span data-ttu-id="8fb27-117">值</span><span class="sxs-lookup"><span data-stu-id="8fb27-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb27-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8fb27-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8fb27-119"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb27-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="8fb27-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="8fb27-120">Library</span></span><br/> | <dl> <span data-ttu-id="8fb27-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8fb27-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb27-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fb27-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb27-123">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="8fb27-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




