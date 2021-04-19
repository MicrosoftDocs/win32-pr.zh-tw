---
description: GetTypeInfo 方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: 'CBaseDispatch. GetTypeInfo 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992919"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="ca58d-103">CBaseDispatch. GetTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ca58d-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="ca58d-104">`GetTypeInfo`方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="ca58d-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca58d-105">語法</span><span class="sxs-lookup"><span data-stu-id="ca58d-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="ca58d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ca58d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca58d-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="ca58d-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="ca58d-108">指定介面 (IID) 的介面識別碼參考。</span><span class="sxs-lookup"><span data-stu-id="ca58d-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ca58d-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="ca58d-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ca58d-110">要傳回的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="ca58d-110">Type information to return.</span></span> <span data-ttu-id="ca58d-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ca58d-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca58d-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="ca58d-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="ca58d-113">地區設定識別項。</span><span class="sxs-lookup"><span data-stu-id="ca58d-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ca58d-114">*>pptinfo*</span><span class="sxs-lookup"><span data-stu-id="ca58d-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ca58d-115">接收 **ITypeInfo** 指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="ca58d-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca58d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca58d-116">Return value</span></span>

<span data-ttu-id="ca58d-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ca58d-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ca58d-118">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="ca58d-118">Possible values include the following.</span></span>



| <span data-ttu-id="ca58d-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ca58d-119">Return code</span></span>                                                                                             | <span data-ttu-id="ca58d-120">Description</span><span class="sxs-lookup"><span data-stu-id="ca58d-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ca58d-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ca58d-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ca58d-122">成功。</span><span class="sxs-lookup"><span data-stu-id="ca58d-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="ca58d-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ca58d-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="ca58d-124">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="ca58d-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="ca58d-125"><dt>**輸入 \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="ca58d-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="ca58d-126">*Itinfo* 參數不是零。</span><span class="sxs-lookup"><span data-stu-id="ca58d-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca58d-127">備註</span><span class="sxs-lookup"><span data-stu-id="ca58d-127">Remarks</span></span>

<span data-ttu-id="ca58d-128">這個方法的行為類似于 **IDispatch：： GetTypeInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="ca58d-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="ca58d-129">不過，它還包含一個額外的 *參數，也* 就是指定要取得其型別資訊的介面。</span><span class="sxs-lookup"><span data-stu-id="ca58d-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca58d-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca58d-130">Requirements</span></span>



| <span data-ttu-id="ca58d-131">需求</span><span class="sxs-lookup"><span data-stu-id="ca58d-131">Requirement</span></span> | <span data-ttu-id="ca58d-132">值</span><span class="sxs-lookup"><span data-stu-id="ca58d-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca58d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="ca58d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ca58d-134"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ca58d-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca58d-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="ca58d-135">Library</span></span><br/> | <dl> <span data-ttu-id="ca58d-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ca58d-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca58d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca58d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca58d-138">**CBaseDispatch 類別**</span><span class="sxs-lookup"><span data-stu-id="ca58d-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




