---
description: SetObjects 方法會為與屬性頁相關聯的物件提供 IUnknown 指標。 這個方法會實 IPropertyPage：： SetObjects 方法。
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: 'CBasePropertyPage. SetObjects 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993439"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="67560-104">CBasePropertyPage. SetObjects 方法</span><span class="sxs-lookup"><span data-stu-id="67560-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="67560-105">`SetObjects`方法會為與屬性頁相關聯的物件提供 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="67560-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="67560-106">這個方法會實 **IPropertyPage：： SetObjects** 方法。</span><span class="sxs-lookup"><span data-stu-id="67560-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67560-107">語法</span><span class="sxs-lookup"><span data-stu-id="67560-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="67560-108">參數</span><span class="sxs-lookup"><span data-stu-id="67560-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67560-109">*cObjects*</span><span class="sxs-lookup"><span data-stu-id="67560-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="67560-110">指定 *ppUnk* 所指定陣列中的 **IUnknown** 指標數目。</span><span class="sxs-lookup"><span data-stu-id="67560-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="67560-111">*ppUnk*</span><span class="sxs-lookup"><span data-stu-id="67560-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="67560-112">指定 **IUnknown** 指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="67560-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67560-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="67560-113">Return value</span></span>

<span data-ttu-id="67560-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="67560-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="67560-115">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="67560-115">Possible values include the following.</span></span>



| <span data-ttu-id="67560-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="67560-116">Return code</span></span>                                                                                  | <span data-ttu-id="67560-117">Description</span><span class="sxs-lookup"><span data-stu-id="67560-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="67560-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="67560-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="67560-119">成功。</span><span class="sxs-lookup"><span data-stu-id="67560-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="67560-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="67560-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="67560-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="67560-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="67560-122"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="67560-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="67560-123">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="67560-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="67560-124">備註</span><span class="sxs-lookup"><span data-stu-id="67560-124">Remarks</span></span>

<span data-ttu-id="67560-125">雖然 *ppUnk* 會指定 **IUnknown** 指標的陣列，但 **CBasePropertyPage** 類別的設計只是為了支援一個相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="67560-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="67560-126">如果 *cObjects* 大於1，方法會傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="67560-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="67560-127">如果 *cObjects* 等於1，這個方法會呼叫 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="67560-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="67560-128">如果 *cObjects* 等於0，這個方法會呼叫 [**CBasePropertyPage：： OnDisconnect**](cbasepropertypage-ondisconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="67560-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="67560-129">衍生類別應該覆寫這兩種方法;如需詳細資訊，請參閱這些方法的備註。</span><span class="sxs-lookup"><span data-stu-id="67560-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="67560-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="67560-130">Requirements</span></span>



| <span data-ttu-id="67560-131">需求</span><span class="sxs-lookup"><span data-stu-id="67560-131">Requirement</span></span> | <span data-ttu-id="67560-132">值</span><span class="sxs-lookup"><span data-stu-id="67560-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67560-133">標頭</span><span class="sxs-lookup"><span data-stu-id="67560-133">Header</span></span><br/>  | <dl> <span data-ttu-id="67560-134"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="67560-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="67560-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="67560-135">Library</span></span><br/> | <dl> <span data-ttu-id="67560-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="67560-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67560-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67560-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67560-138">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="67560-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




