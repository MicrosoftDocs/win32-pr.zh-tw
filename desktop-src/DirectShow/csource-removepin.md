---
description: RemovePin 方法會從篩選中移除指定的 pin。 方法不會刪除 pin。
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: 'CSource. RemovePin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987925"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="6e0c7-104">CSource. RemovePin 方法</span><span class="sxs-lookup"><span data-stu-id="6e0c7-104">CSource.RemovePin method</span></span>

<span data-ttu-id="6e0c7-105">`RemovePin`方法會從篩選中移除指定的 pin。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="6e0c7-106">方法不會刪除 pin。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0c7-107">語法</span><span class="sxs-lookup"><span data-stu-id="6e0c7-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="6e0c7-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e0c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0c7-109">*pStream*</span><span class="sxs-lookup"><span data-stu-id="6e0c7-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="6e0c7-110">[**CSourceStream**](csourcestream.md)物件的指標，該物件會執行釘選。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0c7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e0c7-111">Return value</span></span>

<span data-ttu-id="6e0c7-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6e0c7-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6e0c7-113">Return code</span></span>                                                                             | <span data-ttu-id="6e0c7-114">Description</span><span class="sxs-lookup"><span data-stu-id="6e0c7-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6e0c7-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c7-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6e0c7-116">成功。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="6e0c7-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c7-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6e0c7-118">篩選不包含此 pin。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e0c7-119">備註</span><span class="sxs-lookup"><span data-stu-id="6e0c7-119">Remarks</span></span>

<span data-ttu-id="6e0c7-120">「析構函數」方法會呼叫這個方法，以從篩選中移除輸出的釘選。</span><span class="sxs-lookup"><span data-stu-id="6e0c7-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0c7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e0c7-121">Requirements</span></span>



| <span data-ttu-id="6e0c7-122">需求</span><span class="sxs-lookup"><span data-stu-id="6e0c7-122">Requirement</span></span> | <span data-ttu-id="6e0c7-123">值</span><span class="sxs-lookup"><span data-stu-id="6e0c7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0c7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6e0c7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6e0c7-125"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="6e0c7-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6e0c7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e0c7-126">Library</span></span><br/> | <dl> <span data-ttu-id="6e0c7-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6e0c7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0c7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e0c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0c7-129">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="6e0c7-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




