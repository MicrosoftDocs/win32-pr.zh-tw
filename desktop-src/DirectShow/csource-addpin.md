---
description: AddPin 方法會將新的輸出圖釘新增至篩選準則。
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: 'CSource. AddPin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977154"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="882fa-103">CSource. AddPin 方法</span><span class="sxs-lookup"><span data-stu-id="882fa-103">CSource.AddPin method</span></span>

<span data-ttu-id="882fa-104">`AddPin`方法會將新的輸出圖釘新增至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="882fa-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="882fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="882fa-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="882fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="882fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882fa-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="882fa-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="882fa-108">[**CSourceStream**](csourcestream.md)物件的指標，該物件會執行釘選。</span><span class="sxs-lookup"><span data-stu-id="882fa-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882fa-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="882fa-109">Return value</span></span>

<span data-ttu-id="882fa-110">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="882fa-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="882fa-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="882fa-111">Return code</span></span>                                                                                   | <span data-ttu-id="882fa-112">Description</span><span class="sxs-lookup"><span data-stu-id="882fa-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="882fa-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="882fa-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="882fa-114">Success</span><span class="sxs-lookup"><span data-stu-id="882fa-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="882fa-115"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="882fa-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="882fa-116">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="882fa-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="882fa-117">備註</span><span class="sxs-lookup"><span data-stu-id="882fa-117">Remarks</span></span>

<span data-ttu-id="882fa-118">當您建立衍生自 **CSourceStream** 的新 pin 碼時， **CSourceStream** 的函式會自動呼叫此方法，以將輸出釘選至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="882fa-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="882fa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="882fa-119">Requirements</span></span>



| <span data-ttu-id="882fa-120">需求</span><span class="sxs-lookup"><span data-stu-id="882fa-120">Requirement</span></span> | <span data-ttu-id="882fa-121">值</span><span class="sxs-lookup"><span data-stu-id="882fa-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882fa-122">標頭</span><span class="sxs-lookup"><span data-stu-id="882fa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="882fa-123"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="882fa-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="882fa-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="882fa-124">Library</span></span><br/> | <dl> <span data-ttu-id="882fa-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="882fa-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882fa-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="882fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882fa-127">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="882fa-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




