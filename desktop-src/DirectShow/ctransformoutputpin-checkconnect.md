---
description: CTransformOutputPin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: 'CTransformOutputPin. CheckConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094946"
---
# <a name="ctransformoutputpincheckconnect-method"></a><span data-ttu-id="cbcca-103">CTransformOutputPin. CheckConnect 方法</span><span class="sxs-lookup"><span data-stu-id="cbcca-103">CTransformOutputPin.CheckConnect method</span></span>

<span data-ttu-id="cbcca-104">`CheckConnect`方法會判斷是否適合使用 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="cbcca-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcca-105">語法</span><span class="sxs-lookup"><span data-stu-id="cbcca-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="cbcca-106">參數</span><span class="sxs-lookup"><span data-stu-id="cbcca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbcca-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="cbcca-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="cbcca-108">輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cbcca-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbcca-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbcca-109">Return value</span></span>

<span data-ttu-id="cbcca-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cbcca-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cbcca-111">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="cbcca-111">Possible values include the following.</span></span>



| <span data-ttu-id="cbcca-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cbcca-112">Return code</span></span>                                                                                  | <span data-ttu-id="cbcca-113">Description</span><span class="sxs-lookup"><span data-stu-id="cbcca-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="cbcca-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cbcca-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cbcca-115">成功。</span><span class="sxs-lookup"><span data-stu-id="cbcca-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cbcca-116"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="cbcca-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="cbcca-117">篩選的輸入 pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="cbcca-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbcca-118">備註</span><span class="sxs-lookup"><span data-stu-id="cbcca-118">Remarks</span></span>

<span data-ttu-id="cbcca-119">這個方法會覆寫 [**CBaseOutputPin：： CheckConnect**](cbaseoutputpin-checkconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cbcca-119">This method overrides the [**CBaseOutputPin::CheckConnect**](cbaseoutputpin-checkconnect.md) method.</span></span> <span data-ttu-id="cbcca-120">它會呼叫篩選器的 [**CTransformFilter：： CheckConnect**](ctransformfilter-checkconnect.md) 方法，它會 \_ 在基類中傳回 s OK。</span><span class="sxs-lookup"><span data-stu-id="cbcca-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="cbcca-121">衍生類別可以覆寫 **CTransformFilter：： CheckConnect** 方法，以執行額外的檢查。</span><span class="sxs-lookup"><span data-stu-id="cbcca-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbcca-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbcca-122">Requirements</span></span>



| <span data-ttu-id="cbcca-123">需求</span><span class="sxs-lookup"><span data-stu-id="cbcca-123">Requirement</span></span> | <span data-ttu-id="cbcca-124">值</span><span class="sxs-lookup"><span data-stu-id="cbcca-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcca-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cbcca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cbcca-126"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cbcca-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cbcca-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="cbcca-127">Library</span></span><br/> | <dl> <span data-ttu-id="cbcca-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cbcca-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




