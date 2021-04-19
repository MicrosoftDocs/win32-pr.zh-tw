---
description: GetTypeInfo 方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: 'CMediaPosition. GetTypeInfo 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000438"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="238f7-103">CMediaPosition. GetTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="238f7-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="238f7-104">`GetTypeInfo`方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="238f7-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="238f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="238f7-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="238f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="238f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238f7-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="238f7-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="238f7-108">要傳回的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="238f7-108">Type information to return.</span></span> <span data-ttu-id="238f7-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="238f7-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="238f7-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="238f7-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="238f7-111">地區設定識別項。</span><span class="sxs-lookup"><span data-stu-id="238f7-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="238f7-112">*>pptinfo*</span><span class="sxs-lookup"><span data-stu-id="238f7-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="238f7-113">接收 **ITypeInfo** 指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="238f7-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238f7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="238f7-114">Return value</span></span>

<span data-ttu-id="238f7-115">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="238f7-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="238f7-116">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="238f7-116">Possible values include the following.</span></span>



| <span data-ttu-id="238f7-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="238f7-117">Return code</span></span>                                                                                             | <span data-ttu-id="238f7-118">Description</span><span class="sxs-lookup"><span data-stu-id="238f7-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="238f7-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="238f7-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="238f7-120">成功。</span><span class="sxs-lookup"><span data-stu-id="238f7-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="238f7-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="238f7-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="238f7-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="238f7-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="238f7-123"><dt>**輸入 \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="238f7-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="238f7-124">*Itinfo* 參數不是零。</span><span class="sxs-lookup"><span data-stu-id="238f7-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="238f7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="238f7-125">Requirements</span></span>



| <span data-ttu-id="238f7-126">需求</span><span class="sxs-lookup"><span data-stu-id="238f7-126">Requirement</span></span> | <span data-ttu-id="238f7-127">值</span><span class="sxs-lookup"><span data-stu-id="238f7-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="238f7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="238f7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="238f7-129"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="238f7-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="238f7-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="238f7-130">Library</span></span><br/> | <dl> <span data-ttu-id="238f7-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="238f7-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="238f7-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="238f7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238f7-133">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="238f7-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




