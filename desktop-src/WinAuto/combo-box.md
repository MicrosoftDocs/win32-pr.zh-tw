---
title: '下拉式方塊 (MSAA UI 元素參考) '
description: 下拉式方塊是與靜態控制項結合的清單方塊，或是在下拉式方塊的清單方塊部分中顯示目前選取項目的編輯控制項。
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673599"
---
# <a name="combo-box-msaa-ui-element-reference"></a><span data-ttu-id="d3939-103">下拉式方塊 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="d3939-103">Combo Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="d3939-104">本主題描述用於 MSAA UI 專案參考之 **下拉式列示方塊** 物件的用途。</span><span class="sxs-lookup"><span data-stu-id="d3939-104">This topic describes **Combo Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="d3939-105">此處未說明如何在各種 UI 架構中建立 **下拉式列示方塊** 物件。</span><span class="sxs-lookup"><span data-stu-id="d3939-105">How to create **Combo Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="d3939-106">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="d3939-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="d3939-107">下拉式方塊是與靜態控制項結合的清單方塊，或是在下拉式方塊的清單方塊部分中顯示目前選取項目的編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="d3939-107">A combo box is a list box combined with a static control or an edit control that displays the currently selected item in the list box portion of the combo box.</span></span> <span data-ttu-id="d3939-108">控制項的清單方塊部分會隨時顯示，或只有在使用者選取下拉式箭號時，才會顯示下拉式箭號 (也就是控制項旁邊) 的 [按下] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d3939-108">The list box portion of the control is displayed at all times or only drop down when the user selects the drop-down arrow (which is a push button) next to the control.</span></span> <span data-ttu-id="d3939-109">如果選取欄位是編輯控制項，則使用者可以輸入不在清單中的資訊;否則，使用者只能選取清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="d3939-109">If the selection field is an edit control, the user can enter information not in the list; otherwise, the user can only select items in the list.</span></span>

<span data-ttu-id="d3939-110">下拉式方塊的視窗類別名稱是「COMBOBOX」。</span><span class="sxs-lookup"><span data-stu-id="d3939-110">The window class name for a combo box is "COMBOBOX".</span></span>

<span data-ttu-id="d3939-111">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性的內容取決於用戶端查詢下拉式方塊的下列哪些部分：</span><span class="sxs-lookup"><span data-stu-id="d3939-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on which of the following parts of the combo box is queried by the client:</span></span>

-   <span data-ttu-id="d3939-112">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-112">The combo box window</span></span>
-   <span data-ttu-id="d3939-113">編輯控制項或靜態文字控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-113">The edit control or static text control</span></span>
-   <span data-ttu-id="d3939-114">下拉箭號 (是按下按鈕) </span><span class="sxs-lookup"><span data-stu-id="d3939-114">The drop-down arrow (which is a push button)</span></span>
-   <span data-ttu-id="d3939-115">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-115">The list box</span></span>
-   <span data-ttu-id="d3939-116">清單方塊中的清單專案</span><span class="sxs-lookup"><span data-stu-id="d3939-116">The list items in the list box</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="d3939-117">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="d3939-117">IAccessible Methods</span></span>

<span data-ttu-id="d3939-118">下拉式方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="d3939-118">Combo boxes support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="d3939-119">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="d3939-119">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [<span data-ttu-id="d3939-120">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="d3939-120">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="d3939-121">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="d3939-121">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="d3939-122">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="d3939-122">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="d3939-123">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="d3939-123">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="d3939-124">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="d3939-124">IAccessible Properties</span></span>

<span data-ttu-id="d3939-125">下拉式方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="d3939-125">Combo boxes support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="d3939-126">**取得 \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="d3939-126">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   <span data-ttu-id="d3939-127">[**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)-下表顯示下拉式方塊中不同部分的子計數值。</span><span class="sxs-lookup"><span data-stu-id="d3939-127">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The following table shows the child count value for different parts of the combo box.</span></span> 

    | <span data-ttu-id="d3939-128">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-128">Combo box part</span></span>   | <span data-ttu-id="d3939-129">ChildCount</span><span class="sxs-lookup"><span data-stu-id="d3939-129">ChildCount</span></span>               |
    |------------------|--------------------------|
    | <span data-ttu-id="d3939-130">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-130">Combo box window</span></span> | <span data-ttu-id="d3939-131">3</span><span class="sxs-lookup"><span data-stu-id="d3939-131">3</span></span>                        |
    | <span data-ttu-id="d3939-132">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-132">Edit control</span></span>     | <span data-ttu-id="d3939-133">0</span><span class="sxs-lookup"><span data-stu-id="d3939-133">0</span></span>                        |
    | <span data-ttu-id="d3939-134">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-134">Drop-down arrow</span></span>  | <span data-ttu-id="d3939-135">0</span><span class="sxs-lookup"><span data-stu-id="d3939-135">0</span></span>                        |
    | <span data-ttu-id="d3939-136">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-136">List box</span></span>         | <span data-ttu-id="d3939-137">清單專案的數目</span><span class="sxs-lookup"><span data-stu-id="d3939-137">The number of list items</span></span> |
    | <span data-ttu-id="d3939-138">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-138">List item</span></span>        | <span data-ttu-id="d3939-139">0</span><span class="sxs-lookup"><span data-stu-id="d3939-139">0</span></span>                        |

    

     

-   <span data-ttu-id="d3939-140">[**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)-下表顯示下拉式方塊中不同部分的 **DefaultAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3939-140">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The following table shows the **DefaultAction** property for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-141">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-141">Combo box part</span></span>   | <span data-ttu-id="d3939-142">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="d3939-142">DefaultAction</span></span>                                                  |
    |------------------|----------------------------------------------------------------|
    | <span data-ttu-id="d3939-143">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-143">Combo box window</span></span> | <span data-ttu-id="d3939-144">無</span><span class="sxs-lookup"><span data-stu-id="d3939-144">None</span></span>                                                           |
    | <span data-ttu-id="d3939-145">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-145">Edit control</span></span>     | <span data-ttu-id="d3939-146">無</span><span class="sxs-lookup"><span data-stu-id="d3939-146">None</span></span>                                                           |
    | <span data-ttu-id="d3939-147">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-147">Drop-down arrow</span></span>  | <span data-ttu-id="d3939-148">[開啟] 或 [關閉]，視下拉式清單的狀態而定</span><span class="sxs-lookup"><span data-stu-id="d3939-148">"Open" or "Close" depending on the state of the drop-down list</span></span> |
    | <span data-ttu-id="d3939-149">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-149">List box</span></span>         | <span data-ttu-id="d3939-150">無</span><span class="sxs-lookup"><span data-stu-id="d3939-150">None</span></span>                                                           |
    | <span data-ttu-id="d3939-151">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-151">List item</span></span>        | <span data-ttu-id="d3939-152">[按兩下]</span><span class="sxs-lookup"><span data-stu-id="d3939-152">"Double Click"</span></span>                                                 |

    

     

-   [<span data-ttu-id="d3939-153">**取得 \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="d3939-153">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="d3939-154">**取得 \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="d3939-154">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="d3939-155">**取得 \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="d3939-155">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="d3939-156">**取得 \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="d3939-156">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="d3939-157">[**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)-下表顯示下拉式方塊中不同部分的 **KeyboardShortcut** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3939-157">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The following table shows the **KeyboardShortcut** property for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-158">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-158">Combo box part</span></span>   | <span data-ttu-id="d3939-159">KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="d3939-159">KeyboardShortcut</span></span>               |
    |------------------|--------------------------------|
    | <span data-ttu-id="d3939-160">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-160">Combo box window</span></span> | <span data-ttu-id="d3939-161">相關標籤的存取金鑰</span><span class="sxs-lookup"><span data-stu-id="d3939-161">Access key of associated label</span></span> |
    | <span data-ttu-id="d3939-162">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-162">Edit control</span></span>     | <span data-ttu-id="d3939-163">無</span><span class="sxs-lookup"><span data-stu-id="d3939-163">None</span></span>                           |
    | <span data-ttu-id="d3939-164">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-164">Drop-down arrow</span></span>  | <span data-ttu-id="d3939-165">"Alt + 向下鍵"</span><span class="sxs-lookup"><span data-stu-id="d3939-165">"Alt+Down Arrow"</span></span>               |
    | <span data-ttu-id="d3939-166">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-166">List box</span></span>         | <span data-ttu-id="d3939-167">無</span><span class="sxs-lookup"><span data-stu-id="d3939-167">None</span></span>                           |
    | <span data-ttu-id="d3939-168">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-168">List item</span></span>        | <span data-ttu-id="d3939-169">無</span><span class="sxs-lookup"><span data-stu-id="d3939-169">None</span></span>                           |

    

     

    <span data-ttu-id="d3939-170">下拉式方塊的存取金鑰是標示下拉式方塊之相關聯靜態文字控制項文字中的加底線字元。</span><span class="sxs-lookup"><span data-stu-id="d3939-170">The access key for a combo box is the underlined character in the text from an associated static text control that labels the combo box.</span></span> <span data-ttu-id="d3939-171">例如，在開啟檔案的標準開啟對話方塊（例如 Microsoft WordPad）中，標示為 "Files of type：" 的下拉式方塊具有 **KeyboardShortcut** "Alt + t"。</span><span class="sxs-lookup"><span data-stu-id="d3939-171">For example, on a standard Open dialog box that opens files, such as in Microsoft WordPad, the combo box labeled "Files of type:" has the **KeyboardShortcut** "Alt+t".</span></span>

-   <span data-ttu-id="d3939-172">[**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)-下表顯示下拉式方塊中不同部分的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3939-172">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The following table shows the **Name** property for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-173">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-173">Combo box part</span></span>   | <span data-ttu-id="d3939-174">Name</span><span class="sxs-lookup"><span data-stu-id="d3939-174">Name</span></span>                                                           |
    |------------------|----------------------------------------------------------------|
    | <span data-ttu-id="d3939-175">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-175">Combo box window</span></span> | <span data-ttu-id="d3939-176">當做標籤使用的靜態文字控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-176">Static text control used as a label</span></span>                            |
    | <span data-ttu-id="d3939-177">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-177">Edit control</span></span>     | <span data-ttu-id="d3939-178">當做標籤使用的靜態文字控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-178">Static text control used as a label</span></span>                            |
    | <span data-ttu-id="d3939-179">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-179">Drop-down arrow</span></span>  | <span data-ttu-id="d3939-180">[開啟] 或 [關閉]，視下拉式清單的狀態而定</span><span class="sxs-lookup"><span data-stu-id="d3939-180">"Open" or "Close" depending on the state of the drop-down list</span></span> |
    | <span data-ttu-id="d3939-181">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-181">List box</span></span>         | <span data-ttu-id="d3939-182">相關聯的標籤</span><span class="sxs-lookup"><span data-stu-id="d3939-182">Associated label</span></span>                                               |
    | <span data-ttu-id="d3939-183">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-183">List item</span></span>        | <span data-ttu-id="d3939-184">清單專案的文字</span><span class="sxs-lookup"><span data-stu-id="d3939-184">Text of the list item</span></span>                                          |

    

     

    <span data-ttu-id="d3939-185">下拉式方塊的 [ **名稱** ] 屬性、其子編輯控制項，以及其子清單方塊，都是關聯的靜態文字控制項中標示下拉式方塊的文字。</span><span class="sxs-lookup"><span data-stu-id="d3939-185">The **Name** property of a combo box, its child edit control, and its child list box is the text from an associated static text control that labels the combo box.</span></span> <span data-ttu-id="d3939-186">例如，在開啟檔案的標準開啟對話方塊中（例如在 WordPad 中），兩個下拉式方塊的 **名稱** 屬性是「查詢：」和「檔案類型：」。</span><span class="sxs-lookup"><span data-stu-id="d3939-186">For example, on a standard Open dialog box that opens files, such as in WordPad, the **Name** properties for the two combo boxes are "Look in:" and "Files of type:".</span></span>

-   <span data-ttu-id="d3939-187">[**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)-下表顯示下拉式方塊中不同部分的父值。</span><span class="sxs-lookup"><span data-stu-id="d3939-187">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The following table shows the parent value for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-188">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-188">Combo box part</span></span>                        | <span data-ttu-id="d3939-189">父代</span><span class="sxs-lookup"><span data-stu-id="d3939-189">Parent</span></span>                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d3939-190">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-190">Combo box window</span></span>                      | <span data-ttu-id="d3939-191">具有 [**角色 \_ 系統 \_ 視窗**](object-roles.md)的 **role** 屬性的視窗，此視窗會圍繞下拉式方塊，且具有與下拉式方塊相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="d3939-191">A window with the **Role** property of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) that surrounds the combo box and has the same **Name** property and window class name as the combo box.</span></span> |
    | <span data-ttu-id="d3939-192">編輯控制項 (或靜態文字控制項) </span><span class="sxs-lookup"><span data-stu-id="d3939-192">Edit control (or static text control)</span></span> | <span data-ttu-id="d3939-193">下拉式方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="d3939-193">The combo box window.</span></span>                                                                                                                                                                                          |
    | <span data-ttu-id="d3939-194">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-194">Drop-down arrow</span></span>                       | <span data-ttu-id="d3939-195">下拉式方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="d3939-195">The combo box window.</span></span>                                                                                                                                                                                          |
    | <span data-ttu-id="d3939-196">清單方塊父視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-196">List box parent window</span></span>                | <span data-ttu-id="d3939-197">下拉式方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="d3939-197">The combo box window.</span></span> <span data-ttu-id="d3939-198">此視窗會圍繞在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="d3939-198">This window surrounds the list box.</span></span>                                                                                                                                                      |
    | <span data-ttu-id="d3939-199">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-199">List box</span></span>                              | <span data-ttu-id="d3939-200">清單方塊父視窗。</span><span class="sxs-lookup"><span data-stu-id="d3939-200">The list box parent window.</span></span>                                                                                                                                                                                    |
    | <span data-ttu-id="d3939-201">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-201">List item</span></span>                             | <span data-ttu-id="d3939-202">清單方塊。</span><span class="sxs-lookup"><span data-stu-id="d3939-202">The list box.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="d3939-203">[**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)-下表顯示下拉式方塊中不同部分的 **角色** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3939-203">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The following table shows the **Role** property for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-204">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-204">Combo box part</span></span>                        | [<span data-ttu-id="d3939-205">角色</span><span class="sxs-lookup"><span data-stu-id="d3939-205">Role</span></span>](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d3939-206">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-206">Combo box window</span></span>                      | [<span data-ttu-id="d3939-207">**角色 \_ 系統 \_ COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="d3939-207">**ROLE\_SYSTEM\_COMBOBOX**</span></span>](object-roles.md)                                                                    |
    | <span data-ttu-id="d3939-208">編輯控制項 (或靜態文字控制項) </span><span class="sxs-lookup"><span data-stu-id="d3939-208">Edit control (or static text control)</span></span> | <span data-ttu-id="d3939-209">[**角色 \_系統 \_ 文字**](object-roles.md) 或 [**角色 \_ 系統 \_ STATICTEXT**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="d3939-209">[**ROLE\_SYSTEM\_TEXT**](object-roles.md) or [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md)</span></span> |
    | <span data-ttu-id="d3939-210">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-210">Drop-down arrow</span></span>                       | [<span data-ttu-id="d3939-211">**角色 \_ 系統 \_ 按鍵**</span><span class="sxs-lookup"><span data-stu-id="d3939-211">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md)                                                                |
    | <span data-ttu-id="d3939-212">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-212">List box</span></span>                              | [<span data-ttu-id="d3939-213">**角色 \_ 系統 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="d3939-213">**ROLE\_SYSTEM\_LIST**</span></span>](object-roles.md)                                                                            |
    | <span data-ttu-id="d3939-214">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-214">List item</span></span>                             | [<span data-ttu-id="d3939-215">**角色 \_ 系統 \_**</span><span class="sxs-lookup"><span data-stu-id="d3939-215">**ROLE\_SYSTEM\_LISTITEM**</span></span>](object-roles.md)                                                                    |

    

     

-   <span data-ttu-id="d3939-216">[**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)-下表顯示下拉式方塊的不同部分的 **狀態** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3939-216">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The following table shows the **State** property for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-217">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-217">Combo box part</span></span>   | [<span data-ttu-id="d3939-218">可能的狀態</span><span class="sxs-lookup"><span data-stu-id="d3939-218">Possible states</span></span>](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d3939-219">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-219">Combo box window</span></span> | <span data-ttu-id="d3939-220">[**狀態 \_系統 \_ 隱藏**](object-state-constants.md)式 \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 一般**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 展開**](object-state-constants.md) \| [**狀態 \_ \_**](object-state-constants.md)系統已折迭</span><span class="sxs-lookup"><span data-stu-id="d3939-220">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md) \| [**STATE\_SYSTEM\_EXPANDED**](object-state-constants.md) \| [**STATE\_SYSTEM\_COLLAPSED**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="d3939-221">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-221">Edit control</span></span>     | <span data-ttu-id="d3939-222">[**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d3939-222">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                                                                         |
    | <span data-ttu-id="d3939-223">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-223">Drop-down arrow</span></span>  | <span data-ttu-id="d3939-224">0，表示按鈕為可見且未按下。或 [**狀態 \_ 系統已 \_ 按下**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| 狀態 \_ 系統 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="d3939-224">0, which means the button is visible and not pressed; or [**STATE\_SYSTEM\_PRESSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| STATE\_SYSTEM\_NORMAL</span></span>                                                                                                                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="d3939-225">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-225">List box</span></span>         | <span data-ttu-id="d3939-226">[**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 浮動**](object-state-constants.md) \| [**狀態系統 \_ \_ 正常**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d3939-226">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                      |
    | <span data-ttu-id="d3939-227">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-227">List item</span></span>        | <span data-ttu-id="d3939-228">[**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 選取**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 選取**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d3939-228">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_SELECTABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_SELECTED**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                        |

    

     

-   <span data-ttu-id="d3939-229">[**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)-下表顯示下拉式方塊中不同部分的 [ **值** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3939-229">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The following table shows the **Value** property for different parts of a combo box.</span></span> 

    | <span data-ttu-id="d3939-230">下拉式方塊元件</span><span class="sxs-lookup"><span data-stu-id="d3939-230">Combo box part</span></span>   | <span data-ttu-id="d3939-231">值</span><span class="sxs-lookup"><span data-stu-id="d3939-231">Value</span></span>                                |
    |------------------|--------------------------------------|
    | <span data-ttu-id="d3939-232">下拉式方塊視窗</span><span class="sxs-lookup"><span data-stu-id="d3939-232">Combo box window</span></span> | <span data-ttu-id="d3939-233">目前選取清單專案的文字</span><span class="sxs-lookup"><span data-stu-id="d3939-233">Text of currently selected list item</span></span> |
    | <span data-ttu-id="d3939-234">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="d3939-234">Edit control</span></span>     | <span data-ttu-id="d3939-235">目前選取清單專案的文字</span><span class="sxs-lookup"><span data-stu-id="d3939-235">Text of currently selected list item</span></span> |
    | <span data-ttu-id="d3939-236">下拉箭號</span><span class="sxs-lookup"><span data-stu-id="d3939-236">Drop-down arrow</span></span>  | <span data-ttu-id="d3939-237">無</span><span class="sxs-lookup"><span data-stu-id="d3939-237">None</span></span>                                 |
    | <span data-ttu-id="d3939-238">清單方塊</span><span class="sxs-lookup"><span data-stu-id="d3939-238">List box</span></span>         | <span data-ttu-id="d3939-239">無</span><span class="sxs-lookup"><span data-stu-id="d3939-239">None</span></span>                                 |
    | <span data-ttu-id="d3939-240">清單項目</span><span class="sxs-lookup"><span data-stu-id="d3939-240">List item</span></span>        | <span data-ttu-id="d3939-241">無</span><span class="sxs-lookup"><span data-stu-id="d3939-241">None</span></span>                                 |

    

     

## <a name="notes"></a><span data-ttu-id="d3939-242">備註</span><span class="sxs-lookup"><span data-stu-id="d3939-242">Notes</span></span>

-   <span data-ttu-id="d3939-243">在下拉式方塊的清單方塊中，使用 [ [**NAVDIR \_ 下一個**](navigation-constants.md)] 旗標呼叫 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)時，它會在應該傳回 **VT \_ 空白** 的情況下，不正確地流覽至系統匣視窗。</span><span class="sxs-lookup"><span data-stu-id="d3939-243">When [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) is called with the [**NAVDIR\_NEXT**](navigation-constants.md) flag on the list box part of a combo box, it incorrectly navigates to the tray window when it should return **VT\_EMPTY**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3939-244">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3939-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3939-245">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="d3939-245">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




