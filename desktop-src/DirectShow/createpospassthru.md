---
description: CreatePosPassThru 函數會建立 CPosPassThru 物件或 CRendererPosPassThru 物件。
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: 'CreatePosPassThru 函式 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981655"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="686da-103">CreatePosPassThru 函式</span><span class="sxs-lookup"><span data-stu-id="686da-103">CreatePosPassThru function</span></span>

<span data-ttu-id="686da-104">`CreatePosPassThru`函數會建立 [**CPosPassThru**](cpospassthru.md)物件或 [**CRendererPosPassThru**](crendererpospassthru.md)物件。</span><span class="sxs-lookup"><span data-stu-id="686da-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="686da-105">語法</span><span class="sxs-lookup"><span data-stu-id="686da-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="686da-106">參數</span><span class="sxs-lookup"><span data-stu-id="686da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="686da-107">*pAgg*</span><span class="sxs-lookup"><span data-stu-id="686da-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="686da-108">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="686da-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="686da-109">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="686da-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="686da-110">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="686da-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="686da-111">*bRenderer*</span><span class="sxs-lookup"><span data-stu-id="686da-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="686da-112">指定篩選是否為轉譯器的布林值。</span><span class="sxs-lookup"><span data-stu-id="686da-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="686da-113">如果篩選器是轉譯器，請使用 **TRUE** 值，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="686da-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="686da-114">如果值為 **TRUE**，這個方法會建立 [**CRendererPosPassThru**](crendererpospassthru.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="686da-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="686da-115">如果值為 **FALSE**，則方法會建立 **CPosPassThru** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="686da-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="686da-116">*pPin*</span><span class="sxs-lookup"><span data-stu-id="686da-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="686da-117">篩選器輸入釘選上 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="686da-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="686da-118">*ppPassThru*</span><span class="sxs-lookup"><span data-stu-id="686da-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="686da-119">接收物件的 **IUnknown** 介面指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="686da-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="686da-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="686da-120">Return value</span></span>

<span data-ttu-id="686da-121">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="686da-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="686da-122">否則，會傳回 **HRESULT** 值，指出錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="686da-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="686da-123">備註</span><span class="sxs-lookup"><span data-stu-id="686da-123">Remarks</span></span>

<span data-ttu-id="686da-124">這個方法會使用 [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) 介面來建立物件。</span><span class="sxs-lookup"><span data-stu-id="686da-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="686da-125">物件是從 Quartz.dll 動態載入的。</span><span class="sxs-lookup"><span data-stu-id="686da-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="686da-126">如果函式成功，則傳回的 **IUnknown** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="686da-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="686da-127">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="686da-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="686da-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="686da-128">Requirements</span></span>



| <span data-ttu-id="686da-129">需求</span><span class="sxs-lookup"><span data-stu-id="686da-129">Requirement</span></span> | <span data-ttu-id="686da-130">值</span><span class="sxs-lookup"><span data-stu-id="686da-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="686da-131">標頭</span><span class="sxs-lookup"><span data-stu-id="686da-131">Header</span></span><br/>  | <dl> <span data-ttu-id="686da-132"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="686da-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="686da-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="686da-133">Library</span></span><br/> | <dl> <span data-ttu-id="686da-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="686da-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686da-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="686da-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="686da-136">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="686da-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




