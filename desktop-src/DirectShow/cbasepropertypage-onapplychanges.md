---
description: 當使用者將變更套用至屬性頁時，會呼叫 OnApplyChanges 方法。
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: 'CBasePropertyPage. OnApplyChanges 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976236"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="12394-103">CBasePropertyPage. OnApplyChanges 方法</span><span class="sxs-lookup"><span data-stu-id="12394-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="12394-104">`OnApplyChanges`當使用者將變更套用至屬性頁時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="12394-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="12394-105">語法</span><span class="sxs-lookup"><span data-stu-id="12394-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="12394-106">參數</span><span class="sxs-lookup"><span data-stu-id="12394-106">Parameters</span></span>

<span data-ttu-id="12394-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="12394-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12394-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="12394-108">Return value</span></span>

<span data-ttu-id="12394-109">基底類別執行會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="12394-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="12394-110">備註</span><span class="sxs-lookup"><span data-stu-id="12394-110">Remarks</span></span>

<span data-ttu-id="12394-111">[](cbasepropertypage-apply.md) `OnApplyChanges` 如果 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md)旗標為 **TRUE**，則 CBasePropertyPage：： Apply 方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="12394-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="12394-112">覆寫 `OnApplyChanges` 以處理變更，並將 **m \_ bDirty** 重設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="12394-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="12394-113">範例</span><span class="sxs-lookup"><span data-stu-id="12394-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="12394-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="12394-114">Requirements</span></span>



| <span data-ttu-id="12394-115">需求</span><span class="sxs-lookup"><span data-stu-id="12394-115">Requirement</span></span> | <span data-ttu-id="12394-116">值</span><span class="sxs-lookup"><span data-stu-id="12394-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12394-117">標頭</span><span class="sxs-lookup"><span data-stu-id="12394-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12394-118"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12394-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="12394-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="12394-119">Library</span></span><br/> | <dl> <span data-ttu-id="12394-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12394-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12394-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12394-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12394-122">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="12394-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




