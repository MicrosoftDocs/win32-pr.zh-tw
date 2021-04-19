---
description: GetProperties 方法會抓取範例的屬性。 這個方法會實 IMediaSample2：： GetProperties 方法。
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: 'CMediaSample. GetProperties 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989696"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="7e726-104">CMediaSample. GetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="7e726-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="7e726-105">`GetProperties`方法會捕獲範例的屬性。</span><span class="sxs-lookup"><span data-stu-id="7e726-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="7e726-106">這個方法會實 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 方法。</span><span class="sxs-lookup"><span data-stu-id="7e726-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e726-107">語法</span><span class="sxs-lookup"><span data-stu-id="7e726-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="7e726-108">參數</span><span class="sxs-lookup"><span data-stu-id="7e726-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e726-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="7e726-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="7e726-110">要取出的屬性資料長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e726-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7e726-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="7e726-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="7e726-112">*CbProperties* 大小的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="7e726-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e726-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e726-113">Return value</span></span>

<span data-ttu-id="7e726-114">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7e726-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7e726-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7e726-115">Return code</span></span>                                                                               | <span data-ttu-id="7e726-116">Description</span><span class="sxs-lookup"><span data-stu-id="7e726-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7e726-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7e726-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7e726-118">成功。</span><span class="sxs-lookup"><span data-stu-id="7e726-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="7e726-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="7e726-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7e726-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="7e726-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7e726-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e726-121">Requirements</span></span>



| <span data-ttu-id="7e726-122">需求</span><span class="sxs-lookup"><span data-stu-id="7e726-122">Requirement</span></span> | <span data-ttu-id="7e726-123">值</span><span class="sxs-lookup"><span data-stu-id="7e726-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e726-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7e726-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7e726-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7e726-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e726-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e726-126">Library</span></span><br/> | <dl> <span data-ttu-id="7e726-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7e726-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e726-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e726-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e726-129">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="7e726-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




