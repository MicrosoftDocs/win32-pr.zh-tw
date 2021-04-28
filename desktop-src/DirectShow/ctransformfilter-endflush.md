---
description: CTransformFilter. EndFlush 方法-EndFlush 方法會結束清除作業。
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: 'CTransformFilter. EndFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085057"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="7074e-103">CTransformFilter. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="7074e-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="7074e-104">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="7074e-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7074e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7074e-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="7074e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7074e-106">Parameters</span></span>

<span data-ttu-id="7074e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7074e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7074e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7074e-108">Return value</span></span>

<span data-ttu-id="7074e-109">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7074e-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7074e-110">備註</span><span class="sxs-lookup"><span data-stu-id="7074e-110">Remarks</span></span>

<span data-ttu-id="7074e-111">在清除作業結束時，輸入釘選的 [**CTransformInputPin：： EndFlush**](ctransforminputpin-endflush.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7074e-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="7074e-112">這個方法會將 `EndFlush` 呼叫傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="7074e-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="7074e-113">如果衍生類別使用背景工作執行緒來傳遞範例，則必須先捨棄所有已排入佇列的資料，然後再傳送 `EndFlush` 呼叫下游。</span><span class="sxs-lookup"><span data-stu-id="7074e-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="7074e-114">如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="7074e-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7074e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7074e-115">Requirements</span></span>



| <span data-ttu-id="7074e-116">需求</span><span class="sxs-lookup"><span data-stu-id="7074e-116">Requirement</span></span> | <span data-ttu-id="7074e-117">值</span><span class="sxs-lookup"><span data-stu-id="7074e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7074e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7074e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7074e-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7074e-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7074e-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="7074e-120">Library</span></span><br/> | <dl> <span data-ttu-id="7074e-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7074e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7074e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7074e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7074e-123">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="7074e-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




