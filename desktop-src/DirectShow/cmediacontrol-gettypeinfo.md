---
description: 抓取類型資訊物件，此物件可以取得介面的類型資訊。
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: 'CMediaControl. GetTypeInfo 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe393922206744c23b534bf8d701d6292736c65a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998401"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="d71c3-103">CMediaControl. GetTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="d71c3-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="d71c3-104">抓取類型資訊物件，此物件可以取得介面的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="d71c3-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="d71c3-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="d71c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="d71c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d71c3-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="d71c3-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d71c3-108">要傳回的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="d71c3-108">Type information to return.</span></span> <span data-ttu-id="d71c3-109">傳遞零以取得 **IDispatch** 實作為的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="d71c3-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="d71c3-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="d71c3-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="d71c3-111">類型資訊的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="d71c3-111">Locale ID for the type information.</span></span> <span data-ttu-id="d71c3-112">針對支援當地語系化成員名稱的類別，物件可能會針對不同的語言傳回不同的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="d71c3-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="d71c3-113">對於不支援當地語系化成員名稱的類別，可以忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="d71c3-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d71c3-114">*>pptinfo*</span><span class="sxs-lookup"><span data-stu-id="d71c3-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d71c3-115">所要求之類型資訊物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="d71c3-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d71c3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d71c3-116">Return value</span></span>

<span data-ttu-id="d71c3-117">\_如果 *>pptinfo* 無效，則傳回 E 指標。</span><span class="sxs-lookup"><span data-stu-id="d71c3-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="d71c3-118">\_ \_ 如果 *itinfo* 不是零，則傳回型別 E ELEMENTNOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="d71c3-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="d71c3-119">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="d71c3-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="d71c3-120">否則，會傳回其中一個呼叫的 **HRESULT** ，以抓取型別。</span><span class="sxs-lookup"><span data-stu-id="d71c3-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d71c3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d71c3-121">Requirements</span></span>



| <span data-ttu-id="d71c3-122">需求</span><span class="sxs-lookup"><span data-stu-id="d71c3-122">Requirement</span></span> | <span data-ttu-id="d71c3-123">值</span><span class="sxs-lookup"><span data-stu-id="d71c3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d71c3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d71c3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d71c3-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d71c3-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d71c3-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d71c3-126">Library</span></span><br/> | <dl> <span data-ttu-id="d71c3-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d71c3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d71c3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d71c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71c3-129">**CMediaControl 類別**</span><span class="sxs-lookup"><span data-stu-id="d71c3-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




