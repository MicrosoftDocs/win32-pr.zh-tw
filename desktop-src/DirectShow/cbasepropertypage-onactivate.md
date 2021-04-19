---
description: 當屬性頁啟用時，會呼叫 OnActivate 方法。
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: 'CBasePropertyPage. OnActivate 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983084"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="97c78-103">CBasePropertyPage. OnActivate 方法</span><span class="sxs-lookup"><span data-stu-id="97c78-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="97c78-104">`OnActivate`當屬性頁啟用時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="97c78-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c78-105">語法</span><span class="sxs-lookup"><span data-stu-id="97c78-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="97c78-106">參數</span><span class="sxs-lookup"><span data-stu-id="97c78-106">Parameters</span></span>

<span data-ttu-id="97c78-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="97c78-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97c78-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="97c78-108">Return value</span></span>

<span data-ttu-id="97c78-109">基底類別執行會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="97c78-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c78-110">備註</span><span class="sxs-lookup"><span data-stu-id="97c78-110">Remarks</span></span>

<span data-ttu-id="97c78-111">[**CBasePropertyPage：： Activate**](cbasepropertypage-activate.md)方法會呼叫 `OnActivate` 方法。</span><span class="sxs-lookup"><span data-stu-id="97c78-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="97c78-112">在您的衍生類別中，覆寫 `OnActivate` 以初始化對話方塊。</span><span class="sxs-lookup"><span data-stu-id="97c78-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="97c78-113">範例</span><span class="sxs-lookup"><span data-stu-id="97c78-113">Examples</span></span>

<span data-ttu-id="97c78-114">下列範例會初始化 [執行] 控制項。</span><span class="sxs-lookup"><span data-stu-id="97c78-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="97c78-115">此範例假設 **m \_ pOwningFilter** 是與屬性頁相關聯之篩選準則的自訂介面指標。</span><span class="sxs-lookup"><span data-stu-id="97c78-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="97c78-116"> (使用 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法來初始化這類指標。 ) </span><span class="sxs-lookup"><span data-stu-id="97c78-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="97c78-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="97c78-117">Requirements</span></span>



| <span data-ttu-id="97c78-118">需求</span><span class="sxs-lookup"><span data-stu-id="97c78-118">Requirement</span></span> | <span data-ttu-id="97c78-119">值</span><span class="sxs-lookup"><span data-stu-id="97c78-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c78-120">標頭</span><span class="sxs-lookup"><span data-stu-id="97c78-120">Header</span></span><br/>  | <dl> <span data-ttu-id="97c78-121"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="97c78-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="97c78-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="97c78-122">Library</span></span><br/> | <dl> <span data-ttu-id="97c78-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="97c78-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c78-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97c78-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c78-125">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="97c78-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




