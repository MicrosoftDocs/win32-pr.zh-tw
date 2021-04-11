---
title: 動態注釋的替代方案
description: 動態注釋的替代方案
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092853"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="5b183-103">動態注釋的替代方案</span><span class="sxs-lookup"><span data-stu-id="5b183-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="5b183-104">還有其他方法可以提供 UI 元素的自訂 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援，而且在某些情況下，它們是正確的解決方案。</span><span class="sxs-lookup"><span data-stu-id="5b183-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="5b183-105">在動態注釋之前，這些替代技術是開發人員唯一可用的選項。</span><span class="sxs-lookup"><span data-stu-id="5b183-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="5b183-106">它們包括執行所有 **IAccessible** 介面和程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="5b183-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="5b183-107">執行所有 IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="5b183-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="5b183-108">另一個方法是執行所有 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="5b183-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="5b183-109">自訂控制項或完全不同的 UI 元素通常需要這種方法;不過，開發和測試成本相當重要，除非真的需要，否則應該避免此情況。</span><span class="sxs-lookup"><span data-stu-id="5b183-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="5b183-110">如果目標是要修改單一屬性，則成本很難證明。</span><span class="sxs-lookup"><span data-stu-id="5b183-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="5b183-111">程式設計技術</span><span class="sxs-lookup"><span data-stu-id="5b183-111">Programmatic Techniques</span></span>

<span data-ttu-id="5b183-112">另一個選項是使用子類別化和包裝技術來修改針對特定屬性公開的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b183-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="5b183-113">這是動態注釋要取代的技巧。</span><span class="sxs-lookup"><span data-stu-id="5b183-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="5b183-114">若要使用子類別化和包裝來覆寫單一屬性，開發人員必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5b183-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="5b183-115">子類別化 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件的 HWND。</span><span class="sxs-lookup"><span data-stu-id="5b183-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="5b183-116">攔截 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息以取得正確的 IParam/OBJID 值。</span><span class="sxs-lookup"><span data-stu-id="5b183-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="5b183-117">使用 [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85))函式，將 [**WM \_ GETOBJECT**](wm-getobject.md)訊息轉送至基類。</span><span class="sxs-lookup"><span data-stu-id="5b183-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="5b183-118">如果傳回零，則呼叫 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject);否則，請在傳回的值上呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ，以取得控制項的原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5b183-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="5b183-119">建立包裝函式類別，以執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 並包裝上一個步驟所傳回的 **IAccessible** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5b183-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="5b183-120">除了要覆寫的方法和屬性以外，此包裝函式類別會將所有方法和屬性傳送至原始 **IAccessible** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5b183-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="5b183-121">這牽涉到撰寫所有 **IAccessible** 介面的21個屬性和方法的轉送程式碼，而不論實際覆寫了多少。</span><span class="sxs-lookup"><span data-stu-id="5b183-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="5b183-122">此外，開發人員必須確認下列條件：</span><span class="sxs-lookup"><span data-stu-id="5b183-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="5b183-123">覆寫的方法或屬性只能處理所需的子識別碼，並將所有其他識別碼轉寄至原始 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5b183-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="5b183-124">只有當原始物件支援 [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) 和 [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) 介面時，換行也必須轉送這些介面。</span><span class="sxs-lookup"><span data-stu-id="5b183-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="5b183-125">參考計數必須正確處理，特別是在支援其他介面時。</span><span class="sxs-lookup"><span data-stu-id="5b183-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="5b183-126">[**IDispatch**](idispatch-interface.md) 傳回值必須正確處理，尤其是使用 [**ITypeInfo：： Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) 方法時，必須使用包裝函式介面的介面指標來呼叫，而不是原始 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5b183-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="5b183-127">這些技術需要相當大量的工作，即使只有一或兩個屬性需要覆寫。</span><span class="sxs-lookup"><span data-stu-id="5b183-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="5b183-128">大部分產生的程式碼都涉及子類別化和包裝，而只有小小部分實際上提供覆寫的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b183-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="5b183-129">不過，在某些情況下需要這些技術。</span><span class="sxs-lookup"><span data-stu-id="5b183-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="5b183-130">例如，如果您要進行結構變更以建立預留位置 UI 元素，則應該使用這些技術，而不是動態注釋。</span><span class="sxs-lookup"><span data-stu-id="5b183-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="5b183-131">修正衍生自標籤的名稱</span><span class="sxs-lookup"><span data-stu-id="5b183-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="5b183-132">某些 Microsoft Win32 通用控制項（例如編輯方塊控制項）幾乎一律會搭配 (資源檔) 中的 LTEXT 專案，或資源檔) 中群組方塊 (的群組方塊使用。</span><span class="sxs-lookup"><span data-stu-id="5b183-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="5b183-133">Microsoft Active Accessibility 會自動從其標籤衍生控制項的 [名稱] 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b183-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="5b183-134">針對這類控制項，會忽略 Microsoft Visual Studio 中顯示的 [名稱] 或 [識別碼] 屬性) 的視窗文字 (，因為它通常是自動產生的，而且很少描述。例如，「IDC \_ EDIT1」。</span><span class="sxs-lookup"><span data-stu-id="5b183-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="5b183-135">如果未正確設計應用程式的使用者介面，Microsoft Active Accessibility 可能無法正確設定名稱。</span><span class="sxs-lookup"><span data-stu-id="5b183-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="5b183-136">若要與控制項相關聯，標籤或群組方塊必須緊接在定位順序中的動態控制項之前。</span><span class="sxs-lookup"><span data-stu-id="5b183-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="5b183-137">當資源編輯器開啟) 或直接編輯資源檔時，可以使用 [ **格式** ] 功能表上 Visual Studio (中的工具來變更定位順序。</span><span class="sxs-lookup"><span data-stu-id="5b183-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="5b183-138">下列範例顯示包含兩個標記編輯方塊之對話方塊的資源檔描述。</span><span class="sxs-lookup"><span data-stu-id="5b183-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



<span data-ttu-id="5b183-139">在此範例中，標籤和控制項不會以正確的定位順序列出。</span><span class="sxs-lookup"><span data-stu-id="5b183-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="5b183-140">如此一來，Microsoft Active Accessibility 會將名稱「姓氏」指派給第一個名稱編輯方塊，而不是「姓氏」編輯方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b183-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="5b183-141">下列範例會顯示正確的資源清單。</span><span class="sxs-lookup"><span data-stu-id="5b183-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="5b183-142">另外也請注意，快速鍵已在標籤中指定。</span><span class="sxs-lookup"><span data-stu-id="5b183-142">Note also that shortcut keys have been designated in the labels.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



<span data-ttu-id="5b183-143">當控制項有輔助標籤（例如，針對標題的最小值和最大值）時，這些標籤應放置在定位順序中的控制項之後。</span><span class="sxs-lookup"><span data-stu-id="5b183-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="5b183-144">控制項的主要標籤必須緊接在控制項本身之前出現。</span><span class="sxs-lookup"><span data-stu-id="5b183-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="5b183-145">在沒有標籤的情況下命名控制項</span><span class="sxs-lookup"><span data-stu-id="5b183-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="5b183-146">每個控制項都不一定要有可見的標籤。</span><span class="sxs-lookup"><span data-stu-id="5b183-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="5b183-147">不過，您仍然可以藉由新增不可見的標籤，來提供控制項的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b183-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="5b183-148">如同往常，隱藏的標籤必須緊接在定位順序中的控制項之前。</span><span class="sxs-lookup"><span data-stu-id="5b183-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="5b183-149">如果您在 Microsoft Visual Studio .NET 中使用資源編輯器，則可以將 Visible 屬性設為 False。</span><span class="sxs-lookup"><span data-stu-id="5b183-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="5b183-150">若要在編輯資源檔時使標籤隱藏 ( .rc) ，請將 [不是 WS] \_ 或 [標籤] 控制項的樣式部分新增，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="5b183-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="5b183-151">請注意，即使標籤不可見，任何指定的快速鍵仍可運作。</span><span class="sxs-lookup"><span data-stu-id="5b183-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 