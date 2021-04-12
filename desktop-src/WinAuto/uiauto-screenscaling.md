---
title: 瞭解螢幕縮放問題
description: Windows Vista 和更新版本的作業系統可讓使用者變更每英寸的點 (DPI) 設定，讓螢幕上大部分的 UI 元素顯示較大。
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- 用戶端，消費者介面自動化螢幕縮放比例
- 用戶端，螢幕縮放比例
- 用戶端，調整規模
- 消費者介面自動化，螢幕縮放比例
- 消費者介面自動化，調整規模
- 螢幕縮放比例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382481"
---
# <a name="understanding-screen-scaling-issues"></a><span data-ttu-id="9478a-109">瞭解螢幕縮放問題</span><span class="sxs-lookup"><span data-stu-id="9478a-109">Understanding Screen Scaling Issues</span></span>

<span data-ttu-id="9478a-110">Windows Vista 和更新版本的作業系統可讓使用者變更每英寸的點 (DPI) 設定，讓螢幕上大部分的 UI 元素顯示較大。</span><span class="sxs-lookup"><span data-stu-id="9478a-110">Windows Vista and later versions of the operating system enable users to change the dots per inch (dpi) setting so that most UI elements on the screen appear larger.</span></span> <span data-ttu-id="9478a-111">在舊版的 Windows 中，調整必須由應用程式來執行。</span><span class="sxs-lookup"><span data-stu-id="9478a-111">In earlier versions of Windows, the scaling had to be implemented by applications.</span></span> <span data-ttu-id="9478a-112">在 Windows Vista （含）以後版本中，桌面視窗管理員 (DWM) 會針對所有不會處理其本身調整的應用程式執行預設調整。</span><span class="sxs-lookup"><span data-stu-id="9478a-112">In Windows Vista and later, the Desktop Window Manager (DWM) performs default scaling for all applications that do not handle their own scaling.</span></span> <span data-ttu-id="9478a-113">Microsoft 消費者介面自動化用戶端應用程式必須將這項功能納入考慮。</span><span class="sxs-lookup"><span data-stu-id="9478a-113">Microsoft UI Automation client applications must take this feature into account.</span></span>

<span data-ttu-id="9478a-114">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="9478a-114">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9478a-115">在 Windows Vista 和更新版本中進行調整</span><span class="sxs-lookup"><span data-stu-id="9478a-115">Scaling in Windows Vista and Later</span></span>](#scaling-in-windows-vista-and-later)
-   [<span data-ttu-id="9478a-116">使用者介面自動化用戶端中的縮放比例</span><span class="sxs-lookup"><span data-stu-id="9478a-116">Scaling in UI Automation Clients</span></span>](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a><span data-ttu-id="9478a-117">在 Windows Vista 和更新版本中進行調整</span><span class="sxs-lookup"><span data-stu-id="9478a-117">Scaling in Windows Vista and Later</span></span>

<span data-ttu-id="9478a-118">預設的 DPI 設定為96，這表示96圖元佔用一個名義英寸的寬度或高度。</span><span class="sxs-lookup"><span data-stu-id="9478a-118">The default dpi setting is 96, which means that 96 pixels occupy a width or height of one notional inch.</span></span> <span data-ttu-id="9478a-119">「英吋」的確切測量值取決於監視器的大小和實體解析度。</span><span class="sxs-lookup"><span data-stu-id="9478a-119">The exact measure of an "inch" depends on the size and physical resolution of the monitor.</span></span> <span data-ttu-id="9478a-120">例如，在 12 英吋寬、1280 像素水平解析度的監視器上，96 像素的水平線長度約一英吋的 9/10。</span><span class="sxs-lookup"><span data-stu-id="9478a-120">For example, on a monitor 12 inches wide, at a horizontal resolution of 1280 pixels, a horizontal line of 96 pixels extends about 9/10 of an inch.</span></span>

<span data-ttu-id="9478a-121">變更 DPI 設定與變更螢幕解析度不同。</span><span class="sxs-lookup"><span data-stu-id="9478a-121">Changing the dpi setting is not the same as changing the screen resolution.</span></span> <span data-ttu-id="9478a-122">在 DPI 縮放比例中，螢幕上的實體圖元數目會維持不變。</span><span class="sxs-lookup"><span data-stu-id="9478a-122">With dpi scaling, the number of physical pixels on the screen remains the same.</span></span> <span data-ttu-id="9478a-123">不過，縮放比例會套用至 UI 元素的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="9478a-123">However, scaling is applied to the size and location of UI elements.</span></span> <span data-ttu-id="9478a-124">這項調整可由桌上型電腦的 DWM 以及未明確要求不要調整的應用程式自動執行。</span><span class="sxs-lookup"><span data-stu-id="9478a-124">This scaling can be performed automatically by the DWM for the desktop and for applications that do not explicitly ask not to be scaled.</span></span>

<span data-ttu-id="9478a-125">實際上，當使用者將縮放比例設定為 120 DPI 時，螢幕上的垂直或水準英寸會變大25%。</span><span class="sxs-lookup"><span data-stu-id="9478a-125">In effect, when the user sets the scale factor to 120 dpi, a vertical or horizontal inch on the screen becomes bigger by 25 percent.</span></span> <span data-ttu-id="9478a-126">所有維度都會因此調整。</span><span class="sxs-lookup"><span data-stu-id="9478a-126">All dimensions are scaled accordingly.</span></span> <span data-ttu-id="9478a-127">應用程式視窗在螢幕上邊緣和左邊緣的位移會增加25%。</span><span class="sxs-lookup"><span data-stu-id="9478a-127">The offset of an application window from the top edge and left edge of the screen increases by 25 percent.</span></span> <span data-ttu-id="9478a-128">如果應用程式調整已啟用，且應用程式不是 DPI 感知，則視窗的大小會以相同比例增加，以及其所包含之所有 UI 元素的位移和大小。</span><span class="sxs-lookup"><span data-stu-id="9478a-128">If application scaling is enabled and the application is not dpi-aware, the size of the window increases in the same proportion, along with the offsets and sizes of all UI elements it contains.</span></span>

> [!Note]  
> <span data-ttu-id="9478a-129">根據預設，當使用者將 DPI 設定為120時，DWM 不會執行非 DPI 感知應用程式的縮放比例，但當 DPI 設定為自訂值144或更高時，則會執行調整。</span><span class="sxs-lookup"><span data-stu-id="9478a-129">By default, the DWM does not perform scaling for non-dpi-aware applications when the user sets the dpi to 120, but does perform scaling when the dpi is set to a custom value of 144 or higher.</span></span> <span data-ttu-id="9478a-130">不過，使用者可以覆寫此預設行為。</span><span class="sxs-lookup"><span data-stu-id="9478a-130">However, the user can override the default behavior.</span></span>

 

<span data-ttu-id="9478a-131">針對重視畫面座標的應用程式，畫面縮放比例會產生新挑戰。</span><span class="sxs-lookup"><span data-stu-id="9478a-131">Screen scaling creates new challenges for applications that are concerned in any way with screen coordinates.</span></span> <span data-ttu-id="9478a-132">畫面現在包含兩個座標系統：實體和邏輯。</span><span class="sxs-lookup"><span data-stu-id="9478a-132">The screen now contains two coordinate systems: physical and logical.</span></span> <span data-ttu-id="9478a-133">點的實體座標是來自原點左上角的實際位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9478a-133">The physical coordinates of a point are the actual offset in pixels from the upper-left of the origin point.</span></span> <span data-ttu-id="9478a-134">邏輯座標則是像素本身縮放時，跟著縮放的位移。</span><span class="sxs-lookup"><span data-stu-id="9478a-134">The logical coordinates are the offsets as they would be if the pixels themselves were scaled.</span></span>

<span data-ttu-id="9478a-135">假設您設計的對話方塊在座標 (100, 48) 上有一個按鈕。</span><span class="sxs-lookup"><span data-stu-id="9478a-135">Suppose you design a dialog box with a button at coordinates (100, 48).</span></span> <span data-ttu-id="9478a-136">當此對話方塊顯示為預設 96 DPI 時，此按鈕會位於 (100，48) 的實體座標。</span><span class="sxs-lookup"><span data-stu-id="9478a-136">When this dialog box is displayed at the default 96 dpi, the button is located at physical coordinates of (100, 48).</span></span> <span data-ttu-id="9478a-137">以 120 DPI 為單位，位於 (125，60) 的實體座標。</span><span class="sxs-lookup"><span data-stu-id="9478a-137">At 120 dpi, it is located at physical coordinates of (125, 60).</span></span> <span data-ttu-id="9478a-138">但是在任何 DPI 設定中，邏輯座標都相同： (100、48) 。</span><span class="sxs-lookup"><span data-stu-id="9478a-138">But the logical coordinates are the same at any dpi setting: (100, 48).</span></span>

<span data-ttu-id="9478a-139">邏輯座標很重要，因為它們會使作業系統和應用程式的行為保持一致，無論 DPI 設定為何。</span><span class="sxs-lookup"><span data-stu-id="9478a-139">Logical coordinates are important, because they make the behavior of the operating system and applications consistent, regardless of the dpi setting.</span></span> <span data-ttu-id="9478a-140">例如， [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) 函數通常會傳回邏輯座標。</span><span class="sxs-lookup"><span data-stu-id="9478a-140">For example, typically, the [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) function returns the logical coordinates.</span></span> <span data-ttu-id="9478a-141">如果您將游標移到對話方塊中的專案上方，則會傳回相同的座標，不論 DPI 設定為何。</span><span class="sxs-lookup"><span data-stu-id="9478a-141">If you move the cursor over an element in a dialog box, the same coordinates are returned, regardless of the dpi setting.</span></span> <span data-ttu-id="9478a-142">如果您在 (100、100) 繪製控制項，則會將它繪製至這些邏輯座標，而且會佔用與任何 DPI 設定相同的相對位置。</span><span class="sxs-lookup"><span data-stu-id="9478a-142">If you draw a control at (100, 100), it is drawn to those logical coordinates, and will occupy the same relative position at any dpi setting.</span></span>

## <a name="scaling-in-ui-automation-clients"></a><span data-ttu-id="9478a-143">使用者介面自動化用戶端中的縮放比例</span><span class="sxs-lookup"><span data-stu-id="9478a-143">Scaling in UI Automation Clients</span></span>

<span data-ttu-id="9478a-144">消費者介面自動化 API 不會使用邏輯座標。</span><span class="sxs-lookup"><span data-stu-id="9478a-144">The UI Automation API does not use logical coordinates.</span></span> <span data-ttu-id="9478a-145">下列方法和屬性會傳回實體座標或將實體座標視為參數。</span><span class="sxs-lookup"><span data-stu-id="9478a-145">The following methods and properties return physical coordinates or take physical coordinates as parameters.</span></span>

-   [<span data-ttu-id="9478a-146">**IUIAutomation::ElementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="9478a-146">**IUIAutomation::ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [<span data-ttu-id="9478a-147">**IUIAutomation::ElementFromPointBuildCache**</span><span class="sxs-lookup"><span data-stu-id="9478a-147">**IUIAutomation::ElementFromPointBuildCache**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [<span data-ttu-id="9478a-148">**IUIAutomationElement::GetClickablePoint**</span><span class="sxs-lookup"><span data-stu-id="9478a-148">**IUIAutomationElement::GetClickablePoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [<span data-ttu-id="9478a-149">**IUIAutomationElement::CurrentBoundingRectangle**</span><span class="sxs-lookup"><span data-stu-id="9478a-149">**IUIAutomationElement::CurrentBoundingRectangle**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [<span data-ttu-id="9478a-150">**IUIAutomationElement::CachedBoundingRectangle**</span><span class="sxs-lookup"><span data-stu-id="9478a-150">**IUIAutomationElement::CachedBoundingRectangle**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [<span data-ttu-id="9478a-151">**IRawElementProviderFragment::BoundingRectangle**</span><span class="sxs-lookup"><span data-stu-id="9478a-151">**IRawElementProviderFragment::BoundingRectangle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

<span data-ttu-id="9478a-152">根據預設，在未設定為 96 DPI 的環境中執行的消費者介面自動化應用程式，將無法從這些方法和屬性取得正確的結果。</span><span class="sxs-lookup"><span data-stu-id="9478a-152">By default, UI Automation applications that are running in an environment that is not set to 96 dpi will not obtain correct results from these methods and properties.</span></span> <span data-ttu-id="9478a-153">例如，因為游標位置是以邏輯座標為單位，所以用戶端無法將這些座標傳遞給 [**IUIAutomation：： ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) ，以取得游標下的元素。</span><span class="sxs-lookup"><span data-stu-id="9478a-153">For example, because the cursor position is in logical coordinates, the client cannot pass these coordinates to [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) to obtain the element that is under the cursor.</span></span> <span data-ttu-id="9478a-154">此外，應用程式也將無法在其用戶端區域之外正確放置視窗。</span><span class="sxs-lookup"><span data-stu-id="9478a-154">In addition, the application will not be able to correctly place windows outside its client area.</span></span>

<span data-ttu-id="9478a-155">解決方案有兩個部分。</span><span class="sxs-lookup"><span data-stu-id="9478a-155">The solution has two parts.</span></span>

<span data-ttu-id="9478a-156">首先，將用戶端應用程式設為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="9478a-156">First, make the client application dpi-aware.</span></span> <span data-ttu-id="9478a-157">若要這樣做，請在啟動時呼叫 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數。</span><span class="sxs-lookup"><span data-stu-id="9478a-157">To do this, call the [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function at startup.</span></span> <span data-ttu-id="9478a-158">這個函式會讓整個進程具有 DPI 感知，這表示所有屬於進程的視窗都是無比例的。</span><span class="sxs-lookup"><span data-stu-id="9478a-158">This function makes the entire process dpi-aware, meaning that all windows that belong to the process are unscaled.</span></span>

<span data-ttu-id="9478a-159">其次，若要取得資料指標座標，請呼叫 [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) 函數。</span><span class="sxs-lookup"><span data-stu-id="9478a-159">Second, to get cursor coordinates, call the [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) function.</span></span>

 

 