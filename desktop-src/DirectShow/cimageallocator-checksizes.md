---
description: CheckSizes 方法會根據目前的媒體類型來檢查配置器屬性。
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: 'CImageAllocator. CheckSizes 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989675"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="58cc5-103">CImageAllocator. CheckSizes 方法</span><span class="sxs-lookup"><span data-stu-id="58cc5-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="58cc5-104">`CheckSizes`方法會根據目前的媒體類型來檢查配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="58cc5-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="58cc5-105">語法</span><span class="sxs-lookup"><span data-stu-id="58cc5-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="58cc5-106">參數</span><span class="sxs-lookup"><span data-stu-id="58cc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58cc5-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="58cc5-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="58cc5-108">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，此結構描述所要求的配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="58cc5-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58cc5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="58cc5-109">Return value</span></span>

<span data-ttu-id="58cc5-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="58cc5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="58cc5-111">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="58cc5-111">Possible values include the following.</span></span>



| <span data-ttu-id="58cc5-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="58cc5-112">Return code</span></span>                                                                                           | <span data-ttu-id="58cc5-113">Description</span><span class="sxs-lookup"><span data-stu-id="58cc5-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58cc5-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="58cc5-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="58cc5-115">要求的屬性與媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="58cc5-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="58cc5-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="58cc5-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="58cc5-117">要求的屬性與媒體類型不相容。</span><span class="sxs-lookup"><span data-stu-id="58cc5-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="58cc5-118"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="58cc5-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="58cc5-119">未連接擁有的 pin。</span><span class="sxs-lookup"><span data-stu-id="58cc5-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="58cc5-120">備註</span><span class="sxs-lookup"><span data-stu-id="58cc5-120">Remarks</span></span>

<span data-ttu-id="58cc5-121">當方法傳回時，如果傳回值為 S \_ OK， *PRequest* 的 **cbBuffer** 成員就會包含實際的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="58cc5-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="58cc5-122">這可能大於所要求的大小，但永遠不會較小。</span><span class="sxs-lookup"><span data-stu-id="58cc5-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="58cc5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="58cc5-123">Requirements</span></span>



| <span data-ttu-id="58cc5-124">需求</span><span class="sxs-lookup"><span data-stu-id="58cc5-124">Requirement</span></span> | <span data-ttu-id="58cc5-125">值</span><span class="sxs-lookup"><span data-stu-id="58cc5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58cc5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="58cc5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="58cc5-127"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="58cc5-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="58cc5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="58cc5-128">Library</span></span><br/> | <dl> <span data-ttu-id="58cc5-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="58cc5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58cc5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58cc5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58cc5-131">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="58cc5-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




