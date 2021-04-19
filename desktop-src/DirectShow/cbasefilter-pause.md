---
description: Pause 方法會暫停篩選。 這個方法會實 IMediaFilter：:P ause 方法。
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
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990985"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="7c797-104">CBaseFilter. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="7c797-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="7c797-105">`Pause`方法會暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="7c797-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="7c797-106">這個方法會實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c797-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c797-107">語法</span><span class="sxs-lookup"><span data-stu-id="7c797-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="7c797-108">參數</span><span class="sxs-lookup"><span data-stu-id="7c797-108">Parameters</span></span>

<span data-ttu-id="7c797-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7c797-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c797-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c797-110">Return value</span></span>

<span data-ttu-id="7c797-111">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7c797-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c797-112">備註</span><span class="sxs-lookup"><span data-stu-id="7c797-112">Remarks</span></span>

<span data-ttu-id="7c797-113">這個方法會在每個篩選器的連接釘上呼叫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c797-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c797-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c797-114">Requirements</span></span>



| <span data-ttu-id="7c797-115">需求</span><span class="sxs-lookup"><span data-stu-id="7c797-115">Requirement</span></span> | <span data-ttu-id="7c797-116">值</span><span class="sxs-lookup"><span data-stu-id="7c797-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c797-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7c797-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c797-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7c797-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7c797-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c797-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c797-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7c797-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c797-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c797-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c797-122">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="7c797-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




