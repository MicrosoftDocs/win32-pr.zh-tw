---
description: SetActualDataLength 方法會設定緩衝區中有效資料的長度。 這個方法會實 IMediaSample：： SetActualDataLength 方法。
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: 'CMediaSample. SetActualDataLength 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978615"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="01805-104">CMediaSample. SetActualDataLength 方法</span><span class="sxs-lookup"><span data-stu-id="01805-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="01805-105">`SetActualDataLength`方法會設定緩衝區中有效資料的長度。</span><span class="sxs-lookup"><span data-stu-id="01805-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="01805-106">這個方法會實 [**IMediaSample：： SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) 方法。</span><span class="sxs-lookup"><span data-stu-id="01805-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01805-107">語法</span><span class="sxs-lookup"><span data-stu-id="01805-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="01805-108">參數</span><span class="sxs-lookup"><span data-stu-id="01805-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01805-109">*lLen*</span><span class="sxs-lookup"><span data-stu-id="01805-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="01805-110">有效資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="01805-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01805-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="01805-111">Return value</span></span>

<span data-ttu-id="01805-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="01805-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="01805-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="01805-113">Return code</span></span>                                                                                             | <span data-ttu-id="01805-114">Description</span><span class="sxs-lookup"><span data-stu-id="01805-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="01805-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="01805-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="01805-116">成功。</span><span class="sxs-lookup"><span data-stu-id="01805-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="01805-117"><dt>**VFW \_ E \_ 緩衝區 \_ 溢出**</dt></span><span class="sxs-lookup"><span data-stu-id="01805-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="01805-118">*lLen* 大於配置的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="01805-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01805-119">備註</span><span class="sxs-lookup"><span data-stu-id="01805-119">Remarks</span></span>

<span data-ttu-id="01805-120">這個方法會設定 [**CMediaSample：： m \_ lActual**](cmediasample-m-lactual.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="01805-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="01805-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="01805-121">Requirements</span></span>



| <span data-ttu-id="01805-122">需求</span><span class="sxs-lookup"><span data-stu-id="01805-122">Requirement</span></span> | <span data-ttu-id="01805-123">值</span><span class="sxs-lookup"><span data-stu-id="01805-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01805-124">標頭</span><span class="sxs-lookup"><span data-stu-id="01805-124">Header</span></span><br/>  | <dl> <span data-ttu-id="01805-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="01805-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="01805-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="01805-126">Library</span></span><br/> | <dl> <span data-ttu-id="01805-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="01805-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01805-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01805-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01805-129">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="01805-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




