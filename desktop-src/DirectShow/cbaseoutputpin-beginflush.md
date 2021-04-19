---
description: BeginFlush 方法會開始進行清除作業。 實行 IPin：： BeginFlush 方法。
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: 'CBaseOutputPin. BeginFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992973"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="18ea3-104">CBaseOutputPin. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="18ea3-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="18ea3-105">`BeginFlush`方法會開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="18ea3-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="18ea3-106">實行 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="18ea3-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ea3-107">語法</span><span class="sxs-lookup"><span data-stu-id="18ea3-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="18ea3-108">參數</span><span class="sxs-lookup"><span data-stu-id="18ea3-108">Parameters</span></span>

<span data-ttu-id="18ea3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="18ea3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18ea3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="18ea3-110">Return value</span></span>

<span data-ttu-id="18ea3-111">傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="18ea3-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ea3-112">備註</span><span class="sxs-lookup"><span data-stu-id="18ea3-112">Remarks</span></span>

<span data-ttu-id="18ea3-113">這個方法應該只在輸入圖釘上呼叫，因此 **CBaseOutputPin** 的執行會傳回非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="18ea3-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ea3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="18ea3-114">Requirements</span></span>



| <span data-ttu-id="18ea3-115">需求</span><span class="sxs-lookup"><span data-stu-id="18ea3-115">Requirement</span></span> | <span data-ttu-id="18ea3-116">值</span><span class="sxs-lookup"><span data-stu-id="18ea3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ea3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="18ea3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="18ea3-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="18ea3-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="18ea3-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="18ea3-119">Library</span></span><br/> | <dl> <span data-ttu-id="18ea3-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="18ea3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ea3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18ea3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ea3-122">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="18ea3-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




