---
description: 非使用中的方法會通知 pin，篩選已不再有效。
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: 'CBasePin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978767"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="3638f-103">CBasePin 方法</span><span class="sxs-lookup"><span data-stu-id="3638f-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="3638f-104">`Inactive`方法會通知 pin，篩選已不再有效。</span><span class="sxs-lookup"><span data-stu-id="3638f-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="3638f-105">語法</span><span class="sxs-lookup"><span data-stu-id="3638f-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="3638f-106">參數</span><span class="sxs-lookup"><span data-stu-id="3638f-106">Parameters</span></span>

<span data-ttu-id="3638f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3638f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3638f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3638f-108">Return value</span></span>

<span data-ttu-id="3638f-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3638f-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3638f-110">備註</span><span class="sxs-lookup"><span data-stu-id="3638f-110">Remarks</span></span>

<span data-ttu-id="3638f-111">當篩選準則停止時， [**CBaseFilter**](cbasefilter.md) 類別會在所有篩選連接的釘選上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3638f-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="3638f-112">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="3638f-112">This method does nothing in the base class.</span></span> <span data-ttu-id="3638f-113">衍生類別應該覆寫這個方法，以釋放 [**CBasePin：： Active**](cbasepin-active.md) 方法所取得的任何資源;例如，取消認可釘選的配置器。</span><span class="sxs-lookup"><span data-stu-id="3638f-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="3638f-114">在這個方法傳回之前，不會更新篩選圖形管理員的內部狀態，因此請勿從此方法測試狀態。</span><span class="sxs-lookup"><span data-stu-id="3638f-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3638f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3638f-115">Requirements</span></span>



| <span data-ttu-id="3638f-116">需求</span><span class="sxs-lookup"><span data-stu-id="3638f-116">Requirement</span></span> | <span data-ttu-id="3638f-117">值</span><span class="sxs-lookup"><span data-stu-id="3638f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3638f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3638f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3638f-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3638f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3638f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="3638f-120">Library</span></span><br/> | <dl> <span data-ttu-id="3638f-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3638f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3638f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3638f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3638f-123">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="3638f-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




