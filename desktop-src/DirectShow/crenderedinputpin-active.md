---
description: 使用中的方法會通知釘選篩選現在為使用中狀態。 這個方法會覆寫 CBasePin：： Active 方法。
ms.assetid: e98ca947-df2f-41a7-9785-b35bd1dde1e6
title: 'CRenderedInputPin 方法 (Amextra .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae56439f5e19aa5c039ac81bdd8a7aafe0f2174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000841"
---
# <a name="crenderedinputpinactive-method"></a><span data-ttu-id="9e257-104">CRenderedInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="9e257-104">CRenderedInputPin.Active method</span></span>

<span data-ttu-id="9e257-105">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="9e257-105">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="9e257-106">這個方法會覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9e257-106">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e257-107">語法</span><span class="sxs-lookup"><span data-stu-id="9e257-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="9e257-108">參數</span><span class="sxs-lookup"><span data-stu-id="9e257-108">Parameters</span></span>

<span data-ttu-id="9e257-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9e257-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e257-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e257-110">Return value</span></span>

<span data-ttu-id="9e257-111">\_如果成功，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9e257-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e257-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e257-112">Requirements</span></span>



| <span data-ttu-id="9e257-113">需求</span><span class="sxs-lookup"><span data-stu-id="9e257-113">Requirement</span></span> | <span data-ttu-id="9e257-114">值</span><span class="sxs-lookup"><span data-stu-id="9e257-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e257-115">標頭</span><span class="sxs-lookup"><span data-stu-id="9e257-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9e257-116"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9e257-116"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e257-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e257-117">Library</span></span><br/> | <dl> <span data-ttu-id="9e257-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9e257-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e257-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e257-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e257-120">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9e257-120">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




