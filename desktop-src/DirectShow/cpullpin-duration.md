---
description: Duration 方法會捕獲資料流程的持續時間。
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: 'CPullPin Duration 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991333"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="ecf1c-103">CPullPin Duration 方法</span><span class="sxs-lookup"><span data-stu-id="ecf1c-103">CPullPin.Duration method</span></span>

<span data-ttu-id="ecf1c-104">`Duration`方法會捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="ecf1c-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ecf1c-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="ecf1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ecf1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf1c-107">*ptDuration*</span><span class="sxs-lookup"><span data-stu-id="ecf1c-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf1c-108">接收持續時間之變數的指標，以位元組乘以10000000。</span><span class="sxs-lookup"><span data-stu-id="ecf1c-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf1c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecf1c-109">Return value</span></span>

<span data-ttu-id="ecf1c-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ecf1c-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf1c-111">備註</span><span class="sxs-lookup"><span data-stu-id="ecf1c-111">Remarks</span></span>

<span data-ttu-id="ecf1c-112">在呼叫 [**CPullPin：： Connect**](cpullpin-connect.md) 方法之前，持續時間為不定。</span><span class="sxs-lookup"><span data-stu-id="ecf1c-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf1c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecf1c-113">Requirements</span></span>



| <span data-ttu-id="ecf1c-114">需求</span><span class="sxs-lookup"><span data-stu-id="ecf1c-114">Requirement</span></span> | <span data-ttu-id="ecf1c-115">值</span><span class="sxs-lookup"><span data-stu-id="ecf1c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf1c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ecf1c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ecf1c-117"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf1c-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="ecf1c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ecf1c-118">Library</span></span><br/> | <dl> <span data-ttu-id="ecf1c-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ecf1c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf1c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecf1c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf1c-121">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="ecf1c-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




