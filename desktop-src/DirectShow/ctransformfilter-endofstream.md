---
description: EndOfStream 方法會向篩選發出通知，指出輸入 pin 不需要任何其他資料。
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: 'CTransformFilter. EndOfStream 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982996"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="b08c6-103">CTransformFilter. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="b08c6-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="b08c6-104">`EndOfStream`方法會向篩選通知，輸入 pin 不需要任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="b08c6-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b08c6-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="b08c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="b08c6-106">Parameters</span></span>

<span data-ttu-id="b08c6-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b08c6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b08c6-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b08c6-108">Return value</span></span>

<span data-ttu-id="b08c6-109">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b08c6-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b08c6-110">備註</span><span class="sxs-lookup"><span data-stu-id="b08c6-110">Remarks</span></span>

<span data-ttu-id="b08c6-111">輸入釘選的 [**CTransformInputPin：： EndOfStream**](ctransforminputpin-endofstream.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b08c6-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="b08c6-112">這個方法會傳遞下游的資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="b08c6-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="b08c6-113">如果衍生類別使用背景工作執行緒來傳遞媒體範例，則應該覆寫這個方法，並將資料流程結束通知排入佇列。</span><span class="sxs-lookup"><span data-stu-id="b08c6-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="b08c6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b08c6-114">Requirements</span></span>



| <span data-ttu-id="b08c6-115">需求</span><span class="sxs-lookup"><span data-stu-id="b08c6-115">Requirement</span></span> | <span data-ttu-id="b08c6-116">值</span><span class="sxs-lookup"><span data-stu-id="b08c6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08c6-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b08c6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b08c6-118"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b08c6-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b08c6-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b08c6-119">Library</span></span><br/> | <dl> <span data-ttu-id="b08c6-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b08c6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b08c6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b08c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08c6-122">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="b08c6-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




