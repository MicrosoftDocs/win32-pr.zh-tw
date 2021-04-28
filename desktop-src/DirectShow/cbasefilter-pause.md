---
description: CBaseFilter： pause 方法： Pause 方法會暫停篩選。 這個方法會實 IMediaFilter：:P ause 方法。
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: 'CBaseFilter： Pause 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120086"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="e1bdb-104">CBaseFilter. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="e1bdb-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="e1bdb-105">`Pause`方法會暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="e1bdb-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="e1bdb-106">這個方法會實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。</span><span class="sxs-lookup"><span data-stu-id="e1bdb-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bdb-107">語法</span><span class="sxs-lookup"><span data-stu-id="e1bdb-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="e1bdb-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1bdb-108">Parameters</span></span>

<span data-ttu-id="e1bdb-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e1bdb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1bdb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1bdb-110">Return value</span></span>

<span data-ttu-id="e1bdb-111">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e1bdb-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bdb-112">備註</span><span class="sxs-lookup"><span data-stu-id="e1bdb-112">Remarks</span></span>

<span data-ttu-id="e1bdb-113">這個方法會在每個篩選器的連接釘上呼叫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e1bdb-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1bdb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1bdb-114">Requirements</span></span>



| <span data-ttu-id="e1bdb-115">需求</span><span class="sxs-lookup"><span data-stu-id="e1bdb-115">Requirement</span></span> | <span data-ttu-id="e1bdb-116">值</span><span class="sxs-lookup"><span data-stu-id="e1bdb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bdb-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e1bdb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e1bdb-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e1bdb-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1bdb-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1bdb-119">Library</span></span><br/> | <dl> <span data-ttu-id="e1bdb-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e1bdb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1bdb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1bdb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1bdb-122">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="e1bdb-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




