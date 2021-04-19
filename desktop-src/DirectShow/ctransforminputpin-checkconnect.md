---
description: CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: 'CTransformInputPin. CheckConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985769"
---
# <a name="ctransforminputpincheckconnect-method"></a><span data-ttu-id="82dae-103">CTransformInputPin. CheckConnect 方法</span><span class="sxs-lookup"><span data-stu-id="82dae-103">CTransformInputPin.CheckConnect method</span></span>

<span data-ttu-id="82dae-104">`CheckConnect`方法會判斷是否適合使用 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="82dae-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dae-105">語法</span><span class="sxs-lookup"><span data-stu-id="82dae-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="82dae-106">參數</span><span class="sxs-lookup"><span data-stu-id="82dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82dae-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="82dae-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="82dae-108">輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="82dae-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82dae-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="82dae-109">Return value</span></span>

<span data-ttu-id="82dae-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="82dae-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="82dae-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="82dae-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="82dae-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="82dae-112">Return code</span></span>                                                                                               | <span data-ttu-id="82dae-113">Description</span><span class="sxs-lookup"><span data-stu-id="82dae-113">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="82dae-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="82dae-114"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="82dae-115">Success</span><span class="sxs-lookup"><span data-stu-id="82dae-115">Success</span></span><br/>             |
| <dl> <span data-ttu-id="82dae-116"><dt>**VFW \_ E \_ 不正確 \_ 方向**</dt></span><span class="sxs-lookup"><span data-stu-id="82dae-116"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="82dae-117">錯誤的 pin 方向</span><span class="sxs-lookup"><span data-stu-id="82dae-117">Wrong pin direction</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82dae-118">備註</span><span class="sxs-lookup"><span data-stu-id="82dae-118">Remarks</span></span>

<span data-ttu-id="82dae-119">這個方法會覆寫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="82dae-119">This method overrides the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method.</span></span> <span data-ttu-id="82dae-120">它會呼叫篩選器的 [**CTransformFilter：： CheckConnect**](ctransformfilter-checkconnect.md) 方法，它會 \_ 在基類中傳回 s OK。</span><span class="sxs-lookup"><span data-stu-id="82dae-120">It calls the filter's [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="82dae-121">衍生類別可以覆寫 **CTransformFilter：： CheckConnect** 方法，以執行額外的檢查。</span><span class="sxs-lookup"><span data-stu-id="82dae-121">The derived class can override the **CTransformFilter::CheckConnect** method to perform additional checks.</span></span>

## <a name="requirements"></a><span data-ttu-id="82dae-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="82dae-122">Requirements</span></span>



| <span data-ttu-id="82dae-123">需求</span><span class="sxs-lookup"><span data-stu-id="82dae-123">Requirement</span></span> | <span data-ttu-id="82dae-124">值</span><span class="sxs-lookup"><span data-stu-id="82dae-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82dae-125">標頭</span><span class="sxs-lookup"><span data-stu-id="82dae-125">Header</span></span><br/>  | <dl> <span data-ttu-id="82dae-126"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="82dae-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="82dae-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="82dae-127">Library</span></span><br/> | <dl> <span data-ttu-id="82dae-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="82dae-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




