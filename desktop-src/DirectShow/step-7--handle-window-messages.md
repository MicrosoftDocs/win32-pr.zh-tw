---
description: 步驟 7：
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: 步驟 7： 處理視窗訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987311"
---
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="39e4a-104">步驟 7：</span><span class="sxs-lookup"><span data-stu-id="39e4a-104">Step 7.</span></span> <span data-ttu-id="39e4a-105">處理視窗訊息</span><span class="sxs-lookup"><span data-stu-id="39e4a-105">Handle Window Messages</span></span>

<span data-ttu-id="39e4a-106">覆寫 [**CBasePropertyPage：： OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) 方法，以更新對話方塊控制項以回應使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="39e4a-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="39e4a-107">如果您未處理特定訊息，請在父類別上呼叫 **OnReceiveMessage** 方法。</span><span class="sxs-lookup"><span data-stu-id="39e4a-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="39e4a-108">每當使用者變更屬性時，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="39e4a-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="39e4a-109">將 [屬性] 頁面的 **m \_ bDirty** 變數設定為 [ **TRUE**]。</span><span class="sxs-lookup"><span data-stu-id="39e4a-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="39e4a-110">使用 PROPPAGESTATUS 中途旗標，呼叫屬性框架的 **IPropertyPageSite：： OnStatusChange** 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="39e4a-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="39e4a-111">此旗標會通知屬性框架應該 **啟用 [套用** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="39e4a-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="39e4a-112">[**CBasePropertyPage：： m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)成員會保存 **IPropertyPageSite** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="39e4a-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="39e4a-113">若要簡化這個步驟，您可以將下列 helper 函式新增至您的屬性頁：</span><span class="sxs-lookup"><span data-stu-id="39e4a-113">To simplify this step, you can add the following helper function to your property page:</span></span>


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



<span data-ttu-id="39e4a-114">只要使用者動作變更屬性，就會在 **OnReceiveMessage** 內呼叫這個私用方法，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="39e4a-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



<span data-ttu-id="39e4a-115">此範例中的屬性頁面有兩個控制項：滑動軸和 [ **還原為預設值** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="39e4a-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="39e4a-116">如果使用者滾動滑動軸，屬性頁會設定篩選準則的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="39e4a-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="39e4a-117">如果使用者按一下按鈕，屬性頁會還原篩選的預設飽和度值。</span><span class="sxs-lookup"><span data-stu-id="39e4a-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="39e4a-118">在每個案例中，m \_ lNewVal 會保留目前的值，而 m \_ lVal 會保留原始值。</span><span class="sxs-lookup"><span data-stu-id="39e4a-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="39e4a-119">在 \_ 使用者認可變更之前，不會更新 m lVal 的值，這會在使用者按一下屬性框架上的 [  **確定]** 或 [套用] 按鈕時發生。</span><span class="sxs-lookup"><span data-stu-id="39e4a-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="39e4a-120">下一 [步：步驟8。套用屬性變更](step-8--apply-property-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="39e4a-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="39e4a-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="39e4a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39e4a-122">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="39e4a-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



