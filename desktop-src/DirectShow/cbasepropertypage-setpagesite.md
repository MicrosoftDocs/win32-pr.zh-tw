---
description: SetPageSite 方法會初始化屬性頁，並提供屬性框架的 IPropertyPageSite 介面指標。 這個方法會實 IPropertyPage：： SetPageSite 方法。
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: 'CBasePropertyPage. SetPageSite 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999126"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="c34be-104">CBasePropertyPage. SetPageSite 方法</span><span class="sxs-lookup"><span data-stu-id="c34be-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="c34be-105">`SetPageSite`方法會初始化屬性頁，並提供屬性框架 **IPropertyPageSite** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c34be-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="c34be-106">這個方法會實 **IPropertyPage：： SetPageSite** 方法。</span><span class="sxs-lookup"><span data-stu-id="c34be-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34be-107">語法</span><span class="sxs-lookup"><span data-stu-id="c34be-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="c34be-108">參數</span><span class="sxs-lookup"><span data-stu-id="c34be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34be-109">*pPageSite*</span><span class="sxs-lookup"><span data-stu-id="c34be-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="c34be-110">**IPropertyPageSite** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c34be-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34be-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c34be-111">Return value</span></span>

<span data-ttu-id="c34be-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c34be-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c34be-113">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="c34be-113">Possible values include the following.</span></span>



| <span data-ttu-id="c34be-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c34be-114">Return code</span></span>                                                                                  | <span data-ttu-id="c34be-115">Description</span><span class="sxs-lookup"><span data-stu-id="c34be-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="c34be-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c34be-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c34be-117">成功。</span><span class="sxs-lookup"><span data-stu-id="c34be-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="c34be-118"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="c34be-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="c34be-119">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="c34be-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c34be-120">備註</span><span class="sxs-lookup"><span data-stu-id="c34be-120">Remarks</span></span>

<span data-ttu-id="c34be-121">方法會將 *pPageSite* 指標儲存在 [**CBasePropertyPage：： m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="c34be-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c34be-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c34be-122">Requirements</span></span>



| <span data-ttu-id="c34be-123">需求</span><span class="sxs-lookup"><span data-stu-id="c34be-123">Requirement</span></span> | <span data-ttu-id="c34be-124">值</span><span class="sxs-lookup"><span data-stu-id="c34be-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c34be-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c34be-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c34be-126"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c34be-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c34be-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="c34be-127">Library</span></span><br/> | <dl> <span data-ttu-id="c34be-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c34be-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34be-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c34be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34be-130">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="c34be-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




