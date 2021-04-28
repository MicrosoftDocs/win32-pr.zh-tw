---
description: CBaseRenderer. EndFlush 方法-EndFlush 方法會結束清除作業。
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
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095906"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="baac7-103">CBaseRenderer. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="baac7-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="baac7-104">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="baac7-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="baac7-105">語法</span><span class="sxs-lookup"><span data-stu-id="baac7-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="baac7-106">參數</span><span class="sxs-lookup"><span data-stu-id="baac7-106">Parameters</span></span>

<span data-ttu-id="baac7-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="baac7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="baac7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="baac7-108">Return value</span></span>

<span data-ttu-id="baac7-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="baac7-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="baac7-110">備註</span><span class="sxs-lookup"><span data-stu-id="baac7-110">Remarks</span></span>

<span data-ttu-id="baac7-111">當篩選準則的輸入 pin 收到 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法的呼叫時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="baac7-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="baac7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="baac7-112">Requirements</span></span>



| <span data-ttu-id="baac7-113">需求</span><span class="sxs-lookup"><span data-stu-id="baac7-113">Requirement</span></span> | <span data-ttu-id="baac7-114">值</span><span class="sxs-lookup"><span data-stu-id="baac7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baac7-115">標頭</span><span class="sxs-lookup"><span data-stu-id="baac7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="baac7-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="baac7-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="baac7-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="baac7-117">Library</span></span><br/> | <dl> <span data-ttu-id="baac7-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="baac7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baac7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baac7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baac7-120">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="baac7-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




