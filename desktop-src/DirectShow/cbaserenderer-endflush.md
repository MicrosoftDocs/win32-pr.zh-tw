---
description: EndFlush 方法會結束清除作業。
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: 'CBaseRenderer. EndFlush 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000850"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="7f72c-103">CBaseRenderer. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="7f72c-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="7f72c-104">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="7f72c-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f72c-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f72c-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="7f72c-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f72c-106">Parameters</span></span>

<span data-ttu-id="7f72c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7f72c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f72c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f72c-108">Return value</span></span>

<span data-ttu-id="7f72c-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7f72c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f72c-110">備註</span><span class="sxs-lookup"><span data-stu-id="7f72c-110">Remarks</span></span>

<span data-ttu-id="7f72c-111">當篩選準則的輸入 pin 收到 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法的呼叫時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f72c-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f72c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f72c-112">Requirements</span></span>



| <span data-ttu-id="7f72c-113">需求</span><span class="sxs-lookup"><span data-stu-id="7f72c-113">Requirement</span></span> | <span data-ttu-id="7f72c-114">值</span><span class="sxs-lookup"><span data-stu-id="7f72c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f72c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="7f72c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7f72c-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f72c-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f72c-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f72c-117">Library</span></span><br/> | <dl> <span data-ttu-id="7f72c-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f72c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f72c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f72c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f72c-120">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="7f72c-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




