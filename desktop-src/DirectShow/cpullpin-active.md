---
description: 使用中的方法會建立從輸出圖釘提取資料的工作者執行緒。 這個方法也會認可配置器。
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: 'CPullPin 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991255"
---
# <a name="cpullpinactive-method"></a><span data-ttu-id="e80ca-104">CPullPin 方法</span><span class="sxs-lookup"><span data-stu-id="e80ca-104">CPullPin.Active method</span></span>

<span data-ttu-id="e80ca-105">使用 **中** 的方法會建立從輸出圖釘提取資料的工作者執行緒。</span><span class="sxs-lookup"><span data-stu-id="e80ca-105">The **Active** method creates a worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="e80ca-106">這個方法也會認可配置器。</span><span class="sxs-lookup"><span data-stu-id="e80ca-106">This method also commits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="e80ca-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="e80ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="e80ca-108">Parameters</span></span>

<span data-ttu-id="e80ca-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e80ca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e80ca-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e80ca-110">Return value</span></span>

<span data-ttu-id="e80ca-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e80ca-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e80ca-112">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="e80ca-112">Possible values include the following.</span></span>



| <span data-ttu-id="e80ca-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e80ca-113">Return code</span></span>                                                                                  | <span data-ttu-id="e80ca-114">Description</span><span class="sxs-lookup"><span data-stu-id="e80ca-114">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="e80ca-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e80ca-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e80ca-116">成功。</span><span class="sxs-lookup"><span data-stu-id="e80ca-116">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="e80ca-117"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="e80ca-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="e80ca-118">Pin 連接未正確建立。</span><span class="sxs-lookup"><span data-stu-id="e80ca-118">The pin connection was not established correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="e80ca-119"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e80ca-119"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="e80ca-120">無法建立執行緒，或執行緒已經存在。</span><span class="sxs-lookup"><span data-stu-id="e80ca-120">Could not create the thread, or the thread already exists.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e80ca-121">備註</span><span class="sxs-lookup"><span data-stu-id="e80ca-121">Remarks</span></span>

<span data-ttu-id="e80ca-122">當擁有篩選變成作用中時，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e80ca-122">Call this method when the owning filter becomes active.</span></span> <span data-ttu-id="e80ca-123"> (如果您的輸入 pin 衍生自 [**CBasePin**](cbasepin.md)，請覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。 ) </span><span class="sxs-lookup"><span data-stu-id="e80ca-123">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Active**](cbasepin-active.md) method.)</span></span>

<span data-ttu-id="e80ca-124">在呼叫這個方法之前，請先呼叫 [**CPullPin：： Connect**](cpullpin-connect.md) 方法來建立與輸出圖釘的連接。</span><span class="sxs-lookup"><span data-stu-id="e80ca-124">Before calling this method, call the [**CPullPin::Connect**](cpullpin-connect.md) method to establish the connection with the output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80ca-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e80ca-125">Requirements</span></span>



| <span data-ttu-id="e80ca-126">需求</span><span class="sxs-lookup"><span data-stu-id="e80ca-126">Requirement</span></span> | <span data-ttu-id="e80ca-127">值</span><span class="sxs-lookup"><span data-stu-id="e80ca-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80ca-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e80ca-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e80ca-129"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="e80ca-129"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="e80ca-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="e80ca-130">Library</span></span><br/> | <dl> <span data-ttu-id="e80ca-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e80ca-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80ca-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e80ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80ca-133">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="e80ca-133">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




