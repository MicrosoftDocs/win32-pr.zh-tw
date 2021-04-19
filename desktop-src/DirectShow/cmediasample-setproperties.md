---
description: SetProperties 方法會設定範例的屬性。 這個方法會實 IMediaSample2：： SetProperties 方法。
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: 'CMediaSample. SetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995612"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="bed68-104">CMediaSample. SetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="bed68-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="bed68-105">`SetProperties`方法會設定範例的屬性。</span><span class="sxs-lookup"><span data-stu-id="bed68-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="bed68-106">這個方法會實 [**IMediaSample2：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) 方法。</span><span class="sxs-lookup"><span data-stu-id="bed68-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed68-107">語法</span><span class="sxs-lookup"><span data-stu-id="bed68-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="bed68-108">參數</span><span class="sxs-lookup"><span data-stu-id="bed68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed68-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="bed68-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="bed68-110">要設定之屬性資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bed68-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bed68-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="bed68-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="bed68-112">*CbProperties* 大小的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="bed68-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed68-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bed68-113">Return value</span></span>

<span data-ttu-id="bed68-114">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="bed68-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="bed68-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bed68-115">Return code</span></span>                                                                                   | <span data-ttu-id="bed68-116">Description</span><span class="sxs-lookup"><span data-stu-id="bed68-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="bed68-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bed68-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bed68-118">Success</span><span class="sxs-lookup"><span data-stu-id="bed68-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="bed68-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bed68-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bed68-120">引數無效</span><span class="sxs-lookup"><span data-stu-id="bed68-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="bed68-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bed68-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bed68-122">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="bed68-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="bed68-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="bed68-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bed68-124">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="bed68-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bed68-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bed68-125">Requirements</span></span>



| <span data-ttu-id="bed68-126">需求</span><span class="sxs-lookup"><span data-stu-id="bed68-126">Requirement</span></span> | <span data-ttu-id="bed68-127">值</span><span class="sxs-lookup"><span data-stu-id="bed68-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed68-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bed68-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bed68-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bed68-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bed68-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="bed68-130">Library</span></span><br/> | <dl> <span data-ttu-id="bed68-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bed68-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed68-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bed68-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed68-133">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="bed68-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




