---
description: 當篩選參數切換至 [已停止] 狀態時，就會呼叫 StopStreaming 方法。
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: 'CTransformFilter. StopStreaming 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978406"
---
# <a name="ctransformfilterstopstreaming-method"></a><span data-ttu-id="2bab3-103">CTransformFilter. StopStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="2bab3-103">CTransformFilter.StopStreaming method</span></span>

<span data-ttu-id="2bab3-104">`StopStreaming`當篩選參數切換至 [已停止] 狀態時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="2bab3-104">The `StopStreaming` method is called when the filter switches to the stopped state.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bab3-105">語法</span><span class="sxs-lookup"><span data-stu-id="2bab3-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="2bab3-106">參數</span><span class="sxs-lookup"><span data-stu-id="2bab3-106">Parameters</span></span>

<span data-ttu-id="2bab3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2bab3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bab3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bab3-108">Return value</span></span>

<span data-ttu-id="2bab3-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2bab3-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bab3-110">備註</span><span class="sxs-lookup"><span data-stu-id="2bab3-110">Remarks</span></span>

<span data-ttu-id="2bab3-111">這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="2bab3-111">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bab3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bab3-112">Requirements</span></span>



| <span data-ttu-id="2bab3-113">需求</span><span class="sxs-lookup"><span data-stu-id="2bab3-113">Requirement</span></span> | <span data-ttu-id="2bab3-114">值</span><span class="sxs-lookup"><span data-stu-id="2bab3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bab3-115">標頭</span><span class="sxs-lookup"><span data-stu-id="2bab3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2bab3-116"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2bab3-116"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2bab3-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="2bab3-117">Library</span></span><br/> | <dl> <span data-ttu-id="2bab3-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2bab3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bab3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bab3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bab3-120">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="2bab3-120">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




