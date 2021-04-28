---
description: CMediaPosition. GetTypeInfo 方法-GetTypeInfo 方法會抓取物件的型別資訊，然後用它來取得介面的型別資訊。
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
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099136"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="068f5-103">CMediaPosition. GetTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="068f5-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="068f5-104">`GetTypeInfo`方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="068f5-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="068f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="068f5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="068f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="068f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068f5-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="068f5-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="068f5-108">要傳回的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="068f5-108">Type information to return.</span></span> <span data-ttu-id="068f5-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="068f5-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="068f5-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="068f5-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="068f5-111">地區設定識別項。</span><span class="sxs-lookup"><span data-stu-id="068f5-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="068f5-112">*>pptinfo*</span><span class="sxs-lookup"><span data-stu-id="068f5-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="068f5-113">接收 **ITypeInfo** 指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="068f5-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068f5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="068f5-114">Return value</span></span>

<span data-ttu-id="068f5-115">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="068f5-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="068f5-116">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="068f5-116">Possible values include the following.</span></span>



| <span data-ttu-id="068f5-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="068f5-117">Return code</span></span>                                                                                             | <span data-ttu-id="068f5-118">Description</span><span class="sxs-lookup"><span data-stu-id="068f5-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="068f5-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="068f5-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="068f5-120">成功。</span><span class="sxs-lookup"><span data-stu-id="068f5-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="068f5-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="068f5-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="068f5-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="068f5-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="068f5-123"><dt>**輸入 \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="068f5-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="068f5-124">*Itinfo* 參數不是零。</span><span class="sxs-lookup"><span data-stu-id="068f5-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="068f5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="068f5-125">Requirements</span></span>



| <span data-ttu-id="068f5-126">需求</span><span class="sxs-lookup"><span data-stu-id="068f5-126">Requirement</span></span> | <span data-ttu-id="068f5-127">值</span><span class="sxs-lookup"><span data-stu-id="068f5-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="068f5-128">標頭</span><span class="sxs-lookup"><span data-stu-id="068f5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="068f5-129"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="068f5-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="068f5-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="068f5-130">Library</span></span><br/> | <dl> <span data-ttu-id="068f5-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="068f5-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068f5-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="068f5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068f5-133">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="068f5-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




