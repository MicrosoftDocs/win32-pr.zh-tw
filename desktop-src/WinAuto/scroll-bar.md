---
title: '捲軸 (MSAA UI 元素參考) '
description: 捲軸可讓使用者選擇方向和距離，以在相關的視窗或清單方塊中滾動資訊。 捲軸的視窗類別名稱是 \ 0034;捲軸 \ 0034;。
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024037"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="94fd0-104">捲軸 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="94fd0-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="94fd0-105">本主題描述用於 MSAA UI 元素參考的 **捲軸** 物件。</span><span class="sxs-lookup"><span data-stu-id="94fd0-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="94fd0-106">此處未說明如何在各種 UI 架構中建立 **捲軸** 物件。</span><span class="sxs-lookup"><span data-stu-id="94fd0-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="94fd0-107">請參閱您所使用之 UI 架構的 API 參考檔。</span><span class="sxs-lookup"><span data-stu-id="94fd0-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="94fd0-108">捲軸可讓使用者選擇方向和距離，以在相關的視窗或清單方塊中滾動資訊。</span><span class="sxs-lookup"><span data-stu-id="94fd0-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="94fd0-109">捲軸的視窗類別名稱是「捲軸」。</span><span class="sxs-lookup"><span data-stu-id="94fd0-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="94fd0-110">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性的內容取決於捲軸是垂直或水準，以及用戶端是否正在查詢捲軸的下列部分：</span><span class="sxs-lookup"><span data-stu-id="94fd0-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="94fd0-111">捲軸本身</span><span class="sxs-lookup"><span data-stu-id="94fd0-111">The scroll bar itself</span></span>
-   <span data-ttu-id="94fd0-112">右上箭號或向右箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-112">The top or right arrow button</span></span>
-   <span data-ttu-id="94fd0-113">右下箭號或向左箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="94fd0-114">捲動方塊 (thumb) </span><span class="sxs-lookup"><span data-stu-id="94fd0-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="94fd0-115">Page up 或 page right 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-115">The page up or page right region</span></span>
-   <span data-ttu-id="94fd0-116">Page down 或 page left 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="94fd0-117">IAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="94fd0-117">IAccessible Methods</span></span>

<span data-ttu-id="94fd0-118">捲軸支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：</span><span class="sxs-lookup"><span data-stu-id="94fd0-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="94fd0-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)-捲軸物件本身和捲動方塊不支援 **accDoDefaultAction** 方法。</span><span class="sxs-lookup"><span data-stu-id="94fd0-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="94fd0-120">針對垂直捲動條上的其他捲軸部分， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，並將 *wParam* 設定為下列值的 [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)訊息。</span><span class="sxs-lookup"><span data-stu-id="94fd0-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="94fd0-121">按鈕/區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-121">Button/Region</span></span>       | <span data-ttu-id="94fd0-122">Vaule</span><span class="sxs-lookup"><span data-stu-id="94fd0-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="94fd0-123">上方箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-123">Top arrow button</span></span>    | <span data-ttu-id="94fd0-124">SB \_ 系列</span><span class="sxs-lookup"><span data-stu-id="94fd0-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="94fd0-125">底部箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-125">Bottom arrow button</span></span> | <span data-ttu-id="94fd0-126">SB \_ LINEDOWN</span><span class="sxs-lookup"><span data-stu-id="94fd0-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="94fd0-127">Page up 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-127">Page up region</span></span>      | <span data-ttu-id="94fd0-128">SB \_ PAGEUP</span><span class="sxs-lookup"><span data-stu-id="94fd0-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="94fd0-129">Page down 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-129">Page down region</span></span>    | <span data-ttu-id="94fd0-130">SB \_ PAGEDOWN</span><span class="sxs-lookup"><span data-stu-id="94fd0-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="94fd0-131">針對水準捲軸上的其他捲軸部分， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，並將 *wParam* 設定為下列值的 [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll)訊息。</span><span class="sxs-lookup"><span data-stu-id="94fd0-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="94fd0-132">按鈕/區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-132">Button/Region</span></span>      | <span data-ttu-id="94fd0-133">值</span><span class="sxs-lookup"><span data-stu-id="94fd0-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="94fd0-134">向左箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-134">Left arrow button</span></span>  | <span data-ttu-id="94fd0-135">SB \_ LINELEFT</span><span class="sxs-lookup"><span data-stu-id="94fd0-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="94fd0-136">右箭頭按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-136">Right arrow button</span></span> | <span data-ttu-id="94fd0-137">SB \_ LINERIGHT</span><span class="sxs-lookup"><span data-stu-id="94fd0-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="94fd0-138">左方頁面區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-138">Page left region</span></span>   | <span data-ttu-id="94fd0-139">SB \_ PAGELEFT</span><span class="sxs-lookup"><span data-stu-id="94fd0-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="94fd0-140">頁面右側區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-140">Page right region</span></span>  | <span data-ttu-id="94fd0-141">SB \_ PAGERIGHT</span><span class="sxs-lookup"><span data-stu-id="94fd0-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="94fd0-142">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="94fd0-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="94fd0-143">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="94fd0-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="94fd0-144">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="94fd0-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="94fd0-145">IAccessible 屬性</span><span class="sxs-lookup"><span data-stu-id="94fd0-145">IAccessible Properties</span></span>

<span data-ttu-id="94fd0-146">捲軸支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：</span><span class="sxs-lookup"><span data-stu-id="94fd0-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="94fd0-147">[**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)-捲軸物件的 **ChildCount** 屬性為五。</span><span class="sxs-lookup"><span data-stu-id="94fd0-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="94fd0-148">若為其他捲軸部分， **ChildCount** 屬性為零。</span><span class="sxs-lookup"><span data-stu-id="94fd0-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="94fd0-149">[**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)-捲軸物件本身和捲動方塊不支援 **DefaultAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="94fd0-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="94fd0-150">箭號按鈕的 **DefaultAction** 屬性和捲動方塊兩側的陰影區域是「按下」。</span><span class="sxs-lookup"><span data-stu-id="94fd0-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="94fd0-151">[**取得 \_ AccDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)： **Description** 屬性取決於所查詢捲軸的部分。</span><span class="sxs-lookup"><span data-stu-id="94fd0-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="94fd0-152">垂直捲動條的部分具有下列描述。</span><span class="sxs-lookup"><span data-stu-id="94fd0-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="94fd0-153">部分</span><span class="sxs-lookup"><span data-stu-id="94fd0-153">Part</span></span>                | <span data-ttu-id="94fd0-154">描述</span><span class="sxs-lookup"><span data-stu-id="94fd0-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="94fd0-155">捲軸本身</span><span class="sxs-lookup"><span data-stu-id="94fd0-155">Scroll bar itself</span></span>   | <span data-ttu-id="94fd0-156">"用來變更垂直視圖區域"</span><span class="sxs-lookup"><span data-stu-id="94fd0-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="94fd0-157">上方箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-157">Top arrow button</span></span>    | <span data-ttu-id="94fd0-158">「將垂直位置向上移動一行」</span><span class="sxs-lookup"><span data-stu-id="94fd0-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="94fd0-159">底部箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-159">Bottom arrow button</span></span> | <span data-ttu-id="94fd0-160">「將垂直位置向下移動一行」</span><span class="sxs-lookup"><span data-stu-id="94fd0-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="94fd0-161">捲動方塊</span><span class="sxs-lookup"><span data-stu-id="94fd0-161">Scroll thumb</span></span>        | <span data-ttu-id="94fd0-162">「表示目前的垂直位置，並且可以拖曳來直接變更」。</span><span class="sxs-lookup"><span data-stu-id="94fd0-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="94fd0-163">Page up 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-163">Page up region</span></span>      | <span data-ttu-id="94fd0-164">「將垂直位置向上移動幾行」</span><span class="sxs-lookup"><span data-stu-id="94fd0-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="94fd0-165">Page down 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-165">Page down region</span></span>    | <span data-ttu-id="94fd0-166">「表示目前的垂直位置，並且可以拖曳來直接變更」。</span><span class="sxs-lookup"><span data-stu-id="94fd0-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="94fd0-167">水準捲軸的部分具有下列描述。</span><span class="sxs-lookup"><span data-stu-id="94fd0-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="94fd0-168">部分</span><span class="sxs-lookup"><span data-stu-id="94fd0-168">Part</span></span>               | <span data-ttu-id="94fd0-169">描述</span><span class="sxs-lookup"><span data-stu-id="94fd0-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="94fd0-170">捲軸本身</span><span class="sxs-lookup"><span data-stu-id="94fd0-170">Scroll bar itself</span></span>  | <span data-ttu-id="94fd0-171">"用來變更水準視圖區域"</span><span class="sxs-lookup"><span data-stu-id="94fd0-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="94fd0-172">向左箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-172">Left arrow button</span></span>  | <span data-ttu-id="94fd0-173">「將水準位置向左移動一欄」</span><span class="sxs-lookup"><span data-stu-id="94fd0-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="94fd0-174">右箭頭按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-174">Right arrow button</span></span> | <span data-ttu-id="94fd0-175">「將水準位置向右移動一欄」</span><span class="sxs-lookup"><span data-stu-id="94fd0-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="94fd0-176">捲動方塊</span><span class="sxs-lookup"><span data-stu-id="94fd0-176">Scroll thumb</span></span>       | <span data-ttu-id="94fd0-177">「表示目前的水準位置，並且可以拖曳來直接變更」</span><span class="sxs-lookup"><span data-stu-id="94fd0-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="94fd0-178">左方頁面區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-178">Page left region</span></span>   | <span data-ttu-id="94fd0-179">「將水準位置向左移動幾個資料行」</span><span class="sxs-lookup"><span data-stu-id="94fd0-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="94fd0-180">頁面右側區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-180">Page right region</span></span>  | <span data-ttu-id="94fd0-181">「表示目前的垂直位置，並且可以拖曳來直接變更」。</span><span class="sxs-lookup"><span data-stu-id="94fd0-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="94fd0-182">**取得 \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="94fd0-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="94fd0-183">**取得 \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="94fd0-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="94fd0-184">[**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)： [ **名稱** ] 屬性取決於所查詢捲軸的部分。</span><span class="sxs-lookup"><span data-stu-id="94fd0-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="94fd0-185">垂直捲動條的部分具有下列名稱。</span><span class="sxs-lookup"><span data-stu-id="94fd0-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="94fd0-186">部分</span><span class="sxs-lookup"><span data-stu-id="94fd0-186">Part</span></span>                | <span data-ttu-id="94fd0-187">Name</span><span class="sxs-lookup"><span data-stu-id="94fd0-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="94fd0-188">捲軸視窗</span><span class="sxs-lookup"><span data-stu-id="94fd0-188">Scroll bar window</span></span>   | <span data-ttu-id="94fd0-189">縱</span><span class="sxs-lookup"><span data-stu-id="94fd0-189">"Vertical"</span></span>  |
    | <span data-ttu-id="94fd0-190">上方箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-190">Top arrow button</span></span>    | <span data-ttu-id="94fd0-191">「行出」</span><span class="sxs-lookup"><span data-stu-id="94fd0-191">"Line up"</span></span>   |
    | <span data-ttu-id="94fd0-192">底部箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-192">Bottom arrow button</span></span> | <span data-ttu-id="94fd0-193">「行出」</span><span class="sxs-lookup"><span data-stu-id="94fd0-193">"Line down"</span></span> |
    | <span data-ttu-id="94fd0-194">捲動方塊</span><span class="sxs-lookup"><span data-stu-id="94fd0-194">Scroll thumb</span></span>        | <span data-ttu-id="94fd0-195">居</span><span class="sxs-lookup"><span data-stu-id="94fd0-195">"Position"</span></span>  |
    | <span data-ttu-id="94fd0-196">Page up 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-196">Page up region</span></span>      | <span data-ttu-id="94fd0-197">「Page up」</span><span class="sxs-lookup"><span data-stu-id="94fd0-197">"Page up"</span></span>   |
    | <span data-ttu-id="94fd0-198">Page down 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-198">Page down region</span></span>    | <span data-ttu-id="94fd0-199">「下一頁」</span><span class="sxs-lookup"><span data-stu-id="94fd0-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="94fd0-200">水準捲軸的部分具有下列名稱。</span><span class="sxs-lookup"><span data-stu-id="94fd0-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="94fd0-201">部分</span><span class="sxs-lookup"><span data-stu-id="94fd0-201">Part</span></span>               | <span data-ttu-id="94fd0-202">Name</span><span class="sxs-lookup"><span data-stu-id="94fd0-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="94fd0-203">捲軸視窗</span><span class="sxs-lookup"><span data-stu-id="94fd0-203">Scroll bar window</span></span>  | <span data-ttu-id="94fd0-204">方向</span><span class="sxs-lookup"><span data-stu-id="94fd0-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="94fd0-205">向左箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-205">Left arrow button</span></span>  | <span data-ttu-id="94fd0-206">「左方資料行」</span><span class="sxs-lookup"><span data-stu-id="94fd0-206">"Column left"</span></span>  |
    | <span data-ttu-id="94fd0-207">右箭頭按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-207">Right arrow button</span></span> | <span data-ttu-id="94fd0-208">「資料行右」</span><span class="sxs-lookup"><span data-stu-id="94fd0-208">"Column right"</span></span> |
    | <span data-ttu-id="94fd0-209">捲動方塊</span><span class="sxs-lookup"><span data-stu-id="94fd0-209">Scroll thumb</span></span>       | <span data-ttu-id="94fd0-210">居</span><span class="sxs-lookup"><span data-stu-id="94fd0-210">"Position"</span></span>     |
    | <span data-ttu-id="94fd0-211">頁面右側區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-211">Page right region</span></span>  | <span data-ttu-id="94fd0-212">「Page right」</span><span class="sxs-lookup"><span data-stu-id="94fd0-212">"Page right"</span></span>   |
    | <span data-ttu-id="94fd0-213">左方頁面區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-213">Page left region</span></span>   | <span data-ttu-id="94fd0-214">「左方頁面」</span><span class="sxs-lookup"><span data-stu-id="94fd0-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="94fd0-215">[**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)：箭號按鈕的 **父** 屬性、捲動方塊，以及 thumb 兩側的陰影區域是捲軸視窗。</span><span class="sxs-lookup"><span data-stu-id="94fd0-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="94fd0-216">捲軸視窗的 **父** 屬性是視窗 (角色 \_ 系統 \_ 視窗) ，它會圍繞控制項，而且具有相同的 **名稱** 屬性和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="94fd0-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="94fd0-217">[**取得 \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)- **Role** 屬性取決於所查詢捲軸的部分。</span><span class="sxs-lookup"><span data-stu-id="94fd0-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="94fd0-218">捲軸的部分具有下列角色。</span><span class="sxs-lookup"><span data-stu-id="94fd0-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="94fd0-219">部分</span><span class="sxs-lookup"><span data-stu-id="94fd0-219">Part</span></span>                                                  | <span data-ttu-id="94fd0-220">角色</span><span class="sxs-lookup"><span data-stu-id="94fd0-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="94fd0-221">捲軸本身</span><span class="sxs-lookup"><span data-stu-id="94fd0-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="94fd0-222">**角色 \_ 系統 \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="94fd0-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="94fd0-223">頂端、向下、向左和向右箭號按鈕</span><span class="sxs-lookup"><span data-stu-id="94fd0-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="94fd0-224">**角色 \_ 系統 \_ 按鍵**</span><span class="sxs-lookup"><span data-stu-id="94fd0-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="94fd0-225">捲動方塊</span><span class="sxs-lookup"><span data-stu-id="94fd0-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="94fd0-226">**角色 \_ 系統 \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="94fd0-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="94fd0-227">Page up、page down、page left 和 page right 區域</span><span class="sxs-lookup"><span data-stu-id="94fd0-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="94fd0-228">**角色 \_ 系統 \_ 按鍵**</span><span class="sxs-lookup"><span data-stu-id="94fd0-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="94fd0-229">[**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)：每個捲軸元件的 **State** 屬性包含下列 [值](object-state-constants.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="94fd0-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="94fd0-230">狀態</span><span class="sxs-lookup"><span data-stu-id="94fd0-230">State</span></span>                                                                                 | <span data-ttu-id="94fd0-231">值</span><span class="sxs-lookup"><span data-stu-id="94fd0-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="94fd0-232">**狀態 \_ 系統 \_ 隱藏**</span><span class="sxs-lookup"><span data-stu-id="94fd0-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="94fd0-233">如果是捲軸本身，表示指定的垂直或水準捲軸不存在。</span><span class="sxs-lookup"><span data-stu-id="94fd0-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="94fd0-234">若為 page up 或 page down 區域，這表示 thumb 的位置不存在。</span><span class="sxs-lookup"><span data-stu-id="94fd0-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="94fd0-235">**狀態 \_ 系統 \_ 外**</span><span class="sxs-lookup"><span data-stu-id="94fd0-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="94fd0-236">如果是捲軸本身，這表示視窗已調整大小，因此目前未顯示指定的垂直或水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="94fd0-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="94fd0-237">**已 \_ \_ 按下狀態系統**</span><span class="sxs-lookup"><span data-stu-id="94fd0-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="94fd0-238">按下箭號按鈕或頁面區域。</span><span class="sxs-lookup"><span data-stu-id="94fd0-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="94fd0-239">**狀態 \_ 系統 \_ 無法使用**</span><span class="sxs-lookup"><span data-stu-id="94fd0-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="94fd0-240">元件已停用。</span><span class="sxs-lookup"><span data-stu-id="94fd0-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="94fd0-241">[**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)-捲軸視窗的 [ **值** ] 屬性工作表示捲軸位置，而是包含從 "0" 到 "100" 之整數的字串。</span><span class="sxs-lookup"><span data-stu-id="94fd0-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="94fd0-242">相關主題</span><span class="sxs-lookup"><span data-stu-id="94fd0-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fd0-243">IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="94fd0-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 