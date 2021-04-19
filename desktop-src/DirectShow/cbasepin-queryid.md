---
description: QueryId 方法會抓取 pin 識別碼。 這個方法會實 IPin：： QueryId 方法。
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: 'CBasePin. QueryId 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989609"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="69b59-104">CBasePin. QueryId 方法</span><span class="sxs-lookup"><span data-stu-id="69b59-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="69b59-105">方法會抓取 `QueryId` pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="69b59-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="69b59-106">這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。</span><span class="sxs-lookup"><span data-stu-id="69b59-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b59-107">語法</span><span class="sxs-lookup"><span data-stu-id="69b59-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="69b59-108">參數</span><span class="sxs-lookup"><span data-stu-id="69b59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b59-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="69b59-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="69b59-110">Pin 識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="69b59-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b59-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="69b59-111">Return value</span></span>

<span data-ttu-id="69b59-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="69b59-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="69b59-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="69b59-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="69b59-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="69b59-114">Return code</span></span>                                                                                   | <span data-ttu-id="69b59-115">Description</span><span class="sxs-lookup"><span data-stu-id="69b59-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="69b59-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="69b59-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="69b59-117">成功。</span><span class="sxs-lookup"><span data-stu-id="69b59-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="69b59-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="69b59-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="69b59-119">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="69b59-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="69b59-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="69b59-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="69b59-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="69b59-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69b59-122">備註</span><span class="sxs-lookup"><span data-stu-id="69b59-122">Remarks</span></span>

<span data-ttu-id="69b59-123">這個方法會傳回 [**CBasePin：： m \_ pName**](cbasepin-m-pname.md) 成員變數的複本。</span><span class="sxs-lookup"><span data-stu-id="69b59-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b59-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="69b59-124">Requirements</span></span>



| <span data-ttu-id="69b59-125">需求</span><span class="sxs-lookup"><span data-stu-id="69b59-125">Requirement</span></span> | <span data-ttu-id="69b59-126">值</span><span class="sxs-lookup"><span data-stu-id="69b59-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b59-127">標頭</span><span class="sxs-lookup"><span data-stu-id="69b59-127">Header</span></span><br/>  | <dl> <span data-ttu-id="69b59-128"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="69b59-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="69b59-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="69b59-129">Library</span></span><br/> | <dl> <span data-ttu-id="69b59-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="69b59-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b59-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69b59-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b59-132">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="69b59-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




