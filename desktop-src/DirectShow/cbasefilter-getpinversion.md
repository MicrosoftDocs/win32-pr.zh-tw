---
description: GetPinVersion 方法會在此篩選器上抓取一組釘選的版本號碼。
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: 'CBaseFilter. GetPinVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995033"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="fbb84-103">CBaseFilter. GetPinVersion 方法</span><span class="sxs-lookup"><span data-stu-id="fbb84-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="fbb84-104">`GetPinVersion`方法會在此篩選器上抓取一組釘選的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="fbb84-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb84-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbb84-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="fbb84-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbb84-106">Parameters</span></span>

<span data-ttu-id="fbb84-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fbb84-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbb84-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb84-108">Return value</span></span>

<span data-ttu-id="fbb84-109">傳回 [**CBaseFilter：： m \_ PinVersion**](cbasefilter-m-pinversion.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="fbb84-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb84-110">備註</span><span class="sxs-lookup"><span data-stu-id="fbb84-110">Remarks</span></span>

<span data-ttu-id="fbb84-111">**CBaseFilter** 函式會將 pin 版本初始化為1。</span><span class="sxs-lookup"><span data-stu-id="fbb84-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="fbb84-112">在基類中，此數位永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="fbb84-112">In the base class, this number never changes.</span></span> <span data-ttu-id="fbb84-113">如果篩選動態建立或終結 pin，則每當 pin 變更時，就應該遞增 pin 版本。</span><span class="sxs-lookup"><span data-stu-id="fbb84-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="fbb84-114">若要遞增版本號碼，請呼叫 [**CBaseFilter：： IncrementPinVersion**](cbasefilter-incrementpinversion.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="fbb84-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="fbb84-115">Pin 列舉值物件是由 [**CEnumPins**](cenumpins.md) 類別所執行，它會使用 pin 版本將本身與篩選準則保持同步。</span><span class="sxs-lookup"><span data-stu-id="fbb84-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb84-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb84-116">Requirements</span></span>



| <span data-ttu-id="fbb84-117">需求</span><span class="sxs-lookup"><span data-stu-id="fbb84-117">Requirement</span></span> | <span data-ttu-id="fbb84-118">值</span><span class="sxs-lookup"><span data-stu-id="fbb84-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb84-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fbb84-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fbb84-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fbb84-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fbb84-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="fbb84-121">Library</span></span><br/> | <dl> <span data-ttu-id="fbb84-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fbb84-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb84-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbb84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb84-124">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="fbb84-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




