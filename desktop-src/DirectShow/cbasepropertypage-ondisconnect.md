---
description: 當屬性頁應該釋放相關聯的物件時，就會呼叫 OnDisconnect 方法。
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: 'CBasePropertyPage. OnDisconnect 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977158"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="6ff00-103">CBasePropertyPage. OnDisconnect 方法</span><span class="sxs-lookup"><span data-stu-id="6ff00-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="6ff00-104">`OnDisconnect`當屬性頁應該釋放相關聯的物件時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="6ff00-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff00-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ff00-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="6ff00-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ff00-106">Parameters</span></span>

<span data-ttu-id="6ff00-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6ff00-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ff00-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ff00-108">Return value</span></span>

<span data-ttu-id="6ff00-109">基底類別執行會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6ff00-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff00-110">備註</span><span class="sxs-lookup"><span data-stu-id="6ff00-110">Remarks</span></span>

<span data-ttu-id="6ff00-111">[**CBasePropertyPage：： SetObjects**](cbasepropertypage-setobjects.md)方法會呼叫 `OnDisconnect` 方法。</span><span class="sxs-lookup"><span data-stu-id="6ff00-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="6ff00-112">覆寫 `OnDisconnect` 以釋放在 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法中取得的任何指標。</span><span class="sxs-lookup"><span data-stu-id="6ff00-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6ff00-113">範例</span><span class="sxs-lookup"><span data-stu-id="6ff00-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="6ff00-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ff00-114">Requirements</span></span>



| <span data-ttu-id="6ff00-115">需求</span><span class="sxs-lookup"><span data-stu-id="6ff00-115">Requirement</span></span> | <span data-ttu-id="6ff00-116">值</span><span class="sxs-lookup"><span data-stu-id="6ff00-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff00-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6ff00-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6ff00-118"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6ff00-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6ff00-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ff00-119">Library</span></span><br/> | <dl> <span data-ttu-id="6ff00-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6ff00-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff00-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ff00-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff00-122">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="6ff00-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




