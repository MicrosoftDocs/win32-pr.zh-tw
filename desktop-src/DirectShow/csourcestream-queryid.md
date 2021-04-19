---
description: QueryId 方法會抓取 pin 的識別碼。
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: 'CSourceStream. QueryId 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995386"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="d8ce9-103">CSourceStream. QueryId 方法</span><span class="sxs-lookup"><span data-stu-id="d8ce9-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="d8ce9-104">方法會抓取 `QueryId` pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ce9-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8ce9-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="d8ce9-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8ce9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ce9-107">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="d8ce9-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d8ce9-108">變數的指標，此變數會接收包含 pin 識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ce9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8ce9-109">Return value</span></span>

<span data-ttu-id="d8ce9-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d8ce9-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d8ce9-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d8ce9-112">Return code</span></span>                                                                                       | <span data-ttu-id="d8ce9-113">Description</span><span class="sxs-lookup"><span data-stu-id="d8ce9-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="d8ce9-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ce9-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="d8ce9-115">成功。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="d8ce9-116"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ce9-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="d8ce9-117">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="d8ce9-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ce9-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="d8ce9-119">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="d8ce9-120"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8ce9-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d8ce9-121">在篩選準則中找不到 Pin。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8ce9-122">備註</span><span class="sxs-lookup"><span data-stu-id="d8ce9-122">Remarks</span></span>

<span data-ttu-id="d8ce9-123">這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="d8ce9-124">為了建立識別碼字串，pin 會呼叫 [**CSource：： FindPinNumber**](csource-findpinnumber.md) 方法，並以其本身做為參數。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="d8ce9-125">**FindPinNumber** 方法會傳回從零開始編制索引的 pin 碼。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="d8ce9-126">`QueryId` 將傳回值遞增1，並將結果轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="d8ce9-127">例如，第一個 pin 變成 "1";第二個 pin 會變成 "2";等等。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="d8ce9-128">如果這個方法傳回 VFW \_ E 找 \_ 不到 \_ ，則表示篩選的釘選陣列無效，可能是因為篩選器中的錯誤所造成。</span><span class="sxs-lookup"><span data-stu-id="d8ce9-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ce9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8ce9-129">Requirements</span></span>



| <span data-ttu-id="d8ce9-130">需求</span><span class="sxs-lookup"><span data-stu-id="d8ce9-130">Requirement</span></span> | <span data-ttu-id="d8ce9-131">值</span><span class="sxs-lookup"><span data-stu-id="d8ce9-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ce9-132">標頭</span><span class="sxs-lookup"><span data-stu-id="d8ce9-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d8ce9-133"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="d8ce9-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d8ce9-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8ce9-134">Library</span></span><br/> | <dl> <span data-ttu-id="d8ce9-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d8ce9-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ce9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8ce9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ce9-137">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="d8ce9-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




