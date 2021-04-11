---
title: 確定 UI 元素的命名正確
description: 本主題說明在 Microsoft Win32 應用程式中指定 UI 元素名稱的正確方式，讓 Microsoft Active Accessibility 可以透過 IAccessible \ 32，準確地將名稱公開給用戶端應用程式。Name 屬性。
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933299"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="9b6ad-103">確定 UI 元素的命名正確</span><span class="sxs-lookup"><span data-stu-id="9b6ad-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="9b6ad-104">本主題說明在 Microsoft Win32 應用程式中指定 UI 元素名稱的正確方式，讓 Microsoft Active Accessibility 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name 屬性](name-property.md)，準確地將名稱公開給用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="9b6ad-105">本節中的資訊僅適用于 Microsoft Active Accessibility。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="9b6ad-106">它並不適用于使用 Microsoft 消費者介面自動化的應用程式，或是以標記語言（例如 HTML、動態 HTML (DHTML) 或 XML）為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="9b6ad-107">概觀</span><span class="sxs-lookup"><span data-stu-id="9b6ad-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="9b6ad-108">錯誤命名如何造成問題</span><span class="sxs-lookup"><span data-stu-id="9b6ad-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="9b6ad-109">MSAA 如何取得 Name 屬性</span><span class="sxs-lookup"><span data-stu-id="9b6ad-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="9b6ad-110">如何尋找和修正命名問題</span><span class="sxs-lookup"><span data-stu-id="9b6ad-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="9b6ad-111">如何正確命名的簡介</span><span class="sxs-lookup"><span data-stu-id="9b6ad-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="9b6ad-112">如何使用隱藏的標籤來命名控制項</span><span class="sxs-lookup"><span data-stu-id="9b6ad-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="9b6ad-113">如何使用直接注釋來指定名稱屬性</span><span class="sxs-lookup"><span data-stu-id="9b6ad-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="9b6ad-114">批註名稱屬性的步驟</span><span class="sxs-lookup"><span data-stu-id="9b6ad-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="9b6ad-115">批註名稱屬性的範例</span><span class="sxs-lookup"><span data-stu-id="9b6ad-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="9b6ad-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b6ad-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="9b6ad-117">概觀</span><span class="sxs-lookup"><span data-stu-id="9b6ad-117">Overview</span></span>

<span data-ttu-id="9b6ad-118">在 Microsoft Active Accessibility 中，應用程式中的每個 UI 元素都會以公開 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的物件來表示。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="9b6ad-119">用戶端應用程式會使用 **IAccessible** 介面的屬性和方法來與 UI 元素互動，以及取得其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="9b6ad-120">**IAccessible** 介面所公開的其中一個最重要的屬性是 [Name 屬性](name-property.md)。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="9b6ad-121">用戶端應用程式依賴 Name 屬性來尋找、識別或向使用者宣告 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="9b6ad-122">如果 Microsoft Active Accessibility 無法正確地公開特定 UI 元素的 Name 屬性，用戶端應用程式將無法向使用者顯示該 UI 專案，而且殘障使用者將無法存取 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="9b6ad-123">錯誤命名如何造成問題</span><span class="sxs-lookup"><span data-stu-id="9b6ad-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="9b6ad-124">為了說明 UI 元素命名不正確所造成的問題，請考慮下圖所示的名稱輸入表單。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![輸入姓氏和姓氏的簡單表單圖例](images/incorrect-form.png)

<span data-ttu-id="9b6ad-126">雖然表單中的 UI 元素看起來沒問題，但程式設計的執行是不正確的。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="9b6ad-127">若為 Microsoft Active Accessibility 的用戶端，例如螢幕讀取器，則頂端編輯控制項的 [ [名稱] 屬性](name-property.md) 是 [姓氏：]，而底部編輯控制項的 [名稱] 屬性是空字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="9b6ad-128">螢幕閱讀程式會將最上層的編輯控制項讀取為「姓氏」，雖然使用者預期會輸入名字。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="9b6ad-129">螢幕閱讀程式會將第二個編輯控制項讀取為「沒有名稱」，因此使用者將不知道要在第二個編輯控制項中輸入的內容。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="9b6ad-130">螢幕讀取器無法協助使用者將資料輸入這個簡單的表單。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="9b6ad-131">表單的另一個問題是，沒有任何快捷方式按鍵指派給任何編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="9b6ad-132">使用者會強制使用 tab 鍵移至控制項或使用滑鼠。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="9b6ad-133">下列各節說明這些問題的來源，並提供修正這些問題的指導方針。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="9b6ad-134">MSAA 如何取得 Name 屬性</span><span class="sxs-lookup"><span data-stu-id="9b6ad-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="9b6ad-135">根據 UI 元素的類型而定，Microsoft Active Accessibility 會從不同的位置取得 [名稱屬性](name-property.md) 字串。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="9b6ad-136">對於具有相關聯視窗文字的大部分 UI 元素，Microsoft Active Accessibility 使用視窗文字做為名稱屬性字串。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="9b6ad-137">這種類型的 UI 元素範例包括按鈕、功能表項目和工具提示等控制項。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="9b6ad-138">針對下列控制項，Microsoft Active Accessibility 會忽略視窗文字，而改為在定位順序中的控制項上方尋找靜態文字標籤 (或群組框標籤) 。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="9b6ad-139">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="9b6ad-139">Combo Boxes</span></span>
-   <span data-ttu-id="9b6ad-140">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="9b6ad-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="9b6ad-141">編輯和 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="9b6ad-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="9b6ad-142">IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="9b6ad-142">IP Address controls</span></span>
-   <span data-ttu-id="9b6ad-143">清單方塊</span><span class="sxs-lookup"><span data-stu-id="9b6ad-143">List Boxes</span></span>
-   <span data-ttu-id="9b6ad-144">列出視圖</span><span class="sxs-lookup"><span data-stu-id="9b6ad-144">List Views</span></span>
-   <span data-ttu-id="9b6ad-145">進度列</span><span class="sxs-lookup"><span data-stu-id="9b6ad-145">Progress Bars</span></span>
-   <span data-ttu-id="9b6ad-146">杆</span><span class="sxs-lookup"><span data-stu-id="9b6ad-146">Scrollbars</span></span>
-   <span data-ttu-id="9b6ad-147">具有 SS \_ 圖示或 ss 點陣圖樣式的靜態 \_ 控制項</span><span class="sxs-lookup"><span data-stu-id="9b6ad-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="9b6ad-148">Trackbars</span><span class="sxs-lookup"><span data-stu-id="9b6ad-148">Trackbars</span></span>
-   <span data-ttu-id="9b6ad-149">樹狀檢視</span><span class="sxs-lookup"><span data-stu-id="9b6ad-149">Tree Views</span></span>

<span data-ttu-id="9b6ad-150">如果上述控制項未伴隨著靜態文字標籤，或標籤未正確地執行，Microsoft Active Accessibility 無法提供正確的 [名稱屬性](name-property.md) 給用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="9b6ad-151">上述的大部分控制項實際上都有相關聯的視窗文字。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="9b6ad-152">資源編輯器會自動產生視窗文字，其中包含泛型字串，例如 "edit1" 或 "listbox3"。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="9b6ad-153">雖然開發人員可以使用更有意義的文字來取代產生的視窗文字，但大部分的情況都是如此。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="9b6ad-154">因為產生的視窗文字對使用者沒有任何意義，Microsoft Active Accessibility 會忽略它，並改為使用隨附的靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="9b6ad-155">如何尋找和修正命名問題</span><span class="sxs-lookup"><span data-stu-id="9b6ad-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="9b6ad-156">在名稱輸入表單中所顯示的命名錯誤如何造成問題，問題的原因是控制項的定位順序不正確。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="9b6ad-157">使用 [檢查](inspect-objects.md) 之類的測試控管來檢查 UI 會顯示物件階層的問題。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="9b6ad-158">下列螢幕擷取畫面顯示 [檢查] 中所顯示之名稱輸入表單的中斷物件階層。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![[檢查] 工具的螢幕擷取畫面，其中顯示名稱輸入表單的不正確物件階層](images/incorrect-object-hierarchy.png)

<span data-ttu-id="9b6ad-160">在上一個螢幕擷取畫面中，請注意，物件階層不符合控制項在名稱輸入表單的使用者介面中顯示的結構。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="9b6ad-161">另請注意， [檢查](inspect-objects.md) 已將不正確的名稱指派給下一個專案 (它是輸入名字的編輯控制項，而且應該是名為 "first name：" 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="9b6ad-162">最後，請注意，檢查找不到最後一個專案的名稱 (它是輸入姓氏的編輯控制項，名稱應為 "Last Name："。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="9b6ad-163">下列範例會顯示名稱輸入表單的資源檔內容。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="9b6ad-164">請注意，索引標籤順序與控制項出現在使用者介面中的邏輯結構不一致。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="9b6ad-165">也請注意，這兩個編輯控制項未指定快速鍵。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="9b6ad-166">若要更正名稱輸入表單的問題，應編輯資源 ( .rc) 檔案以指定鍵盤快速鍵，並以下列順序放置控制項：</span><span class="sxs-lookup"><span data-stu-id="9b6ad-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="9b6ad-167">"&First Name：" 靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="9b6ad-168">用來輸入名字 (IDC EDIT1) 的編輯控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="9b6ad-169">"&Last Name：" 靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="9b6ad-170"> (IDC EDIT2) 輸入姓氏的編輯控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="9b6ad-171">[確定] 預設推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-171">The "OK" default push button.</span></span>

<span data-ttu-id="9b6ad-172">下列範例會顯示名稱輸入表單的已更正資源檔：</span><span class="sxs-lookup"><span data-stu-id="9b6ad-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="9b6ad-173">若要更正資源檔，您可以直接編輯檔案，也可以使用 Microsoft Visual Studio 中的定位順序工具。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="9b6ad-174">您可以按下 CTRL + D，或從 [**格式**] 功能表中選取 [定位 **順序]** ，以存取 Visual Studio 中的定位順序工具。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="9b6ad-175">修正和重建應用程式之後，名稱輸入表單的 UI 看起來會與之前相同。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="9b6ad-176">不過，Microsoft Active Accessibility 現在會提供正確的名稱屬性給用戶端應用程式，並在使用者按下 ALT + F 或 ALT + L 鍵盤快速鍵時，正確地設定焦點。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="9b6ad-177">此外， [檢查](inspect-objects.md) 將會顯示正確的物件階層，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![可存取的瀏覽器工具的螢幕擷取畫面，其中顯示名稱輸入表單的正確物件階層](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="9b6ad-179">如何正確命名的簡介</span><span class="sxs-lookup"><span data-stu-id="9b6ad-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="9b6ad-180">當 (或滑杆) 定義標題時，請確定字幕的主要靜態文字標籤會出現在標題之前，而且最小和最大範圍的靜態文字標籤會出現在標題之後。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="9b6ad-181">請記住，Microsoft Active Accessibility 會使用緊接在控制項前面的靜態文字標籤，作為控制項的 [ [名稱] 屬性](name-property.md) 。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="9b6ad-182">將主要靜態文字標籤放在貼文之前，並在其後面加上其他標籤，可確保 Microsoft Active Accessibility 提供正確的名稱屬性給用戶端。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="9b6ad-183">下圖顯示具有主要靜態文字標籤的一般字幕（稱為「速度」），以及最小 ( 「最小」 ) 的靜態文字標籤，以及最大 ( 「最大值」 ) 範圍。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![具有最小和最大範圍之主要標籤和標籤的 [標題] 控制項圖例](images/speed-trackbar.png)

<span data-ttu-id="9b6ad-185">下列範例顯示在資源檔中定義標題和其靜態文字標籤的正確方式：</span><span class="sxs-lookup"><span data-stu-id="9b6ad-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="9b6ad-186">如何使用隱藏的標籤來命名控制項</span><span class="sxs-lookup"><span data-stu-id="9b6ad-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="9b6ad-187">每個控制項都不一定要有可見的標籤。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="9b6ad-188">例如，有時新增標籤可能會在 UI 的外觀中造成不必要的變更。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="9b6ad-189">在此情況下，您可以使用不可見的標籤。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="9b6ad-190">Microsoft Active Accessibility 仍會挑選與隱藏標籤相關聯的文字，但標籤不會出現在視覺效果 UI 中，也不會干擾。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="9b6ad-191">如同可見標籤，隱藏的標籤必須緊接在定位順序中的控制項前面。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="9b6ad-192">若要在資源檔中將標籤隱藏 ( .rc) ，請將 `NOT WS_VISIBLE` 或加入 `|~WS_VISIBLE` 靜態文字控制項的樣式部分。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="9b6ad-193">如果您在 Visual Studio 中使用資源編輯器，則可以將 Visible 屬性設為 False。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="9b6ad-194">如何使用直接注釋來指定名稱屬性</span><span class="sxs-lookup"><span data-stu-id="9b6ad-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="9b6ad-195">Microsoft Active Accessibility 執行時間元件中包含的預設 proxy Oleacc.dll，會自動為所有標準 Windows 控制項提供 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="9b6ad-196">如果您自訂標準的 Windows 控制項，預設 proxy 會為您的自訂控制項正確提供所有 **IAccessible** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="9b6ad-197">您應徹底測試自訂控制項，以確保預設 proxy 會提供精確且完整的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="9b6ad-198">如果測試顯示不正確或不完整的屬性值，您可以使用稱為直接注釋的動態注釋技術來提供正確的屬性值，並新增遺漏的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="9b6ad-199">請注意，動態注釋不只是 Microsoft Active Accessibility proxy 所支援的控制項。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="9b6ad-200">您也可以使用它來修改或提供任何提供自身 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行的控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="9b6ad-201">本節著重于使用直接注釋，為控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 [Name 屬性](name-property.md)提供正確的值。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="9b6ad-202">您也可以使用直接注釋來提供其他屬性值。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="9b6ad-203">此外，直接注釋旁的其他動態注釋技巧也可供使用，而動態批註 API 的特性和功能則延伸到本章節所述的範圍之外。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="9b6ad-204">如需動態注釋的詳細資訊，請參閱 [動態批註 API](dynamic-annotation-api.md)。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="9b6ad-205">批註名稱屬性的步驟</span><span class="sxs-lookup"><span data-stu-id="9b6ad-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="9b6ad-206">使用直接注釋來變更控制項的 [ [名稱] 屬性](name-property.md) 牽涉到下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="9b6ad-207">包含下列標頭檔：</span><span class="sxs-lookup"><span data-stu-id="9b6ad-207">Include the following header files:</span></span>
    -   <span data-ttu-id="9b6ad-208">Initguid。h</span><span class="sxs-lookup"><span data-stu-id="9b6ad-208">Initguid.h</span></span>
    -   <span data-ttu-id="9b6ad-209">Oleacc。h</span><span class="sxs-lookup"><span data-stu-id="9b6ad-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="9b6ad-210">若要定義 Guid，您必須在相同的檔案中包含 Initguid 之前的 Oleacc。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="9b6ad-211">藉由呼叫 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函式（通常是在應用程式初始化過程中），初始化元件物件模型 (COM) 程式庫。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="9b6ad-212">建立目標控制項之後 (通常會在 [WM \_ INITDIALOG](../dlgbox/wm-initdialog.md) 訊息) 期間，建立注釋管理員的實例，並取得其 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="9b6ad-213">使用 [**IAccPropServices：： SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)方法，標注目標控制項的 [[名稱] 屬性](name-property.md)。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="9b6ad-214">釋放 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 指標。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="9b6ad-215">在終結目標控制項之前 (通常會在處理) 的 WM 終結訊息時，建立注釋管理員的實例，並取得其 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)介面的指標。 [ \_](../winmsg/wm-destroy.md)</span><span class="sxs-lookup"><span data-stu-id="9b6ad-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="9b6ad-216">您可以使用 [**IAccPropServices：： ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) 方法，從目標控制項清除 [名稱屬性](name-property.md) 批註。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="9b6ad-217">釋放 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) 指標。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="9b6ad-218">在您的應用程式結束之前 (通常會在處理 [WM 損 \_ 毀](../winmsg/wm-destroy.md) 訊息) 時，呼叫 [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式來釋放 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="9b6ad-219">[**IAccPropServices：： SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)函數接受五個參數。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="9b6ad-220">前三個（*hwnd*、 *idObject* 和 *idChild*）結合以識別控制項。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="9b6ad-221">第四個參數 *idProp* 指定要變更之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="9b6ad-222">若要變更 [Name 屬性](name-property.md)，請將 *IdProp* 設定為 **PROPID \_ ACC \_ Name**。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="9b6ad-223"> (如需您可以透過直接注釋設定之其他屬性的清單，請參閱 [使用直接注釋](using-direct-annotation.md)。 ) **SetHwndPropStr** 的最後一個參數（ *str*）是要做為 Name 屬性的新字串。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="9b6ad-224">批註名稱屬性的範例</span><span class="sxs-lookup"><span data-stu-id="9b6ad-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="9b6ad-225">下列範例程式碼示範如何使用直接注釋來變更控制項之 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 [Name 屬性](name-property.md)。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="9b6ad-226">為了簡單起見，此範例會使用硬式編碼的字串 ( 「新的控制項名稱」 ) 來設定 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="9b6ad-227">在應用程式的最終版本中，不應使用硬式編碼的字串，因為它們無法進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="9b6ad-228">相反地，一律從資源檔載入字串。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="9b6ad-229">此外，此範例不會顯示對 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="9b6ad-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9b6ad-230">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b6ad-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9b6ad-231">**概念**</span><span class="sxs-lookup"><span data-stu-id="9b6ad-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9b6ad-232">動態注釋 API</span><span class="sxs-lookup"><span data-stu-id="9b6ad-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="9b6ad-233">提供 Name 屬性</span><span class="sxs-lookup"><span data-stu-id="9b6ad-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="9b6ad-234">測試控管</span><span class="sxs-lookup"><span data-stu-id="9b6ad-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 