---
description: CTransformFilter： pause 方法： Pause 方法會暫停篩選。 這個方法會實 IMediaFilter：:P ause 方法。
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
ms.openlocfilehash: 903522b63754ff7972e4cdcf5221946442497896
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095096"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="2e6b2-104">CTransformFilter. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="2e6b2-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="2e6b2-105">`Pause`方法會暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="2e6b2-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="2e6b2-106">這個方法會實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。</span><span class="sxs-lookup"><span data-stu-id="2e6b2-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6b2-107">語法</span><span class="sxs-lookup"><span data-stu-id="2e6b2-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="2e6b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e6b2-108">Parameters</span></span>

<span data-ttu-id="2e6b2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2e6b2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e6b2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e6b2-110">Return value</span></span>

<span data-ttu-id="2e6b2-111">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2e6b2-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e6b2-112">備註</span><span class="sxs-lookup"><span data-stu-id="2e6b2-112">Remarks</span></span>

<span data-ttu-id="2e6b2-113">這個方法會呼叫 [**StartStreaming**](ctransformfilter-startstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2e6b2-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="2e6b2-114">**StartStreaming** 方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="2e6b2-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e6b2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e6b2-115">Requirements</span></span>



| <span data-ttu-id="2e6b2-116">需求</span><span class="sxs-lookup"><span data-stu-id="2e6b2-116">Requirement</span></span> | <span data-ttu-id="2e6b2-117">值</span><span class="sxs-lookup"><span data-stu-id="2e6b2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6b2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2e6b2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2e6b2-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2e6b2-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2e6b2-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e6b2-120">Library</span></span><br/> | <dl> <span data-ttu-id="2e6b2-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2e6b2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e6b2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e6b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6b2-123">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="2e6b2-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




