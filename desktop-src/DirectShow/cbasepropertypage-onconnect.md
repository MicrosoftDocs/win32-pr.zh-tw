---
description: OnConnect 方法會提供 IUnknown 指標給與屬性頁相關聯的物件。
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: 'CBasePropertyPage. OnConnect 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984431"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="260d1-103">CBasePropertyPage. OnConnect 方法</span><span class="sxs-lookup"><span data-stu-id="260d1-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="260d1-104">`OnConnect`方法會提供 **IUnknown** 指標給與屬性頁相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="260d1-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="260d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="260d1-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="260d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="260d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="260d1-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="260d1-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="260d1-108">物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="260d1-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="260d1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="260d1-109">Return value</span></span>

<span data-ttu-id="260d1-110">基底類別執行會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="260d1-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="260d1-111">備註</span><span class="sxs-lookup"><span data-stu-id="260d1-111">Remarks</span></span>

<span data-ttu-id="260d1-112">[**CBasePropertyPage：： SetObjects**](cbasepropertypage-setobjects.md)方法會呼叫 `OnConnect` 方法。</span><span class="sxs-lookup"><span data-stu-id="260d1-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="260d1-113">覆寫這個方法，將指標儲存至 *pUnknown* 所指定的物件。</span><span class="sxs-lookup"><span data-stu-id="260d1-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="260d1-114">您可以儲存 *pUnknown* 指標本身，或針對其他介面查詢該指標。</span><span class="sxs-lookup"><span data-stu-id="260d1-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="260d1-115">如果您儲存 *pUnknown* 指標，請在傳回之前呼叫 **AddRef** `OnConnect` 。</span><span class="sxs-lookup"><span data-stu-id="260d1-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="260d1-116">在 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md) 方法中，使用儲存的指標 (或指標) 來取得對話屬性的初始值。</span><span class="sxs-lookup"><span data-stu-id="260d1-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="260d1-117">在 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md) 方法中，將任何變更套用回物件。</span><span class="sxs-lookup"><span data-stu-id="260d1-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="260d1-118">釋放 [**CBasePropertyPage：： OnDisconnect**](cbasepropertypage-ondisconnect.md) 方法中的所有指標。</span><span class="sxs-lookup"><span data-stu-id="260d1-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="260d1-119">範例</span><span class="sxs-lookup"><span data-stu-id="260d1-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="260d1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="260d1-120">Requirements</span></span>



| <span data-ttu-id="260d1-121">需求</span><span class="sxs-lookup"><span data-stu-id="260d1-121">Requirement</span></span> | <span data-ttu-id="260d1-122">值</span><span class="sxs-lookup"><span data-stu-id="260d1-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="260d1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="260d1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="260d1-124"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="260d1-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="260d1-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="260d1-125">Library</span></span><br/> | <dl> <span data-ttu-id="260d1-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="260d1-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="260d1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="260d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260d1-128">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="260d1-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




