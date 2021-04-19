---
description: 函式方法。
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: 'CTransInPlaceFilter. CTransInPlaceFilter (Transip. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990821"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="8c78d-103">CTransInPlaceFilter. CTransInPlaceFilter 函數</span><span class="sxs-lookup"><span data-stu-id="8c78d-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="8c78d-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="8c78d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c78d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c78d-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="8c78d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c78d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c78d-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="8c78d-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="8c78d-108">包含篩選的偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="8c78d-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="8c78d-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="8c78d-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c78d-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="8c78d-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8c78d-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="8c78d-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="8c78d-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="8c78d-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="8c78d-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8c78d-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8c78d-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="8c78d-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="8c78d-115">篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c78d-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="8c78d-116">*phr*</span><span class="sxs-lookup"><span data-stu-id="8c78d-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8c78d-117">忽略。</span><span class="sxs-lookup"><span data-stu-id="8c78d-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="8c78d-118">*bModifiesData*</span><span class="sxs-lookup"><span data-stu-id="8c78d-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="8c78d-119">指定篩選是否修改輸入資料的布林值。</span><span class="sxs-lookup"><span data-stu-id="8c78d-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="8c78d-120">若 **為 TRUE**，則篩選準則會修改資料。</span><span class="sxs-lookup"><span data-stu-id="8c78d-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="8c78d-121">否則，篩選準則會將未變更的資料傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="8c78d-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c78d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c78d-122">Requirements</span></span>



| <span data-ttu-id="8c78d-123">需求</span><span class="sxs-lookup"><span data-stu-id="8c78d-123">Requirement</span></span> | <span data-ttu-id="8c78d-124">值</span><span class="sxs-lookup"><span data-stu-id="8c78d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c78d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8c78d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8c78d-126"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8c78d-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c78d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c78d-127">Library</span></span><br/> | <dl> <span data-ttu-id="8c78d-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8c78d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c78d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c78d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c78d-130">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="8c78d-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




