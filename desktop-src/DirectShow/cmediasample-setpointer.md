---
description: SetPointer 方法會將指標設定為記憶體緩衝區。
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: 'CMediaSample. SetPointer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999123"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="04f50-103">CMediaSample. SetPointer 方法</span><span class="sxs-lookup"><span data-stu-id="04f50-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="04f50-104">`SetPointer`方法會將指標設定為記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="04f50-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f50-105">語法</span><span class="sxs-lookup"><span data-stu-id="04f50-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="04f50-106">參數</span><span class="sxs-lookup"><span data-stu-id="04f50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f50-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="04f50-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="04f50-108">呼叫端所配置的記憶體緩衝區指標，大小為 *cBytes*。</span><span class="sxs-lookup"><span data-stu-id="04f50-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="04f50-109">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="04f50-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="04f50-110">緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="04f50-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f50-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="04f50-111">Return value</span></span>

<span data-ttu-id="04f50-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="04f50-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f50-113">備註</span><span class="sxs-lookup"><span data-stu-id="04f50-113">Remarks</span></span>

<span data-ttu-id="04f50-114">此方法可讓配置器設定範例的新指標。</span><span class="sxs-lookup"><span data-stu-id="04f50-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="04f50-115">這個方法無法透過 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面使用。</span><span class="sxs-lookup"><span data-stu-id="04f50-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="04f50-116">建立範例的物件可以透過 **CMediaSample**) 存取此方法 (，但其他物件則不能。</span><span class="sxs-lookup"><span data-stu-id="04f50-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f50-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="04f50-117">Requirements</span></span>



| <span data-ttu-id="04f50-118">需求</span><span class="sxs-lookup"><span data-stu-id="04f50-118">Requirement</span></span> | <span data-ttu-id="04f50-119">值</span><span class="sxs-lookup"><span data-stu-id="04f50-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f50-120">標頭</span><span class="sxs-lookup"><span data-stu-id="04f50-120">Header</span></span><br/>  | <dl> <span data-ttu-id="04f50-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="04f50-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="04f50-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="04f50-122">Library</span></span><br/> | <dl> <span data-ttu-id="04f50-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="04f50-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f50-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04f50-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f50-125">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="04f50-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




