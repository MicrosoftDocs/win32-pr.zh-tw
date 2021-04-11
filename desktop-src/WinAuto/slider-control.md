---
title: '滑杆控制項 (MSAA UI 元素參考) '
description: 滑杆控制項也稱為「資料格控制項」，可讓使用者藉由移動滑杆，從某個範圍的值進行選取。 Windows 作業系統中的音量控制就是滑桿 (Slider Control)。
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022020"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="71fb3-104">滑杆控制項 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="71fb3-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="71fb3-105">本主題描述用於 MSAA UI 專案參考之 **滑杆控制項** 物件的用途。</span><span class="sxs-lookup"><span data-stu-id="71fb3-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="71fb3-106">此處未說明如何在各種 UI 架構中建立 **滑杆控制項** 物件。</span><span class="sxs-lookup"><span data-stu-id="71fb3-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="71fb3-107">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="71fb3-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="71fb3-108">滑杆控制項也稱為「資料格控制項」，可讓使用者藉由移動滑杆，從某個範圍的值進行選取。</span><span class="sxs-lookup"><span data-stu-id="71fb3-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="71fb3-109">Windows 作業系統中的音量控制就是滑桿 (Slider Control)。</span><span class="sxs-lookup"><span data-stu-id="71fb3-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="71fb3-110">滑杆控制項的視窗類別名稱是 \_ 在 Commctrl 中定義為 "Msctls" 的 [類標] 類別。 \_</span><span class="sxs-lookup"><span data-stu-id="71fb3-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="71fb3-111">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性的內容取決於滑杆是垂直或水準，以及用戶端是否查詢滑杆控制項的下列部分：</span><span class="sxs-lookup"><span data-stu-id="71fb3-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="71fb3-112">滑杆視窗</span><span class="sxs-lookup"><span data-stu-id="71fb3-112">Slider window</span></span>
-   <span data-ttu-id="71fb3-113">滑杆捲軸</span><span class="sxs-lookup"><span data-stu-id="71fb3-113">Slider thumb</span></span>
-   <span data-ttu-id="71fb3-114">上方的陰影區域 (或</span><span class="sxs-lookup"><span data-stu-id="71fb3-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="71fb3-115"> (或) 滑杆捲動方塊右邊的陰影區域</span><span class="sxs-lookup"><span data-stu-id="71fb3-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="71fb3-116">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="71fb3-116">IAccessible Methods</span></span>

<span data-ttu-id="71fb3-117">滑杆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="71fb3-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="71fb3-118">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="71fb3-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="71fb3-119">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="71fb3-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="71fb3-120">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="71fb3-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="71fb3-121">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="71fb3-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="71fb3-122">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="71fb3-122">IAccessible Properties</span></span>

<span data-ttu-id="71fb3-123">滑杆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="71fb3-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="71fb3-124">**取得 \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="71fb3-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="71fb3-125">**取得 \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="71fb3-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="71fb3-126">**取得 \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="71fb3-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="71fb3-127">**取得 \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="71fb3-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="71fb3-128">**取得 \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="71fb3-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="71fb3-129">[**取得 \_ AccKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)： **KeyboardShortcut** 屬性是滑杆視窗的存取金鑰，也就是滑杆的標籤文字中的底線字元。</span><span class="sxs-lookup"><span data-stu-id="71fb3-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="71fb3-130">傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。</span><span class="sxs-lookup"><span data-stu-id="71fb3-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="71fb3-131">[**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)： [ **名稱** ] 屬性取決於所查詢之滑杆的部分。</span><span class="sxs-lookup"><span data-stu-id="71fb3-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="71fb3-132">垂直滑杆的部分具有下列名稱：</span><span class="sxs-lookup"><span data-stu-id="71fb3-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="71fb3-133">滑杆部分</span><span class="sxs-lookup"><span data-stu-id="71fb3-133">Slider part</span></span>                    | <span data-ttu-id="71fb3-134">Name</span><span class="sxs-lookup"><span data-stu-id="71fb3-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="71fb3-135">滑杆視窗</span><span class="sxs-lookup"><span data-stu-id="71fb3-135">Slider window</span></span>                  | <span data-ttu-id="71fb3-136">當做標籤使用的靜態文字控制項</span><span class="sxs-lookup"><span data-stu-id="71fb3-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="71fb3-137">滑杆捲軸</span><span class="sxs-lookup"><span data-stu-id="71fb3-137">Slider thumb</span></span>                   | <span data-ttu-id="71fb3-138">居</span><span class="sxs-lookup"><span data-stu-id="71fb3-138">"Position"</span></span>                          |
    | <span data-ttu-id="71fb3-139">上方的陰影區域滑杆捲軸</span><span class="sxs-lookup"><span data-stu-id="71fb3-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="71fb3-140">「Page up」</span><span class="sxs-lookup"><span data-stu-id="71fb3-140">"Page up"</span></span>                           |
    | <span data-ttu-id="71fb3-141">下滑杆捲動方塊的陰影區域</span><span class="sxs-lookup"><span data-stu-id="71fb3-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="71fb3-142">「下一頁」</span><span class="sxs-lookup"><span data-stu-id="71fb3-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="71fb3-143">水準滑杆的各部分具有下列名稱：</span><span class="sxs-lookup"><span data-stu-id="71fb3-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="71fb3-144">滑杆部分</span><span class="sxs-lookup"><span data-stu-id="71fb3-144">Slider part</span></span>                              | <span data-ttu-id="71fb3-145">Name</span><span class="sxs-lookup"><span data-stu-id="71fb3-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="71fb3-146">滑杆視窗</span><span class="sxs-lookup"><span data-stu-id="71fb3-146">Slider window</span></span>                            | <span data-ttu-id="71fb3-147">當做標籤使用的靜態文字控制項</span><span class="sxs-lookup"><span data-stu-id="71fb3-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="71fb3-148">滑杆捲軸</span><span class="sxs-lookup"><span data-stu-id="71fb3-148">Slider thumb</span></span>                             | <span data-ttu-id="71fb3-149">居</span><span class="sxs-lookup"><span data-stu-id="71fb3-149">"Position"</span></span>                          |
    | <span data-ttu-id="71fb3-150">滑杆捲動方塊左邊的陰影區域</span><span class="sxs-lookup"><span data-stu-id="71fb3-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="71fb3-151">「左方頁面」</span><span class="sxs-lookup"><span data-stu-id="71fb3-151">"Page left"</span></span>                         |
    | <span data-ttu-id="71fb3-152">滑杆捲動方塊右邊的陰影區域</span><span class="sxs-lookup"><span data-stu-id="71fb3-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="71fb3-153">「Page right」</span><span class="sxs-lookup"><span data-stu-id="71fb3-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="71fb3-154">[**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)：箭號按鈕的 **父** 屬性、捲動方塊，以及 thumb 兩側的陰影區域是滑杆視窗。</span><span class="sxs-lookup"><span data-stu-id="71fb3-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="71fb3-155">滑杆視窗的 **Parent** 屬性是視窗 ( [**角色 \_ 系統 \_ 視窗**](object-roles.md) ) ，它會圍繞控制項，而且具有相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="71fb3-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="71fb3-156">[**取得 \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)- **Role** 屬性取決於所查詢之滑杆的部分。</span><span class="sxs-lookup"><span data-stu-id="71fb3-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="71fb3-157">滑杆部分</span><span class="sxs-lookup"><span data-stu-id="71fb3-157">Slider part</span></span>                                     | [<span data-ttu-id="71fb3-158">角色</span><span class="sxs-lookup"><span data-stu-id="71fb3-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="71fb3-159">滑杆視窗</span><span class="sxs-lookup"><span data-stu-id="71fb3-159">Slider window</span></span>                                   | [<span data-ttu-id="71fb3-160">**角色 \_ 系統 \_ 滑杆**</span><span class="sxs-lookup"><span data-stu-id="71fb3-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="71fb3-161">滑杆捲軸</span><span class="sxs-lookup"><span data-stu-id="71fb3-161">Slider thumb</span></span>                                    | [<span data-ttu-id="71fb3-162">**角色 \_ 系統 \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="71fb3-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="71fb3-163">滑杆捲動方塊兩側的陰影區域</span><span class="sxs-lookup"><span data-stu-id="71fb3-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="71fb3-164">**角色 \_ 系統 \_ 按鍵**</span><span class="sxs-lookup"><span data-stu-id="71fb3-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="71fb3-165">[**取得 \_ AccState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)： **State** 屬性的 [值](object-state-constants.md)取決於所查詢之滑杆的部分。</span><span class="sxs-lookup"><span data-stu-id="71fb3-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="71fb3-166">滑杆部分</span><span class="sxs-lookup"><span data-stu-id="71fb3-166">Slider Part</span></span>                                     | <span data-ttu-id="71fb3-167">可能的狀態值</span><span class="sxs-lookup"><span data-stu-id="71fb3-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="71fb3-168">滑杆視窗</span><span class="sxs-lookup"><span data-stu-id="71fb3-168">Slider window</span></span>                                   | <span data-ttu-id="71fb3-169">[**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="71fb3-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="71fb3-170">滑杆捲軸</span><span class="sxs-lookup"><span data-stu-id="71fb3-170">Slider thumb</span></span>                                    | <span data-ttu-id="71fb3-171">零 (0) ，表示物件是可見的，或 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)的狀態 \| [**\_ 系統 \_ 無法使用**](object-state-constants.md)狀態系統 \| [**\_ \_ 正常**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="71fb3-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="71fb3-172">滑杆捲動方塊兩側的陰影區域</span><span class="sxs-lookup"><span data-stu-id="71fb3-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="71fb3-173">零 (0) ，表示物件是可見的，或 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)的狀態 \| [**\_ 系統 \_ 無法使用**](object-state-constants.md)狀態系統 \| [**\_ \_ 正常**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="71fb3-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="71fb3-174">[**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)：滑杆視窗的 **Value** 屬性會指出 thumb 的位置，而是包含從 "0" 到 "100" 之整數的字串。</span><span class="sxs-lookup"><span data-stu-id="71fb3-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="71fb3-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="71fb3-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71fb3-176">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="71fb3-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="71fb3-177">**捲軸**</span><span class="sxs-lookup"><span data-stu-id="71fb3-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




