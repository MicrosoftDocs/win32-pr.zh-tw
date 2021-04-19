---
description: GetIDsOfNames 方法會將一組名稱對應至一組對應的 Dispid。
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: 'CMediaPosition. GetIDsOfNames 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994857"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="fca90-103">CMediaPosition. GetIDsOfNames 方法</span><span class="sxs-lookup"><span data-stu-id="fca90-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="fca90-104">方法會將 `GetIDsOfNames` 一組名稱對應至一組對應的 dispid。</span><span class="sxs-lookup"><span data-stu-id="fca90-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca90-105">語法</span><span class="sxs-lookup"><span data-stu-id="fca90-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="fca90-106">參數</span><span class="sxs-lookup"><span data-stu-id="fca90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fca90-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="fca90-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="fca90-108">保留的。</span><span class="sxs-lookup"><span data-stu-id="fca90-108">Reserved.</span></span> <span data-ttu-id="fca90-109">使用 IID \_ Null。</span><span class="sxs-lookup"><span data-stu-id="fca90-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="fca90-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="fca90-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="fca90-111">寬字元字串陣列的位址，其中包含要對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="fca90-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="fca90-112">*Cname*</span><span class="sxs-lookup"><span data-stu-id="fca90-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="fca90-113">*RgszNames* 參數所指定的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="fca90-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fca90-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="fca90-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="fca90-115">要在其中解讀名稱的地區設定內容。</span><span class="sxs-lookup"><span data-stu-id="fca90-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="fca90-116">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fca90-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fca90-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="fca90-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="fca90-118">接收 Dispid 之陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="fca90-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="fca90-119">的每個專案都會收到一個識別碼，該識別碼對應至 *rgszNames* 參數中傳遞的其中一個名稱。</span><span class="sxs-lookup"><span data-stu-id="fca90-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fca90-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="fca90-120">Return value</span></span>

<span data-ttu-id="fca90-121">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fca90-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fca90-122">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="fca90-122">Possible values include the following.</span></span>



| <span data-ttu-id="fca90-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fca90-123">Return code</span></span>                                                                                         | <span data-ttu-id="fca90-124">Description</span><span class="sxs-lookup"><span data-stu-id="fca90-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="fca90-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fca90-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="fca90-126">成功。</span><span class="sxs-lookup"><span data-stu-id="fca90-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fca90-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fca90-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="fca90-128">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="fca90-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="fca90-129"><dt>**將 \_ 電子 \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="fca90-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="fca90-130">一或多個名稱未知。</span><span class="sxs-lookup"><span data-stu-id="fca90-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fca90-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fca90-131">Requirements</span></span>



| <span data-ttu-id="fca90-132">需求</span><span class="sxs-lookup"><span data-stu-id="fca90-132">Requirement</span></span> | <span data-ttu-id="fca90-133">值</span><span class="sxs-lookup"><span data-stu-id="fca90-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca90-134">標頭</span><span class="sxs-lookup"><span data-stu-id="fca90-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fca90-135"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fca90-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fca90-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="fca90-136">Library</span></span><br/> | <dl> <span data-ttu-id="fca90-137"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fca90-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fca90-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fca90-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca90-139">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="fca90-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




