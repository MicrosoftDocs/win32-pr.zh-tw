---
description: BeginFlush 方法會開始進行清除作業。 這個方法會實 IPin：： BeginFlush 方法。
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: 'CTransformInputPin. BeginFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998405"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="e4317-104">CTransformInputPin. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="e4317-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="e4317-105">`BeginFlush`方法會開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="e4317-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="e4317-106">這個方法會實 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="e4317-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4317-107">語法</span><span class="sxs-lookup"><span data-stu-id="e4317-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e4317-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4317-108">Parameters</span></span>

<span data-ttu-id="e4317-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e4317-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4317-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4317-110">Return value</span></span>

<span data-ttu-id="e4317-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e4317-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e4317-112">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="e4317-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e4317-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e4317-113">Return code</span></span>                                                                                           | <span data-ttu-id="e4317-114">Description</span><span class="sxs-lookup"><span data-stu-id="e4317-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="e4317-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e4317-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="e4317-116">成功。</span><span class="sxs-lookup"><span data-stu-id="e4317-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="e4317-117"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="e4317-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e4317-118">輸出 pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="e4317-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4317-119">備註</span><span class="sxs-lookup"><span data-stu-id="e4317-119">Remarks</span></span>

<span data-ttu-id="e4317-120">這個方法會呼叫釘選的 [**CBaseInputPin：： BeginFlush**](cbaseinputpin-beginflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e4317-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="e4317-121">然後，它會呼叫篩選器的 [**CTransformFilter：： BeginFlush**](ctransformfilter-beginflush.md) 方法，以傳遞下游的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e4317-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4317-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4317-122">Requirements</span></span>



| <span data-ttu-id="e4317-123">需求</span><span class="sxs-lookup"><span data-stu-id="e4317-123">Requirement</span></span> | <span data-ttu-id="e4317-124">值</span><span class="sxs-lookup"><span data-stu-id="e4317-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4317-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e4317-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e4317-126"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e4317-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4317-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4317-127">Library</span></span><br/> | <dl> <span data-ttu-id="e4317-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e4317-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




