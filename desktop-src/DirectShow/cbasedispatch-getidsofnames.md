---
description: GetIDsOfNames 方法會將一組名稱對應至一組對應的 Dispid。
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: 'CBaseDispatch. GetIDsOfNames 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001500"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="0ca9d-103">CBaseDispatch. GetIDsOfNames 方法</span><span class="sxs-lookup"><span data-stu-id="0ca9d-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="0ca9d-104">方法會將 `GetIDsOfNames` 一組名稱對應至一組對應的 dispid。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca9d-105">語法</span><span class="sxs-lookup"><span data-stu-id="0ca9d-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="0ca9d-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ca9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca9d-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="0ca9d-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca9d-108">指定介面 (IID) 的介面識別碼參考。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="0ca9d-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="0ca9d-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca9d-110">寬字元字串陣列的位址，其中包含要對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="0ca9d-111">*Cname*</span><span class="sxs-lookup"><span data-stu-id="0ca9d-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca9d-112">*RgszNames* 參數所指定的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ca9d-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="0ca9d-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca9d-114">要在其中解讀名稱的地區設定內容。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="0ca9d-115">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ca9d-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="0ca9d-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca9d-117">接收 Dispid 之陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="0ca9d-118">的每個專案都會收到一個識別碼，該識別碼對應至 *rgszNames* 參數中傳遞的其中一個名稱。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca9d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ca9d-119">Return value</span></span>

<span data-ttu-id="0ca9d-120">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0ca9d-121">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-121">Possible values include the following.</span></span>



| <span data-ttu-id="0ca9d-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0ca9d-122">Return code</span></span>                                                                                         | <span data-ttu-id="0ca9d-123">Description</span><span class="sxs-lookup"><span data-stu-id="0ca9d-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="0ca9d-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0ca9d-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="0ca9d-125">成功。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0ca9d-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ca9d-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="0ca9d-127">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="0ca9d-128"><dt>**將 \_ 電子 \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="0ca9d-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="0ca9d-129">一或多個名稱未知。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ca9d-130">備註</span><span class="sxs-lookup"><span data-stu-id="0ca9d-130">Remarks</span></span>

<span data-ttu-id="0ca9d-131">這個方法的行為類似 **IDispatch：： GetIDsOfNames** 方法，但 *riid* 參數會指定要在其上取出 dispid 的介面。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="0ca9d-132">在 **IDispatch** 版本中 (，會保留 *riid* 參數。 ) </span><span class="sxs-lookup"><span data-stu-id="0ca9d-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="0ca9d-133">如果方法 \_ \_ 傳回了 UNKNOWNNAME，則傳回的 dispid 包含 \_ 每個對應至未知名稱之專案的 dispid 未知。</span><span class="sxs-lookup"><span data-stu-id="0ca9d-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca9d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ca9d-134">Requirements</span></span>



| <span data-ttu-id="0ca9d-135">需求</span><span class="sxs-lookup"><span data-stu-id="0ca9d-135">Requirement</span></span> | <span data-ttu-id="0ca9d-136">值</span><span class="sxs-lookup"><span data-stu-id="0ca9d-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca9d-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0ca9d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="0ca9d-138"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0ca9d-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ca9d-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ca9d-139">Library</span></span><br/> | <dl> <span data-ttu-id="0ca9d-140"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0ca9d-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca9d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ca9d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca9d-142">**CBaseDispatch 類別**</span><span class="sxs-lookup"><span data-stu-id="0ca9d-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




