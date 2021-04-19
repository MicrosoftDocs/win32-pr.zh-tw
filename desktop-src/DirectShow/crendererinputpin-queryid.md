---
description: QueryId 方法會抓取 pin 識別碼。 這個方法會覆寫 CBasePin：： QueryId 方法。
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: 'CRendererInputPin. QueryId 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b56ae2a846b4d89da4c6a9d4c8f88bd3094c5cff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984874"
---
# <a name="crendererinputpinqueryid-method"></a><span data-ttu-id="442fa-104">CRendererInputPin. QueryId 方法</span><span class="sxs-lookup"><span data-stu-id="442fa-104">CRendererInputPin.QueryId method</span></span>

<span data-ttu-id="442fa-105">方法會抓取 `QueryId` pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="442fa-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="442fa-106">這個方法會覆寫 [**CBasePin：： QueryId**](cbasepin-queryid.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="442fa-106">This method overrides the [**CBasePin::QueryId**](cbasepin-queryid.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="442fa-107">語法</span><span class="sxs-lookup"><span data-stu-id="442fa-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="442fa-108">參數</span><span class="sxs-lookup"><span data-stu-id="442fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442fa-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="442fa-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="442fa-110">接收包含 pin 識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="442fa-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="442fa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="442fa-111">Return value</span></span>

<span data-ttu-id="442fa-112">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="442fa-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="442fa-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="442fa-113">Return code</span></span>                                                                                   | <span data-ttu-id="442fa-114">Description</span><span class="sxs-lookup"><span data-stu-id="442fa-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="442fa-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="442fa-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="442fa-116">Success</span><span class="sxs-lookup"><span data-stu-id="442fa-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="442fa-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="442fa-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="442fa-118">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="442fa-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="442fa-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="442fa-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="442fa-120">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="442fa-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="442fa-121">備註</span><span class="sxs-lookup"><span data-stu-id="442fa-121">Remarks</span></span>

<span data-ttu-id="442fa-122">這個方法會配置 "In" 的寬字元字串，並將它指派給 *Id* 參數。</span><span class="sxs-lookup"><span data-stu-id="442fa-122">This method allocates the wide-character string "In" and assigns it to the *Id* parameter.</span></span> <span data-ttu-id="442fa-123">呼叫端必須使用 **CoTaskMemFree** 函式釋放已配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="442fa-123">The caller must free the allocated memory, using the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="442fa-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="442fa-124">Requirements</span></span>



| <span data-ttu-id="442fa-125">需求</span><span class="sxs-lookup"><span data-stu-id="442fa-125">Requirement</span></span> | <span data-ttu-id="442fa-126">值</span><span class="sxs-lookup"><span data-stu-id="442fa-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="442fa-127">標頭</span><span class="sxs-lookup"><span data-stu-id="442fa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="442fa-128"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="442fa-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="442fa-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="442fa-129">Library</span></span><br/> | <dl> <span data-ttu-id="442fa-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="442fa-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="442fa-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="442fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442fa-132">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="442fa-132">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




