---
title: 如何自訂工具列
description: 大部分的 Windows 應用程式都使用工具列控制項，讓使用者能夠輕鬆存取程式功能。
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104023192"
---
# <a name="how-to-customize-toolbars"></a><span data-ttu-id="bd13f-103">如何自訂工具列</span><span class="sxs-lookup"><span data-stu-id="bd13f-103">How to Customize Toolbars</span></span>

<span data-ttu-id="bd13f-104">大部分的 Windows 應用程式都使用工具列控制項，讓使用者能夠輕鬆存取程式功能。</span><span class="sxs-lookup"><span data-stu-id="bd13f-104">Most Windows-based applications use toolbar controls to provide users with convenient access to the program functionality.</span></span> <span data-ttu-id="bd13f-105">不過，靜態工具列有一些缺點，例如，沒有足夠的空間可有效顯示所有可用的工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-105">However, static toolbars have some shortcomings—such as too little space to effectively display all the available tools.</span></span> <span data-ttu-id="bd13f-106">解決此問題的方法是讓應用程式的工具列成為使用者可自訂的。</span><span class="sxs-lookup"><span data-stu-id="bd13f-106">The solution to this problem is to make your application's toolbars user-customizable.</span></span> <span data-ttu-id="bd13f-107">然後，使用者可以選擇只顯示所需的工具，並以適合其個人工作型態的方式來組織它們。</span><span class="sxs-lookup"><span data-stu-id="bd13f-107">Then, users can choose to display only the tools they need, and they can organize them in a way that suits their personal workstyle.</span></span>

> [!Note]  
> <span data-ttu-id="bd13f-108">對話方塊中的工具列無法自訂。</span><span class="sxs-lookup"><span data-stu-id="bd13f-108">Toolbars in dialog boxes cannot be customized.</span></span>

 

<span data-ttu-id="bd13f-109">若要啟用自訂，請在建立工具列控制項時，加入 [**CCS 可 \_ 調整**](common-control-styles.md) 的通用控制項樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="bd13f-109">To enable customization, include the [**CCS\_ADJUSTABLE**](common-control-styles.md) common controls style flag when you create the toolbar control.</span></span> <span data-ttu-id="bd13f-110">自訂的基本方法有兩種：</span><span class="sxs-lookup"><span data-stu-id="bd13f-110">There are two basic approaches to customization:</span></span>

-   <span data-ttu-id="bd13f-111">[自訂] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-111">The customization dialog box.</span></span> <span data-ttu-id="bd13f-112">這個系統提供的對話方塊是最簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="bd13f-112">This system-provided dialog box is the simplest approach.</span></span> <span data-ttu-id="bd13f-113">它可為使用者提供圖形化使用者介面，讓他們可以新增、刪除或移動圖示。</span><span class="sxs-lookup"><span data-stu-id="bd13f-113">It gives users a graphical user interface that allows them to add, delete, or move icons.</span></span>
-   <span data-ttu-id="bd13f-114">拖放工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-114">Dragging and dropping tools.</span></span> <span data-ttu-id="bd13f-115">執行拖放功能，可讓使用者將工具移至工具列上的另一個位置，或將其拖曳至工具列上以將其刪除。</span><span class="sxs-lookup"><span data-stu-id="bd13f-115">Implementing drag-and-drop functionality allows users to move tools to another location on the toolbar or delete them by dragging them off the toolbar.</span></span> <span data-ttu-id="bd13f-116">它為使用者提供快速且輕鬆的方式來組織其工具列，但不允許他們新增工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-116">It provides users a quick and easy way to organize their toolbar, but does not allow them to add tools.</span></span>

<span data-ttu-id="bd13f-117">您可以根據應用程式的需求，執行任一種方法或兩者。</span><span class="sxs-lookup"><span data-stu-id="bd13f-117">You can implement either approach or both, depending on the needs of the application.</span></span> <span data-ttu-id="bd13f-118">這兩種自訂方法都不會提供內建機制（例如 [取消] 或 [復原] 按鈕），讓工具列回到先前的狀態。</span><span class="sxs-lookup"><span data-stu-id="bd13f-118">Neither of these two approaches to customization provides a built-in mechanism, such as a Cancel or Undo button, to return the toolbar to its former state.</span></span> <span data-ttu-id="bd13f-119">您必須明確地使用工具列控制項 API 來儲存工具列的 precustomization 狀態。</span><span class="sxs-lookup"><span data-stu-id="bd13f-119">You must explicitly use the toolbar control API to store the toolbar's precustomization state.</span></span> <span data-ttu-id="bd13f-120">如有必要，您可以在稍後使用此儲存的資訊，將工具列還原為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="bd13f-120">If necessary, you can later use this stored information to restore the toolbar to its original state.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bd13f-121">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="bd13f-121">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bd13f-122">技術</span><span class="sxs-lookup"><span data-stu-id="bd13f-122">Technologies</span></span>

-   [<span data-ttu-id="bd13f-123">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="bd13f-123">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bd13f-124">必要條件</span><span class="sxs-lookup"><span data-stu-id="bd13f-124">Prerequisites</span></span>

-   <span data-ttu-id="bd13f-125">C/C++</span><span class="sxs-lookup"><span data-stu-id="bd13f-125">C/C++</span></span>
-   <span data-ttu-id="bd13f-126">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="bd13f-126">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bd13f-127">指示</span><span class="sxs-lookup"><span data-stu-id="bd13f-127">Instructions</span></span>

### <a name="customization-dialog-box"></a><span data-ttu-id="bd13f-128">自訂對話方塊</span><span class="sxs-lookup"><span data-stu-id="bd13f-128">Customization Dialog Box</span></span>

<span data-ttu-id="bd13f-129">[自訂] 對話方塊是由工具列控制項提供，可讓使用者以簡單的方式加入、移動或移除工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-129">The customization dialog box is provided by the toolbar control to give users a simple way to add, move, or delete tools.</span></span> <span data-ttu-id="bd13f-130">使用者可以按兩下工具列來啟動它。</span><span class="sxs-lookup"><span data-stu-id="bd13f-130">Users can launch it by double-clicking the toolbar.</span></span> <span data-ttu-id="bd13f-131">應用程式可以藉由傳送一個 [**TB \_ 自訂**](tb-customize.md) 訊息的工具列控制項，以程式設計方式啟動 [自訂] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-131">Applications can launch the customization dialog box programmatically by sending the toolbar control a [**TB\_CUSTOMIZE**](tb-customize.md) message.</span></span>

<span data-ttu-id="bd13f-132">下圖顯示 [工具列自訂] 對話方塊的範例。</span><span class="sxs-lookup"><span data-stu-id="bd13f-132">The following illustration shows an example of the toolbar customization dialog box.</span></span>

![具有三個專案工具列之視窗的螢幕擷取畫面，以及一個對話方塊，其中包含 [可用] 和 [目前] 工具列按鈕的清單](images/tb-customdlg.png)

<span data-ttu-id="bd13f-134">右邊清單方塊中的工具是目前在工具列上的工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-134">The tools in the list box on the right are those currently on the toolbar.</span></span> <span data-ttu-id="bd13f-135">一開始，此清單將包含您在建立工具列時所指定的工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-135">Initially, this list will contain the tools that you specify when you create the toolbar.</span></span> <span data-ttu-id="bd13f-136">左邊的清單方塊包含可新增至工具列的工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-136">The list box in the left contains the tools that are available to add to the toolbar.</span></span> <span data-ttu-id="bd13f-137">您的應用程式會負責將清單填入 (除了分隔符號之外，它會自動) 。</span><span class="sxs-lookup"><span data-stu-id="bd13f-137">Your application is responsible for populating that list (other than with the Separator, which appears automatically).</span></span>

<span data-ttu-id="bd13f-138">Toolbar 控制項會透過傳送 [TBN \_ BEGINADJUST](tbn-beginadjust.md) 通知碼，後面接著 [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) 通知碼的父視窗，來通知您的應用程式正在啟動自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-138">The toolbar control notifies your application that it is launching a customization dialog box by sending its parent window a [TBN\_BEGINADJUST](tbn-beginadjust.md) notification code followed by a [TBN\_INITCUSTOMIZE](tbn-initcustomize.md) notification code.</span></span> <span data-ttu-id="bd13f-139">在大多數情況下，應用程式不需要回應這些通知代碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-139">In most cases, the application does not need to respond to these notification codes.</span></span> <span data-ttu-id="bd13f-140">但是，如果您不想要 [自訂工具列] 對話方塊顯示 [說明] 按鈕，請藉由傳回 TBNRF HIDEHELP 來處理 TBN \_ INITCUSTOMIZE \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd13f-140">However, if you do not want the Customize Toolbar dialog box to display a Help button, handle TBN\_INITCUSTOMIZE by returning TBNRF\_HIDEHELP.</span></span>

<span data-ttu-id="bd13f-141">工具列控制項接著會依下列順序傳送三系列通知碼，以收集初始化對話方塊所需的資訊：</span><span class="sxs-lookup"><span data-stu-id="bd13f-141">The toolbar control then collects the information it needs to initialize the dialog box by sending three series of notification codes, in the following order:</span></span>

-   <span data-ttu-id="bd13f-142">工具列上的每個按鈕的 [TBN \_ QUERYINSERT](tbn-queryinsert.md) 通知碼，以決定可以插入按鈕的位置。</span><span class="sxs-lookup"><span data-stu-id="bd13f-142">A [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code for each button on the toolbar to determine where buttons can be inserted.</span></span> <span data-ttu-id="bd13f-143">傳回 **FALSE** 以防止在通知訊息中指定的按鈕左邊插入按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-143">Return **FALSE** to prevent a button from being inserted to the left of the button specified in the notification message.</span></span> <span data-ttu-id="bd13f-144">如果您對所有 TBN \_ QUERYINSERT 通知碼傳回 FALSE，則不會顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-144">If you return **FALSE** to all TBN\_QUERYINSERT notification codes, the dialog box will not be displayed.</span></span>
-   <span data-ttu-id="bd13f-145">[TBN 會 \_ QUERYDELETE](tbn-querydelete.md)目前在工具列上的每個工具的通知碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-145">A [TBN\_QUERYDELETE](tbn-querydelete.md) notification code for each tool that is currently on the toolbar.</span></span> <span data-ttu-id="bd13f-146">如果可以移除工具，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bd13f-146">Return **TRUE** if a tool can be deleted, or **FALSE** if not.</span></span>
-   <span data-ttu-id="bd13f-147">一系列的 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) 通知程式碼，用來填入可用按鈕的清單。</span><span class="sxs-lookup"><span data-stu-id="bd13f-147">A series of [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification codes to populate the list of available buttons.</span></span> <span data-ttu-id="bd13f-148">若要將按鈕加入至清單，請填入以通知碼傳遞的 [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) 結構，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="bd13f-148">To add a button to the list, fill in the [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that is passed with the notification code and return **TRUE**.</span></span> <span data-ttu-id="bd13f-149">當您沒有其他工具可新增時，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bd13f-149">When you have no more tools to add, return **FALSE**.</span></span> <span data-ttu-id="bd13f-150">請注意，您可以傳回工具列上已有按鈕的資訊;這些按鈕將不會新增至清單。</span><span class="sxs-lookup"><span data-stu-id="bd13f-150">Note that you can return information for buttons that are already on the toolbar; these buttons will not be added to the list.</span></span>

<span data-ttu-id="bd13f-151">接著會顯示對話方塊，而且使用者可以開始自訂工具列。</span><span class="sxs-lookup"><span data-stu-id="bd13f-151">The dialog box is then displayed, and the user can begin to customize the toolbar.</span></span>

<span data-ttu-id="bd13f-152">當對話方塊開啟時，您的應用程式可以根據使用者的動作收到各種通知碼：</span><span class="sxs-lookup"><span data-stu-id="bd13f-152">When the dialog box is open, your application can receive a variety of notification codes, depending on the user's actions:</span></span>

-   <span data-ttu-id="bd13f-153">[TBN \_QUERYINSERT](tbn-queryinsert.md)。</span><span class="sxs-lookup"><span data-stu-id="bd13f-153">[TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="bd13f-154">使用者已變更工具列上的工具位置或新增工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-154">The user has changed the location of a tool on the toolbar or added a tool.</span></span> <span data-ttu-id="bd13f-155">傳回 **FALSE** 以防止工具插入至該位置。</span><span class="sxs-lookup"><span data-stu-id="bd13f-155">Return **FALSE** to prevent the tool from being inserted at that location.</span></span>
-   <span data-ttu-id="bd13f-156">[TBN \_DELETINGBUTTON](tbn-deletingbutton.md)。</span><span class="sxs-lookup"><span data-stu-id="bd13f-156">[TBN\_DELETINGBUTTON](tbn-deletingbutton.md).</span></span> <span data-ttu-id="bd13f-157">使用者即將從工具列移除工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-157">The user is about to remove a tool from the toolbar.</span></span>
-   <span data-ttu-id="bd13f-158">[TBN \_CUSTHELP](tbn-custhelp.md)。</span><span class="sxs-lookup"><span data-stu-id="bd13f-158">[TBN\_CUSTHELP](tbn-custhelp.md).</span></span> <span data-ttu-id="bd13f-159">使用者按一下 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-159">The user has clicked the Help button.</span></span>
-   <span data-ttu-id="bd13f-160">[TBN \_TOOLBARCHANGE](tbn-toolbarchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bd13f-160">[TBN\_TOOLBARCHANGE](tbn-toolbarchange.md).</span></span> <span data-ttu-id="bd13f-161">使用者已新增、移動或移除工具。</span><span class="sxs-lookup"><span data-stu-id="bd13f-161">The user has added, moved, or deleted a tool.</span></span>
-   <span data-ttu-id="bd13f-162">[TBN \_重設](tbn-reset.md)。</span><span class="sxs-lookup"><span data-stu-id="bd13f-162">[TBN\_RESET](tbn-reset.md).</span></span> <span data-ttu-id="bd13f-163">使用者按一下 [重設] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-163">The user has clicked the Reset button.</span></span>

<span data-ttu-id="bd13f-164">終結對話方塊之後，您的應用程式將會收到 [TBN \_ ENDADJUST](tbn-endadjust.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-164">After the dialog box is destroyed, your application will receive a [TBN\_ENDADJUST](tbn-endadjust.md) notification code.</span></span>

<span data-ttu-id="bd13f-165">下列程式碼範例示範一個方法來執行工具列自訂。</span><span class="sxs-lookup"><span data-stu-id="bd13f-165">The following code example shows one way to implement toolbar customization.</span></span>


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a><span data-ttu-id="bd13f-166">拖放工具</span><span class="sxs-lookup"><span data-stu-id="bd13f-166">Dragging and Dropping Tools</span></span>

<span data-ttu-id="bd13f-167">使用者也可以按下 SHIFT 鍵，然後將按鈕拖曳到另一個位置，來重新排列工具列上的按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-167">Users can also rearrange the buttons on a toolbar by pressing the SHIFT key and dragging the button to another location.</span></span> <span data-ttu-id="bd13f-168">拖放進程會由工具列控制項自動處理。</span><span class="sxs-lookup"><span data-stu-id="bd13f-168">The drag-and-drop process is handled automatically by the toolbar control.</span></span> <span data-ttu-id="bd13f-169">它會在拖曳時顯示按鈕的准刪除影像，並在卸載後重新排列工具列。</span><span class="sxs-lookup"><span data-stu-id="bd13f-169">It displays a ghost image of the button as it is dragged, and rearranges the toolbar after it is dropped.</span></span> <span data-ttu-id="bd13f-170">使用者無法以這種方式加入按鈕，但可以藉由將按鈕放在工具列上來刪除按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-170">Users cannot add buttons in this way, but they can delete a button by dropping it off the toolbar.</span></span>

<span data-ttu-id="bd13f-171">雖然工具列控制項通常會自動執行此作業，但它也會將您的應用程式傳送至兩個通知碼： [TBN \_ QUERYDELETE](tbn-querydelete.md) 和 [TBN \_ QUERYINSERT](tbn-queryinsert.md)。</span><span class="sxs-lookup"><span data-stu-id="bd13f-171">Although the toolbar control normally does this operation automatically, it also sends your application two notification codes: [TBN\_QUERYDELETE](tbn-querydelete.md) and [TBN\_QUERYINSERT](tbn-queryinsert.md).</span></span> <span data-ttu-id="bd13f-172">若要控制拖放程式，請依照下列方式處理這些通知碼：</span><span class="sxs-lookup"><span data-stu-id="bd13f-172">To control the drag-and-drop process, handle these notification codes as follows:</span></span>

-   <span data-ttu-id="bd13f-173">[TBN \_ QUERYDELETE](tbn-querydelete.md)通知碼會在使用者嘗試移動按鈕時立即傳送，然後才會顯示 [准刪除] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-173">The [TBN\_QUERYDELETE](tbn-querydelete.md) notification code is sent as soon as the user attempts to move the button, before the ghost button is displayed.</span></span> <span data-ttu-id="bd13f-174">傳回 **FALSE** 以防止移動按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-174">Return **FALSE** to prevent the button from being moved.</span></span> <span data-ttu-id="bd13f-175">如果您傳回 **TRUE**，則使用者將可以移動工具或將它刪除，方法是將它放在工具列上。</span><span class="sxs-lookup"><span data-stu-id="bd13f-175">If you return **TRUE**, the user will be able to either move the tool or delete it by dropping it off the toolbar.</span></span> <span data-ttu-id="bd13f-176">如果工具可以移動，就可以將它刪除。</span><span class="sxs-lookup"><span data-stu-id="bd13f-176">If a tool can be moved, it can be deleted.</span></span> <span data-ttu-id="bd13f-177">不過，如果使用者移除工具，工具列控制項會將 [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) 通知程式碼傳送給您的應用程式，此時您可以選擇在其原始位置重新插入按鈕，藉此取消刪除。</span><span class="sxs-lookup"><span data-stu-id="bd13f-177">However, if the user deletes a tool, the toolbar control will send your application a [TBN\_DELETINGBUTTON](tbn-deletingbutton.md) notification code, at which point you can choose to reinsert the button at its original location, thereby canceling the deletion.</span></span>
-   <span data-ttu-id="bd13f-178">當使用者嘗試在工具列上放置按鈕時，會傳送 [TBN \_ QUERYINSERT](tbn-queryinsert.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-178">The [TBN\_QUERYINSERT](tbn-queryinsert.md) notification code is sent when the user attempts to drop the button on the toolbar.</span></span> <span data-ttu-id="bd13f-179">若要防止將移動的按鈕放在通知中所指定按鈕的左邊，請傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bd13f-179">To prevent the button that is being moved from being dropped to the left of the button specified in the notification, return **FALSE**.</span></span> <span data-ttu-id="bd13f-180">如果使用者將工具從工具列卸載，則不會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-180">This notification code is not sent if the user drops the tool off the toolbar.</span></span>

<span data-ttu-id="bd13f-181">如果使用者嘗試拖曳按鈕，但未按下 SHIFT 鍵，工具列控制項將不會處理拖放作業。</span><span class="sxs-lookup"><span data-stu-id="bd13f-181">If the user attempts to drag a button without also pressing the SHIFT key, the toolbar control will not handle the drag-and-drop operation.</span></span> <span data-ttu-id="bd13f-182">不過，它會將 [TBN \_ BEGINDRAG](tbn-begindrag.md) 通知程式碼傳送給您的應用程式，以指示開始拖曳作業，並使用 [TBN \_ ENDDRAG](tbn-enddrag.md) 通知碼來指出結尾。</span><span class="sxs-lookup"><span data-stu-id="bd13f-182">However, it will send your application a [TBN\_BEGINDRAG](tbn-begindrag.md) notification code to indicate the start of a drag operation, and a [TBN\_ENDDRAG](tbn-enddrag.md) notification code to indicate the end.</span></span> <span data-ttu-id="bd13f-183">如果您想要啟用這種形式的拖放，您的應用程式必須處理這些通知代碼、提供必要的使用者介面，以及修改工具列以反映任何變更。</span><span class="sxs-lookup"><span data-stu-id="bd13f-183">If you want to enable this form of drag-and-drop, your application must handle these notification codes, provide the necessary user interface, and modify the toolbar to reflect any changes.</span></span>

### <a name="saving-and-restoring-toolbars"></a><span data-ttu-id="bd13f-184">儲存和還原工具列</span><span class="sxs-lookup"><span data-stu-id="bd13f-184">Saving and Restoring Toolbars</span></span>

<span data-ttu-id="bd13f-185">在自訂工具列的過程中，您的應用程式可能需要儲存資訊，讓您可以將工具列還原為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="bd13f-185">In the process of customizing a toolbar, your application might need to save information so that you can restore the toolbar to its original state.</span></span> <span data-ttu-id="bd13f-186">若要起始儲存或還原工具列狀態，請將 *lParam* 設定為 **TRUE** 的 [**\_ SAVERESTORE**](tb-saverestore.md)訊息傳送給 toolbar 控制項。</span><span class="sxs-lookup"><span data-stu-id="bd13f-186">To initiate saving or restoring a toolbar state, send the toolbar control a [**TB\_SAVERESTORE**](tb-saverestore.md) message with the *lParam* set to **TRUE**.</span></span> <span data-ttu-id="bd13f-187">此訊息的 *lParam* 值會指定您是否要要求儲存或還原作業。</span><span class="sxs-lookup"><span data-stu-id="bd13f-187">The *lParam* value of this message specifies whether you are requesting a save or a restore operation.</span></span> <span data-ttu-id="bd13f-188">傳送訊息之後，有兩種方式可以處理儲存/還原作業：</span><span class="sxs-lookup"><span data-stu-id="bd13f-188">After the message is sent, there are two ways to handle the save/restore operation:</span></span>

-   <span data-ttu-id="bd13f-189">使用通用控制項 [4.72 版](common-control-versions.md) 和更舊版本，您必須執行 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) 處理常式。</span><span class="sxs-lookup"><span data-stu-id="bd13f-189">With common controls [version 4.72](common-control-versions.md) and earlier, you must implement a [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) handler.</span></span> <span data-ttu-id="bd13f-190">工具列控制項會傳送此通知碼，以要求每個按鈕還原時的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-190">The toolbar control sends this notification code to request information about each button as it is restored.</span></span>
-   <span data-ttu-id="bd13f-191">5.80 版包含儲存/還原選項。</span><span class="sxs-lookup"><span data-stu-id="bd13f-191">Version 5.80 includes a save/restore option.</span></span> <span data-ttu-id="bd13f-192">在程式開始時，您的應用程式會在儲存或還原每個按鈕時收到 [TBN \_ 儲存](tbn-save.md) 或 [TBN \_ 還原](tbn-restore.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-192">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification code.</span></span> <span data-ttu-id="bd13f-193">若要使用此選項，您必須執行通知處理常式，以提供成功儲存或還原工具列狀態所需的點陣圖和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-193">To use this option, you must implement notification handlers to provide the bitmap and state information that is needed to successfully save or restore the toolbar state.</span></span>

<span data-ttu-id="bd13f-194">工具列狀態會儲存在資料流程中，其中包含與應用程式定義資料區塊相關聯的 Shell 定義資料區塊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-194">Toolbar states are saved in a data stream that consists of blocks of Shell-defined data alternating with blocks of application-defined data.</span></span> <span data-ttu-id="bd13f-195">每個按鈕都會儲存每個類型的一個資料區塊，以及一個選擇性的全域資料區塊，應用程式可以在資料流程的開頭放置這些資料。</span><span class="sxs-lookup"><span data-stu-id="bd13f-195">One data block of each type is stored for each button, along with an optional block of global data that applications can place at the beginning of the stream.</span></span> <span data-ttu-id="bd13f-196">在儲存程式期間，您的 [TBN \_ 儲存](tbn-save.md) 處理常式會將應用程式定義的區塊新增至資料流程。</span><span class="sxs-lookup"><span data-stu-id="bd13f-196">During the save process, your [TBN\_SAVE](tbn-save.md) handler adds the application-defined blocks to the data stream.</span></span> <span data-ttu-id="bd13f-197">在還原過程中， [TBN \_ 還原](tbn-restore.md) 處理常式會讀取每個區塊，並為 Shell 提供重建工具列所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-197">During the restore process, the [TBN\_RESTORE](tbn-restore.md) handler reads each block and gives the Shell the information it needs to reconstruct the toolbar.</span></span>

### <a name="how-to-handle-a-tbn_save-notification"></a><span data-ttu-id="bd13f-198">如何處理 TBN \_ 儲存通知</span><span class="sxs-lookup"><span data-stu-id="bd13f-198">How to Handle a TBN\_SAVE Notification</span></span>

<span data-ttu-id="bd13f-199">第一個 [TBN \_ 儲存](tbn-save.md) 通知程式碼會在儲存程式的開頭傳送。</span><span class="sxs-lookup"><span data-stu-id="bd13f-199">The first [TBN\_SAVE](tbn-save.md) notification code is sent at the beginning of the save process.</span></span> <span data-ttu-id="bd13f-200">儲存任何按鈕之前， [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) 結構的成員設定如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bd13f-200">Before any buttons are saved, the members of the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure are set as shown in the following table.</span></span>



| <span data-ttu-id="bd13f-201">成員</span><span class="sxs-lookup"><span data-stu-id="bd13f-201">Member</span></span>       | <span data-ttu-id="bd13f-202">設定</span><span class="sxs-lookup"><span data-stu-id="bd13f-202">Setting</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd13f-203">**iItem**</span><span class="sxs-lookup"><span data-stu-id="bd13f-203">**iItem**</span></span>    | <span data-ttu-id="bd13f-204">–1</span><span class="sxs-lookup"><span data-stu-id="bd13f-204">–1</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bd13f-205">**cbData**</span><span class="sxs-lookup"><span data-stu-id="bd13f-205">**cbData**</span></span>   | <span data-ttu-id="bd13f-206">Shell 定義資料所需的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="bd13f-206">The amount of memory needed for Shell-defined data.</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="bd13f-207">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="bd13f-207">**cButtons**</span></span> | <span data-ttu-id="bd13f-208">按鈕的數目。</span><span class="sxs-lookup"><span data-stu-id="bd13f-208">The number of buttons.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bd13f-209">**.Pdata**</span><span class="sxs-lookup"><span data-stu-id="bd13f-209">**pData**</span></span>    | <span data-ttu-id="bd13f-210">應用程式定義資料所需的記憶體計算量。</span><span class="sxs-lookup"><span data-stu-id="bd13f-210">The calculated amount of memory needed for application-defined data.</span></span> <span data-ttu-id="bd13f-211">一般而言，您會包含一些全域資料，再加上每個按鈕的資料。</span><span class="sxs-lookup"><span data-stu-id="bd13f-211">Typically, you include some global data, plus data for each button.</span></span> <span data-ttu-id="bd13f-212">將該值新增至 **cbData** ，並將足夠的記憶體配置給 **.pdata** ，以將其全部保存。</span><span class="sxs-lookup"><span data-stu-id="bd13f-212">Add that value to **cbData** and allocate enough memory to **pData** to hold it all.</span></span>                                                                                                                      |
| <span data-ttu-id="bd13f-213">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="bd13f-213">**pCurrent**</span></span> | <span data-ttu-id="bd13f-214">資料流程中第一個未使用的位元組。</span><span class="sxs-lookup"><span data-stu-id="bd13f-214">The first unused byte in the data stream.</span></span> <span data-ttu-id="bd13f-215">如果您不需要全域工具列資訊，請設定 **pCurrent**  =  **.pdata** ，使它指向資料流程的開頭。</span><span class="sxs-lookup"><span data-stu-id="bd13f-215">If you do not require global toolbar information, set **pCurrent** = **pData** so that it points to the start of the data stream.</span></span> <span data-ttu-id="bd13f-216">如果您確實需要全域工具列資訊，請將它儲存在 **.pdata**，然後將 **pCurrent** 設定為數據串流未使用部分的開頭，然後再返回。</span><span class="sxs-lookup"><span data-stu-id="bd13f-216">If you do require global toolbar information, store it at **pData**, then set **pCurrent** to the beginning of the unused portion of the data stream before returning.</span></span> |



 

<span data-ttu-id="bd13f-217">如果您想要新增一些全域工具列資訊，請將它放在資料流程的開頭。</span><span class="sxs-lookup"><span data-stu-id="bd13f-217">If you want to add some global toolbar information, put it at the start of the data stream.</span></span> <span data-ttu-id="bd13f-218">前進 **pCurrent** 至全域資料的結尾，使其指向資料流程未使用部分的開頭，然後傳回。</span><span class="sxs-lookup"><span data-stu-id="bd13f-218">Advance **pCurrent** to the end of the global data so that it points to the beginning of the unused portion of the data stream, and return.</span></span>

<span data-ttu-id="bd13f-219">傳回之後，Shell 會開始儲存按鈕資訊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-219">After you return, the Shell starts saving button information.</span></span> <span data-ttu-id="bd13f-220">它會在 **pCurrent** 的第一個按鈕新增 Shell 定義的資料，然後將 **pCurrent** 前進到未使用部分的開頭。</span><span class="sxs-lookup"><span data-stu-id="bd13f-220">It adds the Shell-defined data for the first button at **pCurrent** and then advances **pCurrent** to the start of the unused portion.</span></span>

<span data-ttu-id="bd13f-221">儲存每個按鈕之後，會傳送 [TBN \_ 儲存](tbn-save.md) 通知碼，而且會傳回 [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) ，並將這些成員設定如下。</span><span class="sxs-lookup"><span data-stu-id="bd13f-221">After each button is saved, a [TBN\_SAVE](tbn-save.md) notification code is sent and [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) is returned with these members set as follows.</span></span>



| <span data-ttu-id="bd13f-222">成員</span><span class="sxs-lookup"><span data-stu-id="bd13f-222">Member</span></span>                       | <span data-ttu-id="bd13f-223">設定</span><span class="sxs-lookup"><span data-stu-id="bd13f-223">Setting</span></span>                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd13f-224">**iItem**</span><span class="sxs-lookup"><span data-stu-id="bd13f-224">**iItem**</span></span>                    | <span data-ttu-id="bd13f-225">按鈕編號的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="bd13f-225">The zero-based index of the button number.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="bd13f-226">**pCurrent**</span><span class="sxs-lookup"><span data-stu-id="bd13f-226">**pCurrent**</span></span>                 | <span data-ttu-id="bd13f-227">資料流程中第一個未使用之位元組的指標。</span><span class="sxs-lookup"><span data-stu-id="bd13f-227">A pointer to the first unused byte in the data stream.</span></span> <span data-ttu-id="bd13f-228">如果您想要儲存按鈕的其他相關資訊，請將它儲存在 **pCurrent** 所指向的位置，並更新 **pCurrent** 以指向該資料串流的第一個未使用部分。</span><span class="sxs-lookup"><span data-stu-id="bd13f-228">If you want to store additional information about the button, store it at the location pointed to by **pCurrent** and update **pCurrent** to point to the first unused portion of the data stream after that.</span></span> |
| [<span data-ttu-id="bd13f-229">**TBBUTTON**</span><span class="sxs-lookup"><span data-stu-id="bd13f-229">**TBBUTTON**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | <span data-ttu-id="bd13f-230">描述正在儲存之按鈕的 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) 結構。</span><span class="sxs-lookup"><span data-stu-id="bd13f-230">A [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that describes the button that is being saved.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="bd13f-231">當您收到通知碼時，您應該從 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)中解壓縮任何您需要的按鈕特定資訊。</span><span class="sxs-lookup"><span data-stu-id="bd13f-231">When you receive the notification code, you should extract any button-specific information you need from [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton).</span></span> <span data-ttu-id="bd13f-232">請記住，當您新增按鈕時，可以使用 **TBBUTTON** 的 **dwData** 成員來保存應用程式特定資料。</span><span class="sxs-lookup"><span data-stu-id="bd13f-232">Remember that when you add a button, you can use the **dwData** member of **TBBUTTON** to hold application-specific data.</span></span> <span data-ttu-id="bd13f-233">將您的資料載入資料流程的 **pCurrent**。</span><span class="sxs-lookup"><span data-stu-id="bd13f-233">Load your data into the data stream at **pCurrent**.</span></span> <span data-ttu-id="bd13f-234">將 **pCurrent** 向前移至資料的結尾，再次指向資料流程未使用部分的開頭，然後返回。</span><span class="sxs-lookup"><span data-stu-id="bd13f-234">Advance **pCurrent** to the end of your data, again pointing to the beginning of the unused portion of the stream, and return.</span></span>

<span data-ttu-id="bd13f-235">Shell 接著移至 [下一步] 按鈕，將其資訊新增至 [ **.pdata**]、[前進 **pCurrent**]、[載入 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)]，然後傳送另一個 [TBN \_ 儲存](tbn-save.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="bd13f-235">The Shell then goes to the next button, adds its information to **pData**, advances **pCurrent**, loads [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and sends another [TBN\_SAVE](tbn-save.md) notification code.</span></span> <span data-ttu-id="bd13f-236">此程式會繼續進行，直到儲存所有按鈕為止。</span><span class="sxs-lookup"><span data-stu-id="bd13f-236">This process continues until all buttons are saved.</span></span>

### <a name="restoring-saved-toolbars"></a><span data-ttu-id="bd13f-237">還原已儲存的工具列</span><span class="sxs-lookup"><span data-stu-id="bd13f-237">Restoring Saved Toolbars</span></span>

<span data-ttu-id="bd13f-238">還原程式基本上會反轉儲存流程。</span><span class="sxs-lookup"><span data-stu-id="bd13f-238">The restore process basically reverses the save process.</span></span> <span data-ttu-id="bd13f-239">一開始，您的應用程式將會收到 [TBN \_ 還原](tbn-restore.md)通知碼，其中 [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)結構的 **iItem** 成員會設定為–1。</span><span class="sxs-lookup"><span data-stu-id="bd13f-239">At the beginning, your application will receive a [TBN\_RESTORE](tbn-restore.md) notification code with the **iItem** member of the [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure set to –1.</span></span> <span data-ttu-id="bd13f-240">**CbData** 成員會設定為 **.pdata** 的大小，而 **cButtons** 會設定為按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="bd13f-240">The **cbData** member is set to the size of **pData**, and **cButtons** is set to the number of buttons.</span></span>

<span data-ttu-id="bd13f-241">您的通知處理常式應該將在儲存期間放置於 **.pdata** 開頭的全域資訊解壓縮，並將 **PCurrent** 前進到 Shell 定義資料的第一個區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="bd13f-241">Your notification handler should extract the global information that was placed at the beginning of **pData** during the save, and advance **pCurrent** to the start of the first block of Shell-defined data.</span></span> <span data-ttu-id="bd13f-242">將 **cBytesPerRecord** 設定為您用來儲存按鈕資料的資料區塊大小。</span><span class="sxs-lookup"><span data-stu-id="bd13f-242">Set **cBytesPerRecord** to the size of the data blocks you used to save the button data.</span></span> <span data-ttu-id="bd13f-243">將 **cButtons** 設定為按鈕數目，然後傳回。</span><span class="sxs-lookup"><span data-stu-id="bd13f-243">Set **cButtons** to the number of buttons, and return.</span></span>

<span data-ttu-id="bd13f-244">下一個 [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) 是第一個按鈕。</span><span class="sxs-lookup"><span data-stu-id="bd13f-244">The next [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) is for the first button.</span></span> <span data-ttu-id="bd13f-245">**PCurrent** 成員指向第一個按鈕資料區塊的開頭，而 **iItem** 則設定為按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="bd13f-245">The **pCurrent** member points to the start of your first block of button data, and **iItem** is set to the button index.</span></span> <span data-ttu-id="bd13f-246">將該資料解壓縮，並繼續 **pCurrent**。</span><span class="sxs-lookup"><span data-stu-id="bd13f-246">Extract that data and advance **pCurrent**.</span></span> <span data-ttu-id="bd13f-247">將資料載入 [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)中，然後傳回。</span><span class="sxs-lookup"><span data-stu-id="bd13f-247">Load the data into [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton), and return.</span></span> <span data-ttu-id="bd13f-248">若要從還原的工具列省略按鈕，請將 **TBBUTTON** 的 **idCommand** 成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="bd13f-248">To omit a button from the restored toolbar, set the **idCommand** member of **TBBUTTON** to zero.</span></span> <span data-ttu-id="bd13f-249">Shell 會針對其餘按鈕重複此程式。</span><span class="sxs-lookup"><span data-stu-id="bd13f-249">The Shell will repeat the process for the remaining buttons.</span></span> <span data-ttu-id="bd13f-250">除了 [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) 和 **NMTBRESTORE** 訊息以外，您也可以使用像是 [TBN \_ RESET](tbn-reset.md) 的訊息來儲存和還原工具列。</span><span class="sxs-lookup"><span data-stu-id="bd13f-250">In addition to the [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) and **NMTBRESTORE** messages, you can also use messages such as [TBN\_RESET](tbn-reset.md) to save and restore a toolbar.</span></span>

<span data-ttu-id="bd13f-251">下列程式碼範例會先儲存工具列再進行自訂，並在應用程式收到 [TBN \_ 重設](tbn-reset.md) 訊息時加以還原。</span><span class="sxs-lookup"><span data-stu-id="bd13f-251">The following code example saves a toolbar before it is customized, and restores it if the application receives a [TBN\_RESET](tbn-reset.md) message.</span></span>


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="bd13f-252">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd13f-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd13f-253">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="bd13f-253">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

[<span data-ttu-id="bd13f-254">**工具列標準按鈕影像索引值**</span><span class="sxs-lookup"><span data-stu-id="bd13f-254">**Toolbar Standard Button Image Index Values**</span></span>](toolbar-standard-button-image-index-values.md)
</dt> <dt>

<span data-ttu-id="bd13f-255">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bd13f-255">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




