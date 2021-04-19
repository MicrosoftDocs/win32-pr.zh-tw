---
description: CompleteConnect 方法會完成與另一個 pin 的連接。
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: 'CTransformInputPin. CompleteConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 455517968481b9333fbeba590aca644b34b2f5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994734"
---
# <a name="ctransforminputpincompleteconnect-method"></a><span data-ttu-id="8dcb4-103">CTransformInputPin. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="8dcb4-103">CTransformInputPin.CompleteConnect method</span></span>

<span data-ttu-id="8dcb4-104">`CompleteConnect`方法會完成與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="8dcb4-104">The `CompleteConnect` method completes a connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dcb4-105">語法</span><span class="sxs-lookup"><span data-stu-id="8dcb4-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="8dcb4-106">參數</span><span class="sxs-lookup"><span data-stu-id="8dcb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dcb4-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="8dcb4-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="8dcb4-108">指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8dcb4-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dcb4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8dcb4-109">Return value</span></span>

<span data-ttu-id="8dcb4-110">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8dcb4-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dcb4-111">備註</span><span class="sxs-lookup"><span data-stu-id="8dcb4-111">Remarks</span></span>

<span data-ttu-id="8dcb4-112">這個方法會覆寫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8dcb4-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="8dcb4-113">它會呼叫篩選器的 [**CTransformFilter：： CompleteConnect**](ctransformfilter-completeconnect.md) 方法，它會 \_ 在基類中傳回 s OK。</span><span class="sxs-lookup"><span data-stu-id="8dcb4-113">It calls the filter's [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="8dcb4-114">衍生類別可以覆寫 **CTransformFilter：： CompleteConnect** 方法，以執行額外的檢查。</span><span class="sxs-lookup"><span data-stu-id="8dcb4-114">The derived class can override the **CTransformFilter::CompleteConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dcb4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dcb4-115">Requirements</span></span>



| <span data-ttu-id="8dcb4-116">需求</span><span class="sxs-lookup"><span data-stu-id="8dcb4-116">Requirement</span></span> | <span data-ttu-id="8dcb4-117">值</span><span class="sxs-lookup"><span data-stu-id="8dcb4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dcb4-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8dcb4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8dcb4-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8dcb4-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8dcb4-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="8dcb4-120">Library</span></span><br/> | <dl> <span data-ttu-id="8dcb4-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8dcb4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




