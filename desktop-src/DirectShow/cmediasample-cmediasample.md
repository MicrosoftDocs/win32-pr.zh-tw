---
description: 函式方法。
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: 'CMediaSample. CMediaSample (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981278"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="d72b8-103">CMediaSample. CMediaSample 函數</span><span class="sxs-lookup"><span data-stu-id="d72b8-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="d72b8-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="d72b8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d72b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="d72b8-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="d72b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="d72b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72b8-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d72b8-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d72b8-108">忽略。</span><span class="sxs-lookup"><span data-stu-id="d72b8-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d72b8-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="d72b8-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="d72b8-110">建立此範例之 [**CBaseAllocator**](cbaseallocator.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d72b8-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="d72b8-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="d72b8-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d72b8-112">忽略。</span><span class="sxs-lookup"><span data-stu-id="d72b8-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d72b8-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="d72b8-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="d72b8-114">由呼叫端配置的記憶體緩衝區指標，大小 *長度*。</span><span class="sxs-lookup"><span data-stu-id="d72b8-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="d72b8-115">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="d72b8-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="d72b8-116">記憶體緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="d72b8-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d72b8-117">備註</span><span class="sxs-lookup"><span data-stu-id="d72b8-117">Remarks</span></span>

<span data-ttu-id="d72b8-118">基類不會修改在 *phr* 參數中傳遞的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d72b8-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d72b8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d72b8-119">Requirements</span></span>



| <span data-ttu-id="d72b8-120">需求</span><span class="sxs-lookup"><span data-stu-id="d72b8-120">Requirement</span></span> | <span data-ttu-id="d72b8-121">值</span><span class="sxs-lookup"><span data-stu-id="d72b8-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d72b8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d72b8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d72b8-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d72b8-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d72b8-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="d72b8-124">Library</span></span><br/> | <dl> <span data-ttu-id="d72b8-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d72b8-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d72b8-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d72b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72b8-127">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="d72b8-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




