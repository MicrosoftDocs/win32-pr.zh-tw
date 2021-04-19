---
description: Pause 方法會暫停篩選。 這個方法會實 IMediaFilter：:P ause 方法。
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: 'CTransformFilter： Pause 方法 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5408b9a39f92fd68eacb83474a18da0acda6b961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996002"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="68bd1-104">CTransformFilter. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="68bd1-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="68bd1-105">`Pause`方法會暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="68bd1-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="68bd1-106">這個方法會實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。</span><span class="sxs-lookup"><span data-stu-id="68bd1-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68bd1-107">語法</span><span class="sxs-lookup"><span data-stu-id="68bd1-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="68bd1-108">參數</span><span class="sxs-lookup"><span data-stu-id="68bd1-108">Parameters</span></span>

<span data-ttu-id="68bd1-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="68bd1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68bd1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="68bd1-110">Return value</span></span>

<span data-ttu-id="68bd1-111">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="68bd1-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68bd1-112">備註</span><span class="sxs-lookup"><span data-stu-id="68bd1-112">Remarks</span></span>

<span data-ttu-id="68bd1-113">這個方法會呼叫 [**StartStreaming**](ctransformfilter-startstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="68bd1-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="68bd1-114">**StartStreaming** 方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="68bd1-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="68bd1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="68bd1-115">Requirements</span></span>



| <span data-ttu-id="68bd1-116">需求</span><span class="sxs-lookup"><span data-stu-id="68bd1-116">Requirement</span></span> | <span data-ttu-id="68bd1-117">值</span><span class="sxs-lookup"><span data-stu-id="68bd1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68bd1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="68bd1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68bd1-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68bd1-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="68bd1-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="68bd1-120">Library</span></span><br/> | <dl> <span data-ttu-id="68bd1-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="68bd1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68bd1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68bd1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bd1-123">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="68bd1-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




