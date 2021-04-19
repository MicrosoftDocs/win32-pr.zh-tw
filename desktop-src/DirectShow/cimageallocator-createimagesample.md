---
description: CreateImageSample 方法會建立媒體範例。
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: 'CImageAllocator. CreateImageSample 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995355"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="1f4cd-103">CImageAllocator. CreateImageSample 方法</span><span class="sxs-lookup"><span data-stu-id="1f4cd-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="1f4cd-104">`CreateImageSample`方法會建立媒體範例。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f4cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f4cd-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="1f4cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f4cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f4cd-107">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="1f4cd-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="1f4cd-108">大小 *長度* 緩衝區的指標，由呼叫端配置。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="1f4cd-109">*長度*</span><span class="sxs-lookup"><span data-stu-id="1f4cd-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="1f4cd-110">緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f4cd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f4cd-111">Return value</span></span>

<span data-ttu-id="1f4cd-112">傳回 [**CImageSample**](cimagesample.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f4cd-113">備註</span><span class="sxs-lookup"><span data-stu-id="1f4cd-113">Remarks</span></span>

<span data-ttu-id="1f4cd-114">這個方法會建立新的媒體範例，實作為 **CImageSample** 物件。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="1f4cd-115">範例的 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 方法會傳回 *.pdata* 參數中所指定之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="1f4cd-116">如果您從 [**CImageAllocator**](cimageallocator.md) 衍生新的配置器類別，並從 [**CImageSample**](cimagesample.md)衍生新的媒體範例類別，您應該覆寫這個方法，以建立媒體範例類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1f4cd-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f4cd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f4cd-117">Requirements</span></span>



| <span data-ttu-id="1f4cd-118">需求</span><span class="sxs-lookup"><span data-stu-id="1f4cd-118">Requirement</span></span> | <span data-ttu-id="1f4cd-119">值</span><span class="sxs-lookup"><span data-stu-id="1f4cd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f4cd-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1f4cd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1f4cd-121"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1f4cd-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f4cd-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f4cd-122">Library</span></span><br/> | <dl> <span data-ttu-id="1f4cd-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1f4cd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f4cd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f4cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f4cd-125">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="1f4cd-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="1f4cd-126">**CImageAllocator：：配置**</span><span class="sxs-lookup"><span data-stu-id="1f4cd-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




