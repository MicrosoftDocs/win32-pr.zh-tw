---
description: GetAllocatorRequirements 方法會抓取 pin 所要求的配置器屬性。 這個方法會實 IMemInputPin：： GetAllocatorRequirements 方法。
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: 'CTransInPlaceInputPin. GetAllocatorRequirements 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001920"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a><span data-ttu-id="7b636-104">CTransInPlaceInputPin. GetAllocatorRequirements 方法</span><span class="sxs-lookup"><span data-stu-id="7b636-104">CTransInPlaceInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="7b636-105">方法會抓取 `GetAllocatorRequirements` pin 所要求的配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="7b636-105">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the pin.</span></span> <span data-ttu-id="7b636-106">這個方法會實 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) 方法。</span><span class="sxs-lookup"><span data-stu-id="7b636-106">This method implements the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b636-107">語法</span><span class="sxs-lookup"><span data-stu-id="7b636-107">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="7b636-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b636-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b636-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="7b636-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="7b636-110">配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，該結構會填入需求。</span><span class="sxs-lookup"><span data-stu-id="7b636-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b636-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b636-111">Return value</span></span>

<span data-ttu-id="7b636-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7b636-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7b636-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="7b636-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7b636-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7b636-114">Return code</span></span>                                                                               | <span data-ttu-id="7b636-115">Description</span><span class="sxs-lookup"><span data-stu-id="7b636-115">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b636-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7b636-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7b636-117">Success</span><span class="sxs-lookup"><span data-stu-id="7b636-117">Success</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="7b636-118"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b636-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="7b636-119">輸出針腳未連接，或下游輸入 pin 不支援方法。</span><span class="sxs-lookup"><span data-stu-id="7b636-119">The output pin is not connected, or the downstream input pin does not support the method.</span></span><br/> |
| <dl> <span data-ttu-id="7b636-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="7b636-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7b636-121">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="7b636-121">**NULL** pointer argument</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="7b636-122">備註</span><span class="sxs-lookup"><span data-stu-id="7b636-122">Remarks</span></span>

<span data-ttu-id="7b636-123">如果輸出連接已連線，這個方法會將呼叫傳遞給下游輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="7b636-123">If the output pin is connected, this method passes the call to the downstream input pin.</span></span> <span data-ttu-id="7b636-124">否則，它會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="7b636-124">Otherwise, it returns E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b636-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b636-125">Requirements</span></span>



| <span data-ttu-id="7b636-126">需求</span><span class="sxs-lookup"><span data-stu-id="7b636-126">Requirement</span></span> | <span data-ttu-id="7b636-127">值</span><span class="sxs-lookup"><span data-stu-id="7b636-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b636-128">標頭</span><span class="sxs-lookup"><span data-stu-id="7b636-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7b636-129"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7b636-129"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b636-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b636-130">Library</span></span><br/> | <dl> <span data-ttu-id="7b636-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7b636-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b636-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b636-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b636-133">**CTransInPlaceInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="7b636-133">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




