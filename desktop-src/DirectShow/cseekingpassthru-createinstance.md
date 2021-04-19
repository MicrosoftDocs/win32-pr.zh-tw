---
description: CreateInstance 方法會建立物件的實例。 這個方法支援透過 class factory 建立物件。 如需詳細資訊，請參閱 CFactoryTemplate。
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: CSeekingPassThru (Seekpt) 的 CreateInstance 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994687"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="6c42d-105">CSeekingPassThru CreateInstance 方法</span><span class="sxs-lookup"><span data-stu-id="6c42d-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="6c42d-106">`CreateInstance`方法會建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="6c42d-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="6c42d-107">這個方法支援透過 class factory 建立物件。</span><span class="sxs-lookup"><span data-stu-id="6c42d-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="6c42d-108">如需詳細資訊，請參閱 [**CFactoryTemplate**](cfactorytemplate.md)。</span><span class="sxs-lookup"><span data-stu-id="6c42d-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c42d-109">語法</span><span class="sxs-lookup"><span data-stu-id="6c42d-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6c42d-110">參數</span><span class="sxs-lookup"><span data-stu-id="6c42d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c42d-111">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="6c42d-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6c42d-112">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="6c42d-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="6c42d-113">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="6c42d-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6c42d-114">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6c42d-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6c42d-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="6c42d-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6c42d-116">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="6c42d-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6c42d-117">忽略。</span><span class="sxs-lookup"><span data-stu-id="6c42d-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c42d-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c42d-118">Return value</span></span>

<span data-ttu-id="6c42d-119">傳回新 **CSeekingPassThru** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6c42d-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c42d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c42d-120">Requirements</span></span>



| <span data-ttu-id="6c42d-121">需求</span><span class="sxs-lookup"><span data-stu-id="6c42d-121">Requirement</span></span> | <span data-ttu-id="6c42d-122">值</span><span class="sxs-lookup"><span data-stu-id="6c42d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c42d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6c42d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6c42d-124"><dt>Seekpt (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6c42d-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6c42d-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c42d-125">Library</span></span><br/> | <dl> <span data-ttu-id="6c42d-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6c42d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c42d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c42d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c42d-128">**CSeekingPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="6c42d-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




