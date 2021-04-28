---
description: CMediaSample。 CMediaSample 函式-函數方法。
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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095436"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="86f12-103">CMediaSample. CMediaSample 函數</span><span class="sxs-lookup"><span data-stu-id="86f12-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="86f12-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="86f12-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f12-105">語法</span><span class="sxs-lookup"><span data-stu-id="86f12-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="86f12-106">參數</span><span class="sxs-lookup"><span data-stu-id="86f12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f12-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="86f12-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="86f12-108">忽略。</span><span class="sxs-lookup"><span data-stu-id="86f12-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="86f12-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="86f12-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="86f12-110">建立此範例之 [**CBaseAllocator**](cbaseallocator.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="86f12-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="86f12-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="86f12-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="86f12-112">忽略。</span><span class="sxs-lookup"><span data-stu-id="86f12-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="86f12-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="86f12-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="86f12-114">由呼叫端配置的記憶體緩衝區指標，大小 *長度*。</span><span class="sxs-lookup"><span data-stu-id="86f12-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="86f12-115">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="86f12-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="86f12-116">記憶體緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="86f12-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86f12-117">備註</span><span class="sxs-lookup"><span data-stu-id="86f12-117">Remarks</span></span>

<span data-ttu-id="86f12-118">基類不會修改在 *phr* 參數中傳遞的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="86f12-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="86f12-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="86f12-119">Requirements</span></span>



| <span data-ttu-id="86f12-120">需求</span><span class="sxs-lookup"><span data-stu-id="86f12-120">Requirement</span></span> | <span data-ttu-id="86f12-121">值</span><span class="sxs-lookup"><span data-stu-id="86f12-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f12-122">標頭</span><span class="sxs-lookup"><span data-stu-id="86f12-122">Header</span></span><br/>  | <dl> <span data-ttu-id="86f12-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="86f12-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="86f12-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="86f12-124">Library</span></span><br/> | <dl> <span data-ttu-id="86f12-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="86f12-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f12-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86f12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f12-127">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="86f12-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




