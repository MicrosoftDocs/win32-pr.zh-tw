---
title: 關於 ComboBoxEx 控制項
description: ComboBoxEx 控制項是下拉式方塊控制項，可提供專案影像的原生支援。
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427abef015474047d1842d13e5fb40640d0406c5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842803"
---
# <a name="about-comboboxex-controls"></a><span data-ttu-id="0241c-103">關於 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="0241c-103">About ComboBoxEx Controls</span></span>

<span data-ttu-id="0241c-104">ComboBoxEx 控制項是下拉式方塊控制項，可提供專案影像的原生支援。</span><span class="sxs-lookup"><span data-stu-id="0241c-104">ComboBoxEx controls are combo box controls that provide native support for item images.</span></span> <span data-ttu-id="0241c-105">為了讓專案影像易於存取，控制項提供影像清單支援。</span><span class="sxs-lookup"><span data-stu-id="0241c-105">To make item images easily accessible, the control provides image list support.</span></span> <span data-ttu-id="0241c-106">藉由使用這個控制項，您可以提供下拉式方塊的功能，而不需要手動繪製專案圖形。</span><span class="sxs-lookup"><span data-stu-id="0241c-106">By using this control, you can provide the functionality of a combo box without having to manually draw item graphics.</span></span>

<span data-ttu-id="0241c-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0241c-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0241c-108">建立 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="0241c-108">Creating ComboBoxEx Controls</span></span>](#creating-comboboxex-controls)
-   [<span data-ttu-id="0241c-109">ComboBoxEx 控制項樣式</span><span class="sxs-lookup"><span data-stu-id="0241c-109">ComboBoxEx Control Styles</span></span>](#comboboxex-control-styles)
-   [<span data-ttu-id="0241c-110">ComboBoxEx 控制項專案</span><span class="sxs-lookup"><span data-stu-id="0241c-110">ComboBoxEx Control Items</span></span>](#comboboxex-control-items)
-   [<span data-ttu-id="0241c-111">回呼專案</span><span class="sxs-lookup"><span data-stu-id="0241c-111">Callback Items</span></span>](#callback-items)
-   [<span data-ttu-id="0241c-112">ComboBoxEx 控制項影像清單</span><span class="sxs-lookup"><span data-stu-id="0241c-112">ComboBoxEx Control Image Lists</span></span>](#comboboxex-control-image-lists)
-   [<span data-ttu-id="0241c-113">關於 ComboBoxEx 控制通知訊息</span><span class="sxs-lookup"><span data-stu-id="0241c-113">About ComboBoxEx Control Notification Messages</span></span>](#about-comboboxex-control-notification-messages)
-   [<span data-ttu-id="0241c-114">ComboBoxEx 控制訊息轉送</span><span class="sxs-lookup"><span data-stu-id="0241c-114">ComboBoxEx Control Message Forwarding</span></span>](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a><span data-ttu-id="0241c-115">建立 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="0241c-115">Creating ComboBoxEx Controls</span></span>

<span data-ttu-id="0241c-116">實際上，ComboBoxEx 控制項會建立子下拉式方塊，並根據指派的影像清單，為您執行擁有者繪製工作。</span><span class="sxs-lookup"><span data-stu-id="0241c-116">Effectively, a ComboBoxEx control creates a child combo box and performs owner draw tasks for you based on an assigned image list.</span></span> <span data-ttu-id="0241c-117">因此， [**\_ OWNERDRAWFIXED**](combo-box-styles.md) 樣式是隱含的，而且在建立控制項時並不需要使用它。</span><span class="sxs-lookup"><span data-stu-id="0241c-117">Therefore, the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style is implied and it's not necessary to use it when creating the control.</span></span> <span data-ttu-id="0241c-118">因為影像清單是用來提供專案圖形，所以無法使用 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="0241c-118">Because image lists are used to provide item graphics, the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style cannot be used.</span></span>

<span data-ttu-id="0241c-119">ComboBoxEx 控制項必須透過呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來初始化， \_ \_ 在隨附的 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定 ICC USEREX 類別。</span><span class="sxs-lookup"><span data-stu-id="0241c-119">A ComboBoxEx control must be initialized by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying ICC\_USEREX\_CLASSES in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="0241c-120">您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數來建立 ComboBoxEx 控制項，並指定 [**WC \_ ComboBoxEx**](common-control-window-classes.md) 做為視窗類別。</span><span class="sxs-lookup"><span data-stu-id="0241c-120">You can create a ComboBoxEx control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying [**WC\_COMBOBOXEX**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="0241c-121">如上面所述呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式時，會註冊類別。</span><span class="sxs-lookup"><span data-stu-id="0241c-121">The class is registered when the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function is called as explained above.</span></span>

<span data-ttu-id="0241c-122">系統會建立不含預設影像清單的 ComboBoxEx 控制項。</span><span class="sxs-lookup"><span data-stu-id="0241c-122">ComboBoxEx controls are created without a default image list.</span></span> <span data-ttu-id="0241c-123">若要使用專案影像，您必須建立 ComboBoxEx 控制項的影像清單，並使用 [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) 訊息將它指派給控制項。</span><span class="sxs-lookup"><span data-stu-id="0241c-123">To use item images, you must create an image list for the ComboBoxEx control and assign it to the control using the [**CBEM\_SETIMAGELIST**](cbem-setimagelist.md) message.</span></span> <span data-ttu-id="0241c-124">如果您未將影像清單指派給 ComboBoxEx 控制項，控制項只會顯示專案文字。</span><span class="sxs-lookup"><span data-stu-id="0241c-124">If you do not assign an image list to the ComboBoxEx control, the control displays item text only.</span></span>

## <a name="comboboxex-control-styles"></a><span data-ttu-id="0241c-125">ComboBoxEx 控制項樣式</span><span class="sxs-lookup"><span data-stu-id="0241c-125">ComboBoxEx Control Styles</span></span>

<span data-ttu-id="0241c-126">ComboBoxEx 控制項僅支援下列 ComboBox 樣式：</span><span class="sxs-lookup"><span data-stu-id="0241c-126">ComboBoxEx controls support only the following ComboBox styles:</span></span>

-   <span data-ttu-id="0241c-127">CBS \_ 簡單</span><span class="sxs-lookup"><span data-stu-id="0241c-127">CBS\_SIMPLE</span></span>
-   <span data-ttu-id="0241c-128">CBS \_ 下拉式清單</span><span class="sxs-lookup"><span data-stu-id="0241c-128">CBS\_DROPDOWN</span></span>
-   <span data-ttu-id="0241c-129">CBS \_ DROPDOWNLIST</span><span class="sxs-lookup"><span data-stu-id="0241c-129">CBS\_DROPDOWNLIST</span></span>
-   <span data-ttu-id="0241c-130">WS \_ 子系</span><span class="sxs-lookup"><span data-stu-id="0241c-130">WS\_CHILD</span></span>

<span data-ttu-id="0241c-131">另外還有數個 [ComboBoxEx 控制項延伸樣式](comboboxex-control-extended-styles.md) ，只供 ComboBoxEx 使用。</span><span class="sxs-lookup"><span data-stu-id="0241c-131">There are also several [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) that are used only by ComboBoxEx.</span></span>

> [!Note]  
> <span data-ttu-id="0241c-132">在某些情況下， [**CBS \_ 簡單**](combo-box-styles.md) 樣式可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0241c-132">The [**CBS\_SIMPLE**](combo-box-styles.md) style may not work properly in some cases.</span></span>

 

<span data-ttu-id="0241c-133">由於 ComboBoxEx 控制項會根據指派的影像清單，為您執行「擁有者」繪製工作，因此會隱含 [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) 樣式; 您在建立控制項時不需要使用它。</span><span class="sxs-lookup"><span data-stu-id="0241c-133">Because the ComboBoxEx control performs owner draw tasks for you based on an assigned image list, the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style is implied; you need not use it when creating the control.</span></span> <span data-ttu-id="0241c-134">因為影像清單是用來提供專案圖形，所以無法使用 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式。</span><span class="sxs-lookup"><span data-stu-id="0241c-134">Because image lists are used to provide item graphics, the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style cannot be used.</span></span> <span data-ttu-id="0241c-135">ComboBoxEx 控制項也支援 [ComboBoxEx 控制項擴充樣式](comboboxex-control-extended-styles.md) ，以提供額外的功能。</span><span class="sxs-lookup"><span data-stu-id="0241c-135">The ComboBoxEx control also supports [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) that provide additional features.</span></span>

## <a name="comboboxex-control-items"></a><span data-ttu-id="0241c-136">ComboBoxEx 控制項專案</span><span class="sxs-lookup"><span data-stu-id="0241c-136">ComboBoxEx Control Items</span></span>

<span data-ttu-id="0241c-137">ComboBoxEx 控制項會使用 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構來維護專案資訊。</span><span class="sxs-lookup"><span data-stu-id="0241c-137">ComboBoxEx controls maintain item information using a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="0241c-138">此結構包含專案索引、影像索引 (正常、選取狀態和重迭) 、縮排值、文字字串和專案特定值的成員。</span><span class="sxs-lookup"><span data-stu-id="0241c-138">This structure includes members for item indexes, image indexes (normal, selection state, and overlay), indentation values, text strings, and item-specific values.</span></span>

<span data-ttu-id="0241c-139">ComboBoxEx 控制項可讓您輕鬆地透過訊息存取和操作專案。</span><span class="sxs-lookup"><span data-stu-id="0241c-139">The ComboBoxEx control provides easy access to and manipulation of items through messaging.</span></span> <span data-ttu-id="0241c-140">若要加入或刪除專案，請傳送 [**CBEM \_ INSERTITEM**](cbem-insertitem.md) 或 [**CBEM \_ DELETEITEM**](cbem-deleteitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0241c-140">To add or delete an item, send the [**CBEM\_INSERTITEM**](cbem-insertitem.md) or [**CBEM\_DELETEITEM**](cbem-deleteitem.md) message.</span></span> <span data-ttu-id="0241c-141">您可以使用 [**CBEM \_ SETITEM**](cbem-setitem.md) 訊息來修改目前在控制項中的專案。</span><span class="sxs-lookup"><span data-stu-id="0241c-141">You can modify items currently in the control using the [**CBEM\_SETITEM**](cbem-setitem.md) message.</span></span>

## <a name="callback-items"></a><span data-ttu-id="0241c-142">回呼專案</span><span class="sxs-lookup"><span data-stu-id="0241c-142">Callback Items</span></span>

<span data-ttu-id="0241c-143">ComboBoxEx 控制項支援回呼專案屬性。</span><span class="sxs-lookup"><span data-stu-id="0241c-143">ComboBoxEx controls support callback item attributes.</span></span> <span data-ttu-id="0241c-144">當您使用 [**CBEM \_ INSERTITEM**](cbem-insertitem.md)將專案新增至控制項時，您可以將它指定為回呼專案。</span><span class="sxs-lookup"><span data-stu-id="0241c-144">You can specify an item as a callback item when you add it to the control using [**CBEM\_INSERTITEM**](cbem-insertitem.md).</span></span> <span data-ttu-id="0241c-145">當您將值指派給專案的 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) 結構時，您必須指定適當的回呼旗標值。</span><span class="sxs-lookup"><span data-stu-id="0241c-145">When you assign values to an item's [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, you must specify the appropriate callback flag values.</span></span> <span data-ttu-id="0241c-146">以下是 **COMBOBOXEXITEM** 結構成員及其對應的回呼旗標值。</span><span class="sxs-lookup"><span data-stu-id="0241c-146">The following are **COMBOBOXEXITEM** structure members and their corresponding callback flag values.</span></span>



| <span data-ttu-id="0241c-147">成員</span><span class="sxs-lookup"><span data-stu-id="0241c-147">Member</span></span>             | <span data-ttu-id="0241c-148">回呼值</span><span class="sxs-lookup"><span data-stu-id="0241c-148">Callback value</span></span>      |
|--------------------|---------------------|
| <span data-ttu-id="0241c-149">**pszText**</span><span class="sxs-lookup"><span data-stu-id="0241c-149">**pszText**</span></span>        | <span data-ttu-id="0241c-150">LPSTR \_ TEXTCALLBACK</span><span class="sxs-lookup"><span data-stu-id="0241c-150">LPSTR\_TEXTCALLBACK</span></span> |
| <span data-ttu-id="0241c-151">**iImage**</span><span class="sxs-lookup"><span data-stu-id="0241c-151">**iImage**</span></span>         | <span data-ttu-id="0241c-152">我 \_ IMAGECALLBACK</span><span class="sxs-lookup"><span data-stu-id="0241c-152">I\_IMAGECALLBACK</span></span>    |
| <span data-ttu-id="0241c-153">**iSelectedImage**</span><span class="sxs-lookup"><span data-stu-id="0241c-153">**iSelectedImage**</span></span> | <span data-ttu-id="0241c-154">我 \_ IMAGECALLBACK</span><span class="sxs-lookup"><span data-stu-id="0241c-154">I\_IMAGECALLBACK</span></span>    |
| <span data-ttu-id="0241c-155">**iOverlay**</span><span class="sxs-lookup"><span data-stu-id="0241c-155">**iOverlay**</span></span>       | <span data-ttu-id="0241c-156">我 \_ IMAGECALLBACK</span><span class="sxs-lookup"><span data-stu-id="0241c-156">I\_IMAGECALLBACK</span></span>    |
| <span data-ttu-id="0241c-157">**iIndent**</span><span class="sxs-lookup"><span data-stu-id="0241c-157">**iIndent**</span></span>        | <span data-ttu-id="0241c-158">我 \_ INDENTCALLBACK</span><span class="sxs-lookup"><span data-stu-id="0241c-158">I\_INDENTCALLBACK</span></span>   |



 

<span data-ttu-id="0241c-159">控制項將會透過傳送 [CBEN \_ GETDISPINFO](cben-getdispinfo.md) 通知碼來要求回呼專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0241c-159">The control will request information about callback items by sending [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification codes.</span></span> <span data-ttu-id="0241c-160">此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="0241c-160">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <span data-ttu-id="0241c-161">當您的應用程式處理此訊息時，它必須提供控制項要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="0241c-161">When your application processes this message, it must provide the requested information for the control.</span></span> <span data-ttu-id="0241c-162">如果您將隨附 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **mask** 成員設定為 CBEIF \_ DI \_ SETITEM，控制項將會儲存專案資料，而且不會再次要求它。</span><span class="sxs-lookup"><span data-stu-id="0241c-162">If you set the **mask** member of the accompanying [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control will store the item data and will not request it again.</span></span>

## <a name="comboboxex-control-image-lists"></a><span data-ttu-id="0241c-163">ComboBoxEx 控制項影像清單</span><span class="sxs-lookup"><span data-stu-id="0241c-163">ComboBoxEx Control Image Lists</span></span>

<span data-ttu-id="0241c-164">如果您想要讓 ComboBoxEx 控制項顯示具有專案的圖示，您必須提供影像清單。</span><span class="sxs-lookup"><span data-stu-id="0241c-164">If you want a ComboBoxEx control to display icons with items, you must provide an image list.</span></span> <span data-ttu-id="0241c-165">ComboBoxEx 控制項最多支援三個專案的影像-一個用於其選取狀態、一個用於其 nonselected 狀態，另一個用於重迭影像。</span><span class="sxs-lookup"><span data-stu-id="0241c-165">ComboBoxEx controls support up to three images for an item—one for its selected state, one for its nonselected state, and one for an overlay image.</span></span> <span data-ttu-id="0241c-166">使用 [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) 訊息，將現有的影像清單指派給 ComboBoxEx 控制項。</span><span class="sxs-lookup"><span data-stu-id="0241c-166">Assign an existing image list to a ComboBoxEx control using the [**CBEM\_SETIMAGELIST**](cbem-setimagelist.md) message.</span></span>

<span data-ttu-id="0241c-167">[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構包含成員，這些成員代表每個影像清單 (選取、未選取和重迭) 的影像索引。</span><span class="sxs-lookup"><span data-stu-id="0241c-167">The [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure contains members that represent the image indexes for each image list (selected, unselected, and overlay).</span></span> <span data-ttu-id="0241c-168">針對每個專案，設定這些成員以顯示所需的影像。</span><span class="sxs-lookup"><span data-stu-id="0241c-168">For each item, set these members to display the desired images.</span></span> <span data-ttu-id="0241c-169">不需要為每個影像類型指定影像索引。</span><span class="sxs-lookup"><span data-stu-id="0241c-169">It is not necessary to specify image indexes for each type of image.</span></span> <span data-ttu-id="0241c-170">您可以依需要混合和比對影像類型，但請一律設定 **COMBOBOXEXITEM** 結構的 **遮罩** 成員，以指出正在使用哪些成員。</span><span class="sxs-lookup"><span data-stu-id="0241c-170">You can mix and match image types as you like, but always set the **mask** member of the **COMBOBOXEXITEM** structure to indicate which members are being used.</span></span> <span data-ttu-id="0241c-171">控制項會忽略未標示為有效的成員。</span><span class="sxs-lookup"><span data-stu-id="0241c-171">The control ignores members that have not been flagged as valid.</span></span>

> [!Note]  
> <span data-ttu-id="0241c-172">如果您使用 [**CBS \_ 簡單**](combo-box-styles.md) 樣式，則不會顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="0241c-172">If you use the [**CBS\_SIMPLE**](combo-box-styles.md) style, icons are not displayed.</span></span>

 

## <a name="about-comboboxex-control-notification-messages"></a><span data-ttu-id="0241c-173">關於 ComboBoxEx 控制通知訊息</span><span class="sxs-lookup"><span data-stu-id="0241c-173">About ComboBoxEx Control Notification Messages</span></span>

<span data-ttu-id="0241c-174">ComboBoxEx 控制項會傳送通知訊息，以在本身或要求回呼專案資訊中報告變更。</span><span class="sxs-lookup"><span data-stu-id="0241c-174">A ComboBoxEx control sends notification messages to report changes within itself or to request callback item information.</span></span> <span data-ttu-id="0241c-175">控制項的父系會從包含在 ComboBoxEx 控制項內的下拉式方塊接收所有的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。</span><span class="sxs-lookup"><span data-stu-id="0241c-175">The parent of the control receives all [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from the combo box contained within the ComboBoxEx control.</span></span> <span data-ttu-id="0241c-176">ComboBoxEx 控制項會使用 [**WM \_ 通知**](wm-notify.md) 訊息傳送自己的通知。</span><span class="sxs-lookup"><span data-stu-id="0241c-176">The ComboBoxEx control sends its own notifications using [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="0241c-177">因此，控制項的擁有者必須準備好處理這兩種形式的通知訊息。</span><span class="sxs-lookup"><span data-stu-id="0241c-177">As a result, the control's owner must be prepared to process both forms of notification messages.</span></span>

<span data-ttu-id="0241c-178">以下是透過 [**WM \_ 通知**](wm-notify.md) 訊息傳送的 ComboBoxEx 特定通知碼。</span><span class="sxs-lookup"><span data-stu-id="0241c-178">Following are the ComboBoxEx-specific notification codes that are sent through [**WM\_NOTIFY**](wm-notify.md) messages.</span></span>



| <span data-ttu-id="0241c-179">通知</span><span class="sxs-lookup"><span data-stu-id="0241c-179">Notification</span></span>                              | <span data-ttu-id="0241c-180">**說明**</span><span class="sxs-lookup"><span data-stu-id="0241c-180">**Description**</span></span>                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0241c-181">CBEN \_ BEGINEDIT</span><span class="sxs-lookup"><span data-stu-id="0241c-181">CBEN\_BEGINEDIT</span></span>](cben-beginedit.md)     | <span data-ttu-id="0241c-182">通知使用者已啟動下拉式清單，或按一下控制項的編輯方塊。</span><span class="sxs-lookup"><span data-stu-id="0241c-182">Signals that the user has activated the drop-down list or clicked in the control's edit box.</span></span>                               |
| [<span data-ttu-id="0241c-183">CBEN \_ ENDEDIT</span><span class="sxs-lookup"><span data-stu-id="0241c-183">CBEN\_ENDEDIT</span></span>](cben-endedit.md)         | <span data-ttu-id="0241c-184">表示使用者已從下拉式清單中選取專案，或已結束編輯方塊中的編輯作業。</span><span class="sxs-lookup"><span data-stu-id="0241c-184">Signals that the user has selected an item from the drop-down list or has concluded an edit operation within the edit box.</span></span> |
| [<span data-ttu-id="0241c-185">CBEN \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="0241c-185">CBEN\_DELETEITEM</span></span>](cben-deleteitem.md)   | <span data-ttu-id="0241c-186">報告已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="0241c-186">Reports that an item was deleted.</span></span>                                                                                          |
| [<span data-ttu-id="0241c-187">CBEN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="0241c-187">CBEN\_GETDISPINFO</span></span>](cben-getdispinfo.md) | <span data-ttu-id="0241c-188">要求專案屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0241c-188">Requests information about an item's attributes.</span></span>                                                                           |
| [<span data-ttu-id="0241c-189">CBEN \_ INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="0241c-189">CBEN\_INSERTITEM</span></span>](cben-insertitem.md)   | <span data-ttu-id="0241c-190">指出專案已插入控制項中的信號。</span><span class="sxs-lookup"><span data-stu-id="0241c-190">Signals that an item was inserted in the control.</span></span>                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a><span data-ttu-id="0241c-191">ComboBoxEx 控制訊息轉送</span><span class="sxs-lookup"><span data-stu-id="0241c-191">ComboBoxEx Control Message Forwarding</span></span>

<span data-ttu-id="0241c-192">以下是 ComboBoxEx 控制項轉送至其子下拉式方塊的標準下拉式方塊訊息。</span><span class="sxs-lookup"><span data-stu-id="0241c-192">The following are the standard combo box messages that a ComboBoxEx control forwards to its child combo box.</span></span> <span data-ttu-id="0241c-193">在轉送訊息之前或之後，ComboBoxEx 控制項可能會處理其中某些訊息。</span><span class="sxs-lookup"><span data-stu-id="0241c-193">Some of these messages may be processed by the ComboBoxEx control either before or after the message has been forwarded.</span></span>

-   [<span data-ttu-id="0241c-194">**CB \_ DELETESTRING**</span><span class="sxs-lookup"><span data-stu-id="0241c-194">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
-   [<span data-ttu-id="0241c-195">**CB \_ FINDSTRINGEXACT**</span><span class="sxs-lookup"><span data-stu-id="0241c-195">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
-   [<span data-ttu-id="0241c-196">**CB \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="0241c-196">**CB\_GETCOUNT**</span></span>](cb-getcount.md)
-   [<span data-ttu-id="0241c-197">**CB \_ GETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="0241c-197">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
-   [<span data-ttu-id="0241c-198">**CB \_ GETDROPPEDCONTROLRECT**</span><span class="sxs-lookup"><span data-stu-id="0241c-198">**CB\_GETDROPPEDCONTROLRECT**</span></span>](cb-getdroppedcontrolrect.md)
-   [<span data-ttu-id="0241c-199">**CB \_ GETDROPPEDSTATE**</span><span class="sxs-lookup"><span data-stu-id="0241c-199">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
-   [<span data-ttu-id="0241c-200">**CB \_ GETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="0241c-200">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
-   [<span data-ttu-id="0241c-201">**CB \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="0241c-201">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
-   [<span data-ttu-id="0241c-202">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="0241c-202">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="0241c-203">**CB \_ GETLBTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="0241c-203">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
-   [<span data-ttu-id="0241c-204">**CB \_ GETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="0241c-204">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
-   [<span data-ttu-id="0241c-205">**CB \_ LIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="0241c-205">**CB\_LIMITTEXT**</span></span>](cb-limittext.md)
-   [<span data-ttu-id="0241c-206">**CB \_ RESETCONTENT**</span><span class="sxs-lookup"><span data-stu-id="0241c-206">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
-   [<span data-ttu-id="0241c-207">**CB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="0241c-207">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
-   [<span data-ttu-id="0241c-208">**CB \_ SETDROPPEDWIDTH**</span><span class="sxs-lookup"><span data-stu-id="0241c-208">**CB\_SETDROPPEDWIDTH**</span></span>](cb-setdroppedwidth.md)
-   [<span data-ttu-id="0241c-209">**CB \_ SETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="0241c-209">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
-   [<span data-ttu-id="0241c-210">**CB \_ SETITEMDATA**</span><span class="sxs-lookup"><span data-stu-id="0241c-210">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
-   [<span data-ttu-id="0241c-211">**CB \_ SETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="0241c-211">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
-   [<span data-ttu-id="0241c-212">**CB \_ SHOWDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="0241c-212">**CB\_SHOWDROPDOWN**</span></span>](cb-showdropdown.md)

<span data-ttu-id="0241c-213">以下是 ComboBoxEx 控制項轉送至其父視窗的 windows 訊息：</span><span class="sxs-lookup"><span data-stu-id="0241c-213">Following are the windows messages that a ComboBoxEx control forwards to its parent window:</span></span>

-   <span data-ttu-id="0241c-214">[**WM \_命令**](/windows/desktop/menurc/wm-command) (其中包含所有 CBN \_ 通知。 ) </span><span class="sxs-lookup"><span data-stu-id="0241c-214">[**WM\_COMMAND**](/windows/desktop/menurc/wm-command) (This includes all of the CBN\_ notifications.)</span></span>
-   [<span data-ttu-id="0241c-215">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="0241c-215">**WM\_NOTIFY**</span></span>](wm-notify.md)

 

 