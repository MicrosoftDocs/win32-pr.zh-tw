---
description: 函式方法。
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: 'CTransformFilter. CTransformFilter (Transfrm. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987166"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="48c45-103">CTransformFilter. CTransformFilter 函數</span><span class="sxs-lookup"><span data-stu-id="48c45-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="48c45-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="48c45-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c45-105">語法</span><span class="sxs-lookup"><span data-stu-id="48c45-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="48c45-106">參數</span><span class="sxs-lookup"><span data-stu-id="48c45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c45-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="48c45-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="48c45-108">包含篩選的偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="48c45-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="48c45-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="48c45-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="48c45-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="48c45-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="48c45-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="48c45-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="48c45-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="48c45-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="48c45-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="48c45-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48c45-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="48c45-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="48c45-115">篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="48c45-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48c45-116">備註</span><span class="sxs-lookup"><span data-stu-id="48c45-116">Remarks</span></span>

<span data-ttu-id="48c45-117">此函式不會建立篩選器的釘選。</span><span class="sxs-lookup"><span data-stu-id="48c45-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="48c45-118">這是在第一次呼叫 [**GetPin**](ctransformfilter-getpin.md) 方法期間發生的。</span><span class="sxs-lookup"><span data-stu-id="48c45-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="48c45-119">此函數會將 [**m \_ pInput**](ctransformfilter-m-pinput.md) 和 [**m \_ POutput**](ctransformfilter-m-poutput.md) 成員變數初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="48c45-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c45-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="48c45-120">Requirements</span></span>



| <span data-ttu-id="48c45-121">需求</span><span class="sxs-lookup"><span data-stu-id="48c45-121">Requirement</span></span> | <span data-ttu-id="48c45-122">值</span><span class="sxs-lookup"><span data-stu-id="48c45-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c45-123">標頭</span><span class="sxs-lookup"><span data-stu-id="48c45-123">Header</span></span><br/>  | <dl> <span data-ttu-id="48c45-124"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="48c45-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48c45-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="48c45-125">Library</span></span><br/> | <dl> <span data-ttu-id="48c45-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="48c45-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c45-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48c45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c45-128">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="48c45-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




