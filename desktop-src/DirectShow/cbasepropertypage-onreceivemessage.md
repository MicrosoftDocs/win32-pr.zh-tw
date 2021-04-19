---
description: 當對話方塊收到訊息時，就會呼叫 OnReceiveMessage 方法。
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: 'CBasePropertyPage. OnReceiveMessage 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978612"
---
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="619af-103">CBasePropertyPage. OnReceiveMessage 方法</span><span class="sxs-lookup"><span data-stu-id="619af-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="619af-104">`OnReceiveMessage`當對話方塊收到訊息時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="619af-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="619af-105">語法</span><span class="sxs-lookup"><span data-stu-id="619af-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="619af-106">參數</span><span class="sxs-lookup"><span data-stu-id="619af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619af-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="619af-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="619af-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="619af-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="619af-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="619af-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="619af-110">Message.</span><span class="sxs-lookup"><span data-stu-id="619af-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="619af-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="619af-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="619af-112">第一個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="619af-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="619af-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="619af-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="619af-114">第二個訊息參數。</span><span class="sxs-lookup"><span data-stu-id="619af-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619af-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="619af-115">Return value</span></span>

<span data-ttu-id="619af-116">傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="619af-116">Returns a Boolean value.</span></span> <span data-ttu-id="619af-117">對話方塊程式會傳回此值;如需詳細資訊，請參閱 Platform SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="619af-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="619af-118">備註</span><span class="sxs-lookup"><span data-stu-id="619af-118">Remarks</span></span>

<span data-ttu-id="619af-119">基底類別的實 **DefWindowProc** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="619af-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="619af-120">覆寫這個方法，以處理與對話方塊控制項相關的訊息。</span><span class="sxs-lookup"><span data-stu-id="619af-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="619af-121">如果覆寫方法未處理特定訊息，則應該呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="619af-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="619af-122">如果使用者透過對話方塊控制項變更任何屬性，請將 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md) 旗標設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="619af-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="619af-123">然後呼叫 [**CBasePropertyPage：： m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)指標上的 **IPropertyPageSite：： OnStatusChange** 方法來通知框架。</span><span class="sxs-lookup"><span data-stu-id="619af-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="619af-124">範例</span><span class="sxs-lookup"><span data-stu-id="619af-124">Examples</span></span>

<span data-ttu-id="619af-125">下列範例會藉由更新成員變數（假設要在衍生類別中定義）來回應按鈕點擊。</span><span class="sxs-lookup"><span data-stu-id="619af-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="619af-126">此範例也會顯示用於設定屬性頁變更狀態的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="619af-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="619af-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="619af-127">Requirements</span></span>



| <span data-ttu-id="619af-128">需求</span><span class="sxs-lookup"><span data-stu-id="619af-128">Requirement</span></span> | <span data-ttu-id="619af-129">值</span><span class="sxs-lookup"><span data-stu-id="619af-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619af-130">標頭</span><span class="sxs-lookup"><span data-stu-id="619af-130">Header</span></span><br/>  | <dl> <span data-ttu-id="619af-131"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="619af-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="619af-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="619af-132">Library</span></span><br/> | <dl> <span data-ttu-id="619af-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="619af-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="619af-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="619af-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619af-135">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="619af-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




