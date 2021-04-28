---
description: CBasePin 方法-使用中的方法會通知釘選篩選現在為使用中狀態。
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: 'CBasePin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096105"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="39666-103">CBasePin 方法</span><span class="sxs-lookup"><span data-stu-id="39666-103">CBasePin.Active method</span></span>

<span data-ttu-id="39666-104">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="39666-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="39666-105">語法</span><span class="sxs-lookup"><span data-stu-id="39666-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="39666-106">參數</span><span class="sxs-lookup"><span data-stu-id="39666-106">Parameters</span></span>

<span data-ttu-id="39666-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="39666-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39666-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="39666-108">Return value</span></span>

<span data-ttu-id="39666-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="39666-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="39666-110">備註</span><span class="sxs-lookup"><span data-stu-id="39666-110">Remarks</span></span>

<span data-ttu-id="39666-111">當篩選準則從 [已停止] 變成 [已暫停] 時， [**CBaseFilter**](cbasefilter.md) 類別會在所有篩選連接的釘選上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="39666-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="39666-112">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="39666-112">This method does nothing in the base class.</span></span> <span data-ttu-id="39666-113">衍生類別可以覆寫這個方法;例如，pin 可能會認可配置器或取得硬體資源。</span><span class="sxs-lookup"><span data-stu-id="39666-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="39666-114">除非這個成員函式傳回，否則篩選圖形管理員的內部狀態不會更新，因此請勿從此方法測試狀態。</span><span class="sxs-lookup"><span data-stu-id="39666-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="39666-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="39666-115">Requirements</span></span>



| <span data-ttu-id="39666-116">需求</span><span class="sxs-lookup"><span data-stu-id="39666-116">Requirement</span></span> | <span data-ttu-id="39666-117">值</span><span class="sxs-lookup"><span data-stu-id="39666-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39666-118">標頭</span><span class="sxs-lookup"><span data-stu-id="39666-118">Header</span></span><br/>  | <dl> <span data-ttu-id="39666-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="39666-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39666-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="39666-120">Library</span></span><br/> | <dl> <span data-ttu-id="39666-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="39666-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39666-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39666-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39666-123">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="39666-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




