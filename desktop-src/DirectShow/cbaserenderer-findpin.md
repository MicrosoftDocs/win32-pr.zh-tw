---
description: FindPin 方法會使用指定的識別碼抓取 pin。
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: 'CBaseRenderer. FindPin 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994755"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="f2c1c-103">CBaseRenderer. FindPin 方法</span><span class="sxs-lookup"><span data-stu-id="f2c1c-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="f2c1c-104">`FindPin`方法會使用指定的識別碼抓取 pin。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2c1c-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="f2c1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c1c-107">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="f2c1c-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c1c-108">常數、以 null 結尾的寬字元字串的指標，可識別 pin。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="f2c1c-109">必須是 L "In"。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="f2c1c-110">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="f2c1c-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f2c1c-111">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="f2c1c-112">如果方法失敗， *\* ppPin* 會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c1c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2c1c-113">Return value</span></span>

<span data-ttu-id="f2c1c-114">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f2c1c-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f2c1c-115">Return code</span></span>                                                                                       | <span data-ttu-id="f2c1c-116">Description</span><span class="sxs-lookup"><span data-stu-id="f2c1c-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f2c1c-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1c-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="f2c1c-118">成功。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f2c1c-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1c-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="f2c1c-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="f2c1c-121"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1c-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f2c1c-122">找不到。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="f2c1c-123">備註</span><span class="sxs-lookup"><span data-stu-id="f2c1c-123">Remarks</span></span>

<span data-ttu-id="f2c1c-124">這個方法會覆寫 [**CBaseFilter：： FindPin**](cbasefilter-findpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="f2c1c-125">篩選器的唯一 pin (輸入 pin) 名稱為 "In"。</span><span class="sxs-lookup"><span data-stu-id="f2c1c-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c1c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2c1c-126">Requirements</span></span>



| <span data-ttu-id="f2c1c-127">需求</span><span class="sxs-lookup"><span data-stu-id="f2c1c-127">Requirement</span></span> | <span data-ttu-id="f2c1c-128">值</span><span class="sxs-lookup"><span data-stu-id="f2c1c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c1c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f2c1c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f2c1c-130"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f2c1c-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2c1c-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2c1c-131">Library</span></span><br/> | <dl> <span data-ttu-id="f2c1c-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f2c1c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2c1c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2c1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c1c-134">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="f2c1c-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




