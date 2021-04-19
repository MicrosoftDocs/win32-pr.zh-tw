---
description: Apply 方法會將目前的屬性頁值套用至與屬性頁相關聯的物件。 這個方法會實 IPropertyPage：： Apply 方法。
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: 'CBasePropertyPage 將方法套用 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994757"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="c3a57-104">CBasePropertyPage. Apply 方法</span><span class="sxs-lookup"><span data-stu-id="c3a57-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="c3a57-105">`Apply`方法會將目前的屬性頁值套用至與屬性頁相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="c3a57-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="c3a57-106">這個方法會實 **IPropertyPage：： Apply** 方法。</span><span class="sxs-lookup"><span data-stu-id="c3a57-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a57-107">語法</span><span class="sxs-lookup"><span data-stu-id="c3a57-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="c3a57-108">參數</span><span class="sxs-lookup"><span data-stu-id="c3a57-108">Parameters</span></span>

<span data-ttu-id="c3a57-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c3a57-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3a57-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3a57-110">Return value</span></span>

<span data-ttu-id="c3a57-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c3a57-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c3a57-112">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="c3a57-112">Possible values include the following.</span></span>



| <span data-ttu-id="c3a57-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c3a57-113">Return code</span></span>                                                                                  | <span data-ttu-id="c3a57-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3a57-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c3a57-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a57-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c3a57-116">成功。</span><span class="sxs-lookup"><span data-stu-id="c3a57-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="c3a57-117"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="c3a57-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c3a57-118">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="c3a57-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3a57-119">備註</span><span class="sxs-lookup"><span data-stu-id="c3a57-119">Remarks</span></span>

<span data-ttu-id="c3a57-120">如果 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md) 旗標為 **TRUE**，這個方法會呼叫 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c3a57-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="c3a57-121">覆寫 **OnApplyChanges** 以將變更套用至物件。</span><span class="sxs-lookup"><span data-stu-id="c3a57-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a57-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3a57-122">Requirements</span></span>



| <span data-ttu-id="c3a57-123">需求</span><span class="sxs-lookup"><span data-stu-id="c3a57-123">Requirement</span></span> | <span data-ttu-id="c3a57-124">值</span><span class="sxs-lookup"><span data-stu-id="c3a57-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a57-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c3a57-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c3a57-126"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c3a57-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c3a57-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3a57-127">Library</span></span><br/> | <dl> <span data-ttu-id="c3a57-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c3a57-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a57-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3a57-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a57-130">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="c3a57-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




