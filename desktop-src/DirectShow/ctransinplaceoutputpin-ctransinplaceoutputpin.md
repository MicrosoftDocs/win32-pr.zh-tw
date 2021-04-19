---
description: 函式方法。
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: 'CTransInPlaceOutputPin. CTransInPlaceOutputPin (Transip. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2c9ca668d3780ece082f9cab55db8406af7ad3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989533"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a><span data-ttu-id="ed2c6-103">CTransInPlaceOutputPin. CTransInPlaceOutputPin 函數</span><span class="sxs-lookup"><span data-stu-id="ed2c6-103">CTransInPlaceOutputPin.CTransInPlaceOutputPin constructor</span></span>

<span data-ttu-id="ed2c6-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed2c6-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="ed2c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed2c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed2c6-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="ed2c6-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="ed2c6-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-108">String containing the debug name of the object.</span></span> <span data-ttu-id="ed2c6-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed2c6-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ed2c6-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ed2c6-111">建立此 pin 之篩選準則的指標，其必須是 [**CTransInPlaceFilter**](ctransinplacefilter.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ed2c6-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="ed2c6-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ed2c6-113">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="ed2c6-114">在建立物件之前，將值初始化為「 \_ 確定」。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="ed2c6-115">只有在發生錯誤時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="ed2c6-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="ed2c6-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ed2c6-117">包含 pin 名稱的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed2c6-118">備註</span><span class="sxs-lookup"><span data-stu-id="ed2c6-118">Remarks</span></span>

<span data-ttu-id="ed2c6-119">*PName* 參數會指定 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)方法所傳回的 pin 名稱。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="ed2c6-120">不過，此字串不會用於 pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="ed2c6-121">此類別的 pin 識別碼一律為 "Out"。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="ed2c6-122">如需詳細資訊，請參閱 [**QueryId**](ctransforminputpin-queryid.md)。</span><span class="sxs-lookup"><span data-stu-id="ed2c6-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2c6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed2c6-123">Requirements</span></span>



| <span data-ttu-id="ed2c6-124">需求</span><span class="sxs-lookup"><span data-stu-id="ed2c6-124">Requirement</span></span> | <span data-ttu-id="ed2c6-125">值</span><span class="sxs-lookup"><span data-stu-id="ed2c6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2c6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ed2c6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ed2c6-127"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ed2c6-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed2c6-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed2c6-128">Library</span></span><br/> | <dl> <span data-ttu-id="ed2c6-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed2c6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed2c6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed2c6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2c6-131">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="ed2c6-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




