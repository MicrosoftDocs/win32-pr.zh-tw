---
title: 子類別化控制項
description: 如果控制項幾乎會執行您想要的所有專案，但您需要更多的功能，您可以將功能子類別化來變更或加入原始控制項。
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024192"
---
# <a name="subclassing-controls"></a><span data-ttu-id="13c8b-103">子類別化控制項</span><span class="sxs-lookup"><span data-stu-id="13c8b-103">Subclassing Controls</span></span>

<span data-ttu-id="13c8b-104">如果控制項幾乎會執行您想要的所有專案，但您需要更多的功能，您可以將功能子類別化來變更或加入原始控制項。</span><span class="sxs-lookup"><span data-stu-id="13c8b-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="13c8b-105">子類別可以擁有現有類別的所有功能，以及您想要提供給它的任何其他功能。</span><span class="sxs-lookup"><span data-stu-id="13c8b-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="13c8b-106">本檔討論如何建立子類別，並包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="13c8b-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="13c8b-107">ComCtl32.dll 第6版之前的子類別化控制項</span><span class="sxs-lookup"><span data-stu-id="13c8b-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="13c8b-108">儲存使用者資料</span><span class="sxs-lookup"><span data-stu-id="13c8b-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="13c8b-109">舊子類別化方法的缺點</span><span class="sxs-lookup"><span data-stu-id="13c8b-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="13c8b-110">使用 ComCtl32.dll 第6版將控制項子類別化</span><span class="sxs-lookup"><span data-stu-id="13c8b-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="13c8b-111">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="13c8b-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="13c8b-112">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="13c8b-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="13c8b-113">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="13c8b-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="13c8b-114">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="13c8b-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="13c8b-115">ComCtl32.dll 第6版之前的子類別化控制項</span><span class="sxs-lookup"><span data-stu-id="13c8b-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="13c8b-116">您可以將控制項放在子類別中，並將使用者資料儲存在控制項內。</span><span class="sxs-lookup"><span data-stu-id="13c8b-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="13c8b-117">當您使用版本6之前的 ComCtl32.dll 版本時，請執行此動作。</span><span class="sxs-lookup"><span data-stu-id="13c8b-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="13c8b-118">使用舊版 ComCtl32.dll 建立子類別有一些缺點。</span><span class="sxs-lookup"><span data-stu-id="13c8b-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="13c8b-119">若要建立新的控制項，最好是從其中一個 Windows 通用控制項開始，並加以擴充以符合特定需求。</span><span class="sxs-lookup"><span data-stu-id="13c8b-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="13c8b-120">若要擴充控制項，請建立控制項，並將其現有的視窗程式取代為新的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="13c8b-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="13c8b-121">新程式會攔截控制項的訊息，並對其採取動作，或將它們傳遞至原始程式進行預設處理。</span><span class="sxs-lookup"><span data-stu-id="13c8b-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="13c8b-122">使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 或 [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) 函式來取代控制項的 WNDPROC。</span><span class="sxs-lookup"><span data-stu-id="13c8b-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="13c8b-123">下列程式碼範例顯示如何取代 WNDPROC。</span><span class="sxs-lookup"><span data-stu-id="13c8b-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="13c8b-124">儲存使用者資料</span><span class="sxs-lookup"><span data-stu-id="13c8b-124">Storing User Data</span></span>

<span data-ttu-id="13c8b-125">您可能會想要將使用者資料儲存在個別的視窗中。</span><span class="sxs-lookup"><span data-stu-id="13c8b-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="13c8b-126">這項資料可供新的視窗程式用來判斷如何繪製控制項，或是要將特定訊息傳送至何處。</span><span class="sxs-lookup"><span data-stu-id="13c8b-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="13c8b-127">例如，您可以使用資料將 c + + 類別指標儲存至代表控制項的類別。</span><span class="sxs-lookup"><span data-stu-id="13c8b-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="13c8b-128">下列程式碼範例示範如何使用 [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) ，以視窗儲存資料。</span><span class="sxs-lookup"><span data-stu-id="13c8b-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="13c8b-129">舊子類別化方法的缺點</span><span class="sxs-lookup"><span data-stu-id="13c8b-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="13c8b-130">下列清單指出使用先前所述方法將控制項子類別化的一些缺點。</span><span class="sxs-lookup"><span data-stu-id="13c8b-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="13c8b-131">視窗程式只能取代一次。</span><span class="sxs-lookup"><span data-stu-id="13c8b-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="13c8b-132">建立子類別之後，很難將它移除。</span><span class="sxs-lookup"><span data-stu-id="13c8b-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="13c8b-133">建立私用資料與視窗的關聯效率不佳。</span><span class="sxs-lookup"><span data-stu-id="13c8b-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="13c8b-134">若要呼叫子類別鏈中的下一個程式，您無法轉換舊的視窗程式並呼叫它，您必須使用 [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="13c8b-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="13c8b-135">使用 ComCtl32.dll 第6版將控制項子類別化</span><span class="sxs-lookup"><span data-stu-id="13c8b-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="13c8b-136">ComCtl32.dll 第6版僅限 Unicode。</span><span class="sxs-lookup"><span data-stu-id="13c8b-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="13c8b-137">ComCtl32.dll 第6版所支援的通用控制項，不應使用 ANSI 視窗程式 (或 superclass) 進行子類別化。</span><span class="sxs-lookup"><span data-stu-id="13c8b-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="13c8b-138">ComCtl32.dll 第6版包含四個功能，可讓您更輕鬆地建立子類別，並消除先前所討論的缺點。</span><span class="sxs-lookup"><span data-stu-id="13c8b-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="13c8b-139">新的函式會封裝與多組參考資料相關的管理，因此開發人員可以專注于程式設計功能，而不是管理子類別。</span><span class="sxs-lookup"><span data-stu-id="13c8b-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="13c8b-140">子類別化函數包括：</span><span class="sxs-lookup"><span data-stu-id="13c8b-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="13c8b-141">**SetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="13c8b-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="13c8b-142">**GetWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="13c8b-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="13c8b-143">**RemoveWindowSubclass**</span><span class="sxs-lookup"><span data-stu-id="13c8b-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="13c8b-144">**DefSubclassProc**</span><span class="sxs-lookup"><span data-stu-id="13c8b-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="13c8b-145">SetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="13c8b-145">SetWindowSubclass</span></span>

<span data-ttu-id="13c8b-146">這個函式是用來一開始將視窗子類別化。</span><span class="sxs-lookup"><span data-stu-id="13c8b-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="13c8b-147">每個子類別都是由 *pfnSubclass* 和其 *uIdSubclass* 的位址唯一識別。</span><span class="sxs-lookup"><span data-stu-id="13c8b-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="13c8b-148">這兩個都是 [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) 函式的參數。</span><span class="sxs-lookup"><span data-stu-id="13c8b-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="13c8b-149">數個子類別可以共用相同的子類別程式，且識別碼可以識別每個呼叫。</span><span class="sxs-lookup"><span data-stu-id="13c8b-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="13c8b-150">若要變更參考資料，您可以對 **SetWindowSubclass** 進行後續的呼叫。</span><span class="sxs-lookup"><span data-stu-id="13c8b-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="13c8b-151">重要的優點是每個子類別實例都有自己的參考資料。</span><span class="sxs-lookup"><span data-stu-id="13c8b-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="13c8b-152">子類別程式的宣告與一般視窗程式稍有不同，因為它有兩個額外的資料片段：子類別識別碼和參考資料。</span><span class="sxs-lookup"><span data-stu-id="13c8b-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="13c8b-153">下列函式宣告的最後兩個參數顯示此。</span><span class="sxs-lookup"><span data-stu-id="13c8b-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="13c8b-154">每次新的視窗程式收到訊息時，就會包含子類別識別碼和參考資料。</span><span class="sxs-lookup"><span data-stu-id="13c8b-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="13c8b-155">傳遞至程式的所有字串都是 Unicode 字串，即使 Unicode 未指定為預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="13c8b-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="13c8b-156">下列範例顯示子類別化控制項之視窗程式的基本架構執行。</span><span class="sxs-lookup"><span data-stu-id="13c8b-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="13c8b-157">視窗程式可以附加至對話程式之 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 處理常式中的控制項，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="13c8b-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="13c8b-158">GetWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="13c8b-158">GetWindowSubclass</span></span>

<span data-ttu-id="13c8b-159">此函數會抓取子類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13c8b-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="13c8b-160">例如，您可以使用 [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) 來存取參考資料。</span><span class="sxs-lookup"><span data-stu-id="13c8b-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="13c8b-161">RemoveWindowSubclass</span><span class="sxs-lookup"><span data-stu-id="13c8b-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="13c8b-162">此函數會移除子類別。</span><span class="sxs-lookup"><span data-stu-id="13c8b-162">This function removes subclasses.</span></span> <span data-ttu-id="13c8b-163">結合 [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)的 [**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)可讓您以動態方式新增和移除子類別。</span><span class="sxs-lookup"><span data-stu-id="13c8b-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="13c8b-164">DefSubclassProc</span><span class="sxs-lookup"><span data-stu-id="13c8b-164">DefSubclassProc</span></span>

<span data-ttu-id="13c8b-165">[**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)函式會呼叫子類別鏈中的下一個處理常式。</span><span class="sxs-lookup"><span data-stu-id="13c8b-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="13c8b-166">函數也會抓取適當的識別碼和參考資料，並將資訊傳遞至下一個視窗程式。</span><span class="sxs-lookup"><span data-stu-id="13c8b-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 