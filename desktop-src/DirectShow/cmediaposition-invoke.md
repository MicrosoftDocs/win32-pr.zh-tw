---
description: Invoke 方法可讓您存取物件所公開的屬性和方法。
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: 'CMediaPosition： Invoke 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001177"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="985c7-103">CMediaPosition 方法</span><span class="sxs-lookup"><span data-stu-id="985c7-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="985c7-104">`Invoke`方法可讓您存取物件所公開的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="985c7-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="985c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="985c7-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="985c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="985c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985c7-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="985c7-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-108">成員的識別碼。</span><span class="sxs-lookup"><span data-stu-id="985c7-108">Identifier of the member.</span></span> <span data-ttu-id="985c7-109">使用 [**CMediaPosition：： GetIDsOfNames**](cmediaposition-getidsofnames.md) 取得分派識別碼。</span><span class="sxs-lookup"><span data-stu-id="985c7-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="985c7-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-111">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="985c7-111">Reserved for future use.</span></span> <span data-ttu-id="985c7-112">必須是 IID \_ Null。</span><span class="sxs-lookup"><span data-stu-id="985c7-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="985c7-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-114">要在其中解讀引數的地區設定內容。</span><span class="sxs-lookup"><span data-stu-id="985c7-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="985c7-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-116">描述呼叫之內容的旗標。</span><span class="sxs-lookup"><span data-stu-id="985c7-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="985c7-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-118">**DIPPARAMS** 結構的指標，其中包含引數。</span><span class="sxs-lookup"><span data-stu-id="985c7-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="985c7-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-120">接收結果之 **變異** 的指標，如果呼叫端不需要任何結果，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="985c7-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="985c7-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-122">接收例外狀況資訊之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="985c7-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="985c7-123">*>puargerr*</span><span class="sxs-lookup"><span data-stu-id="985c7-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="985c7-124">變數的指標，此變數會接收導致錯誤之第一個引數的索引。</span><span class="sxs-lookup"><span data-stu-id="985c7-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985c7-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="985c7-125">Return value</span></span>

<span data-ttu-id="985c7-126">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="985c7-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="985c7-127">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="985c7-127">Possible values include the following.</span></span>



| <span data-ttu-id="985c7-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="985c7-128">Return code</span></span>                                                                                              | <span data-ttu-id="985c7-129">Description</span><span class="sxs-lookup"><span data-stu-id="985c7-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="985c7-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="985c7-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="985c7-131">成功。</span><span class="sxs-lookup"><span data-stu-id="985c7-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="985c7-132"><dt>**將 \_ 電子 \_ UNKNOWNINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="985c7-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="985c7-133">*Riid* 參數不是 IID \_ Null</span><span class="sxs-lookup"><span data-stu-id="985c7-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="985c7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="985c7-134">Requirements</span></span>



| <span data-ttu-id="985c7-135">需求</span><span class="sxs-lookup"><span data-stu-id="985c7-135">Requirement</span></span> | <span data-ttu-id="985c7-136">值</span><span class="sxs-lookup"><span data-stu-id="985c7-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985c7-137">標頭</span><span class="sxs-lookup"><span data-stu-id="985c7-137">Header</span></span><br/>  | <dl> <span data-ttu-id="985c7-138"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="985c7-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="985c7-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="985c7-139">Library</span></span><br/> | <dl> <span data-ttu-id="985c7-140"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="985c7-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985c7-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="985c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985c7-142">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="985c7-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




