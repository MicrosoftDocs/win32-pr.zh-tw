---
description: CBaseDispatch. GetTypeInfo 方法-GetTypeInfo 方法會抓取物件的型別資訊，然後用它來取得介面的型別資訊。
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
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120116"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="aff43-103">CBaseDispatch. GetTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="aff43-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="aff43-104">`GetTypeInfo`方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="aff43-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff43-105">語法</span><span class="sxs-lookup"><span data-stu-id="aff43-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="aff43-106">參數</span><span class="sxs-lookup"><span data-stu-id="aff43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff43-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="aff43-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="aff43-108">指定介面 (IID) 的介面識別碼參考。</span><span class="sxs-lookup"><span data-stu-id="aff43-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="aff43-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="aff43-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="aff43-110">要傳回的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="aff43-110">Type information to return.</span></span> <span data-ttu-id="aff43-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="aff43-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aff43-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="aff43-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="aff43-113">地區設定識別項。</span><span class="sxs-lookup"><span data-stu-id="aff43-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="aff43-114">*>pptinfo*</span><span class="sxs-lookup"><span data-stu-id="aff43-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="aff43-115">接收 **ITypeInfo** 指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="aff43-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff43-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="aff43-116">Return value</span></span>

<span data-ttu-id="aff43-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="aff43-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="aff43-118">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="aff43-118">Possible values include the following.</span></span>



| <span data-ttu-id="aff43-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aff43-119">Return code</span></span>                                                                                             | <span data-ttu-id="aff43-120">Description</span><span class="sxs-lookup"><span data-stu-id="aff43-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="aff43-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="aff43-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="aff43-122">成功。</span><span class="sxs-lookup"><span data-stu-id="aff43-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="aff43-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="aff43-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="aff43-124">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="aff43-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="aff43-125"><dt>**輸入 \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="aff43-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="aff43-126">*Itinfo* 參數不是零。</span><span class="sxs-lookup"><span data-stu-id="aff43-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aff43-127">備註</span><span class="sxs-lookup"><span data-stu-id="aff43-127">Remarks</span></span>

<span data-ttu-id="aff43-128">這個方法的行為類似于 **IDispatch：： GetTypeInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="aff43-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="aff43-129">不過，它還包含一個額外的 *參數，也* 就是指定要取得其型別資訊的介面。</span><span class="sxs-lookup"><span data-stu-id="aff43-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff43-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="aff43-130">Requirements</span></span>



| <span data-ttu-id="aff43-131">需求</span><span class="sxs-lookup"><span data-stu-id="aff43-131">Requirement</span></span> | <span data-ttu-id="aff43-132">值</span><span class="sxs-lookup"><span data-stu-id="aff43-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff43-133">標頭</span><span class="sxs-lookup"><span data-stu-id="aff43-133">Header</span></span><br/>  | <dl> <span data-ttu-id="aff43-134"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="aff43-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aff43-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="aff43-135">Library</span></span><br/> | <dl> <span data-ttu-id="aff43-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="aff43-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff43-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aff43-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff43-138">**CBaseDispatch 類別**</span><span class="sxs-lookup"><span data-stu-id="aff43-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




