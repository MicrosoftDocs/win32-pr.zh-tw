---
description: BreakConnect 方法會從連接釋放輸入的 pin。
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: 'CBaseRenderer. BreakConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983083"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="314dd-103">CBaseRenderer. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="314dd-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="314dd-104">`BreakConnect`方法會從連接釋放輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="314dd-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="314dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="314dd-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="314dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="314dd-106">Parameters</span></span>

<span data-ttu-id="314dd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="314dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="314dd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="314dd-108">Return value</span></span>

<span data-ttu-id="314dd-109">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="314dd-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="314dd-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="314dd-110">Return code</span></span>                                                                                         | <span data-ttu-id="314dd-111">Description</span><span class="sxs-lookup"><span data-stu-id="314dd-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="314dd-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="314dd-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="314dd-113">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="314dd-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="314dd-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="314dd-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="314dd-115">成功。</span><span class="sxs-lookup"><span data-stu-id="314dd-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="314dd-116"><dt>**VFW \_ E \_ 未 \_ 停止**</dt></span><span class="sxs-lookup"><span data-stu-id="314dd-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="314dd-117">篩選仍處於使用中。</span><span class="sxs-lookup"><span data-stu-id="314dd-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="314dd-118">備註</span><span class="sxs-lookup"><span data-stu-id="314dd-118">Remarks</span></span>

<span data-ttu-id="314dd-119">篩選器的輸入圖釘會從它自己的方法內呼叫這個方法 `BreakConnect` 。</span><span class="sxs-lookup"><span data-stu-id="314dd-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="314dd-120"> (如需詳細資訊，請參閱 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md)。 ) 篩選準則會執行一些內部的簿記，例如重設資料流程結尾旗標。</span><span class="sxs-lookup"><span data-stu-id="314dd-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="314dd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="314dd-121">Requirements</span></span>



| <span data-ttu-id="314dd-122">需求</span><span class="sxs-lookup"><span data-stu-id="314dd-122">Requirement</span></span> | <span data-ttu-id="314dd-123">值</span><span class="sxs-lookup"><span data-stu-id="314dd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314dd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="314dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="314dd-125"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="314dd-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="314dd-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="314dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="314dd-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="314dd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314dd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="314dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314dd-129">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="314dd-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




