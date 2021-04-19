---
description: 複製方法會複製媒體範例。
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: 'CTransInPlaceFilter 複製方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978498"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="daf28-103">CTransInPlaceFilter 複製方法</span><span class="sxs-lookup"><span data-stu-id="daf28-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="daf28-104">`Copy`方法會複製媒體範例。</span><span class="sxs-lookup"><span data-stu-id="daf28-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf28-105">語法</span><span class="sxs-lookup"><span data-stu-id="daf28-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="daf28-106">參數</span><span class="sxs-lookup"><span data-stu-id="daf28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf28-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="daf28-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="daf28-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="daf28-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf28-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="daf28-109">Return value</span></span>

<span data-ttu-id="daf28-110">傳回新範例上 **IMediaSample** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="daf28-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf28-111">備註</span><span class="sxs-lookup"><span data-stu-id="daf28-111">Remarks</span></span>

<span data-ttu-id="daf28-112">這個方法會從下游配置器抓取空的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="daf28-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="daf28-113">它會將 *pSource* 中的所有範例屬性複製到新的範例中，以及範例中的實際資料。</span><span class="sxs-lookup"><span data-stu-id="daf28-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="daf28-114">如果篩選準則使用兩個配置器，則會呼叫這個方法來跨緩衝區複製資料。</span><span class="sxs-lookup"><span data-stu-id="daf28-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf28-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="daf28-115">Requirements</span></span>



| <span data-ttu-id="daf28-116">需求</span><span class="sxs-lookup"><span data-stu-id="daf28-116">Requirement</span></span> | <span data-ttu-id="daf28-117">值</span><span class="sxs-lookup"><span data-stu-id="daf28-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf28-118">標頭</span><span class="sxs-lookup"><span data-stu-id="daf28-118">Header</span></span><br/>  | <dl> <span data-ttu-id="daf28-119"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="daf28-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="daf28-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="daf28-120">Library</span></span><br/> | <dl> <span data-ttu-id="daf28-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="daf28-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf28-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="daf28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf28-123">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="daf28-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




