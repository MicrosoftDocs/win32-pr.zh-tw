---
description: WaitEvent 方法會等候，直到指定的事件發出信號為止。
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: 'CDynamicOutputPin. WaitEvent 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997773"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="95948-103">CDynamicOutputPin. WaitEvent 方法</span><span class="sxs-lookup"><span data-stu-id="95948-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="95948-104">`WaitEvent`方法會等候，直到指定的事件發出信號為止。</span><span class="sxs-lookup"><span data-stu-id="95948-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="95948-105">語法</span><span class="sxs-lookup"><span data-stu-id="95948-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="95948-106">參數</span><span class="sxs-lookup"><span data-stu-id="95948-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95948-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="95948-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="95948-108">事件的控制代碼。</span><span class="sxs-lookup"><span data-stu-id="95948-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95948-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="95948-109">Return value</span></span>

<span data-ttu-id="95948-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="95948-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="95948-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="95948-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="95948-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="95948-112">Return code</span></span>                                                                                  | <span data-ttu-id="95948-113">Description</span><span class="sxs-lookup"><span data-stu-id="95948-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="95948-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="95948-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="95948-115">成功。</span><span class="sxs-lookup"><span data-stu-id="95948-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="95948-116"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="95948-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="95948-117">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95948-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="95948-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="95948-118">Requirements</span></span>



| <span data-ttu-id="95948-119">需求</span><span class="sxs-lookup"><span data-stu-id="95948-119">Requirement</span></span> | <span data-ttu-id="95948-120">值</span><span class="sxs-lookup"><span data-stu-id="95948-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95948-121">標頭</span><span class="sxs-lookup"><span data-stu-id="95948-121">Header</span></span><br/>  | <dl> <span data-ttu-id="95948-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="95948-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95948-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="95948-123">Library</span></span><br/> | <dl> <span data-ttu-id="95948-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="95948-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95948-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95948-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95948-126">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="95948-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




