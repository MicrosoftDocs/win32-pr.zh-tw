---
description: ConnectedIMemInputPin 方法會抓取下游輸入圖釘的指標。 這個方法會傳回 CBaseOutputPin：： m \_ pInputPin 成員變數。
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: 'CTransInPlaceOutputPin. ConnectedIMemInputPin 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977466"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="e7df4-104">CTransInPlaceOutputPin. ConnectedIMemInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="e7df4-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="e7df4-105">方法會抓取 `ConnectedIMemInputPin` 下游輸入圖釘的指標。</span><span class="sxs-lookup"><span data-stu-id="e7df4-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="e7df4-106">這個方法會傳回 [**CBaseOutputPin：： m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="e7df4-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7df4-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7df4-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="e7df4-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7df4-108">Parameters</span></span>

<span data-ttu-id="e7df4-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e7df4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7df4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7df4-110">Return value</span></span>

<span data-ttu-id="e7df4-111">傳回下游輸入釘選上 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e7df4-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7df4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7df4-112">Requirements</span></span>



| <span data-ttu-id="e7df4-113">需求</span><span class="sxs-lookup"><span data-stu-id="e7df4-113">Requirement</span></span> | <span data-ttu-id="e7df4-114">值</span><span class="sxs-lookup"><span data-stu-id="e7df4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7df4-115">標頭</span><span class="sxs-lookup"><span data-stu-id="e7df4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e7df4-116"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e7df4-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7df4-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="e7df4-117">Library</span></span><br/> | <dl> <span data-ttu-id="e7df4-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e7df4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7df4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7df4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7df4-120">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="e7df4-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




