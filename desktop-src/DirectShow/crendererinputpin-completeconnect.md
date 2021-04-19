---
description: CompleteConnect 方法會完成輸出釘選的連接。 這個方法會覆寫 CBasePin：： CompleteConnect 方法。
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: 'CRendererInputPin. CompleteConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996087"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="3bbd5-104">CRendererInputPin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="3bbd5-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="3bbd5-105">`CompleteConnect`方法會完成輸出釘選的連接。</span><span class="sxs-lookup"><span data-stu-id="3bbd5-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="3bbd5-106">這個方法會覆寫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3bbd5-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbd5-107">語法</span><span class="sxs-lookup"><span data-stu-id="3bbd5-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="3bbd5-108">參數</span><span class="sxs-lookup"><span data-stu-id="3bbd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbd5-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="3bbd5-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="3bbd5-110">輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標</span><span class="sxs-lookup"><span data-stu-id="3bbd5-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbd5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bbd5-111">Return value</span></span>

<span data-ttu-id="3bbd5-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3bbd5-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbd5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bbd5-113">Requirements</span></span>



| <span data-ttu-id="3bbd5-114">需求</span><span class="sxs-lookup"><span data-stu-id="3bbd5-114">Requirement</span></span> | <span data-ttu-id="3bbd5-115">值</span><span class="sxs-lookup"><span data-stu-id="3bbd5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbd5-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3bbd5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3bbd5-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3bbd5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3bbd5-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3bbd5-118">Library</span></span><br/> | <dl> <span data-ttu-id="3bbd5-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3bbd5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bbd5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bbd5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbd5-121">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="3bbd5-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




