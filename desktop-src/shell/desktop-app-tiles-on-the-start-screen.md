---
description: 以下提供針對 Windows 8 量身打造傳統型應用程式圖格時應考慮的選項資訊，包括如何設計新開始畫面的桌面應用程式磚，以及如何選擇要在開始畫面中顯示的進入點。
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: '[開始] 畫面上的桌面應用程式磚'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcc5475732926300e2125ae9e97ea2d188bc468
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321368"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a><span data-ttu-id="9cc26-103">[開始] 畫面上的桌面應用程式磚</span><span class="sxs-lookup"><span data-stu-id="9cc26-103">Desktop App Tiles on the Start Screen</span></span>

<span data-ttu-id="9cc26-104">以下提供針對 Windows 8 量身打造傳統型應用程式圖格時應考慮的選項資訊，包括如何設計新開始畫面的桌面應用程式磚，以及如何選擇要在開始畫面中顯示的進入點。</span><span class="sxs-lookup"><span data-stu-id="9cc26-104">The following provides information on choices to consider when tailoring desktop app tiles for Windows 8 including how to design desktop app tiles for the new Start screen and how to choose what entry points to show in the Start screen.</span></span>

## <a name="design-your-tile-for-the-start-screen"></a><span data-ttu-id="9cc26-105">設計開始畫面的磚</span><span class="sxs-lookup"><span data-stu-id="9cc26-105">Design your tile for the Start screen</span></span>

<span data-ttu-id="9cc26-106">您可以自訂桌面應用程式磚的兩個部分：應用程式名稱和圖示。</span><span class="sxs-lookup"><span data-stu-id="9cc26-106">You can customize two aspects of your desktop app tiles: the app name, and icon.</span></span> <span data-ttu-id="9cc26-107">背景色彩衍生自使用者所選擇的背景色彩，而不是以程式設計的方式進行自訂。</span><span class="sxs-lookup"><span data-stu-id="9cc26-107">The background color is derived from the user's chosen background color and isn't programmatically customizable.</span></span>

![應用程式磚設計指引。](images/tiles-desktop-1.png)

<span data-ttu-id="9cc26-109">DO：避免截斷您的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="9cc26-109">DO: Avoid truncation of your application name.</span></span> <span data-ttu-id="9cc26-110">釘選到開始畫面的桌面磚最多可容納兩行文字，也可以容納大約十個字元 (不過這取決於 UI 語言) ，因此請儘量讓應用程式名稱夠短，以避免截斷。</span><span class="sxs-lookup"><span data-stu-id="9cc26-110">Desktop tiles pinned to the Start screen can accommodate up to two lines of text each line, or about around ten characters (though this depends on the UI language), so try to keep the application name short enough to avoid truncation.</span></span>

<span data-ttu-id="9cc26-111">DO：提供四個支援開始畫面縮放值的圖示，以確保您的圖示在所有外型規格上看起來都很清晰。</span><span class="sxs-lookup"><span data-stu-id="9cc26-111">DO: Provide icons for the four supported Start screen scale values to ensure that your icons look crisp on all form factors.</span></span>



| <span data-ttu-id="9cc26-112">調整</span><span class="sxs-lookup"><span data-stu-id="9cc26-112">Scale</span></span> | <span data-ttu-id="9cc26-113">磚大小 (以圖元為單位) </span><span class="sxs-lookup"><span data-stu-id="9cc26-113">Tile size (in pixels)</span></span> | <span data-ttu-id="9cc26-114">使用的圖示大小 (以圖元為單位) </span><span class="sxs-lookup"><span data-stu-id="9cc26-114">Icon size used (in pixels)</span></span> |
|-------|-----------------------|----------------------------|
| <span data-ttu-id="9cc26-115">80%</span><span class="sxs-lookup"><span data-stu-id="9cc26-115">80%</span></span>   | <span data-ttu-id="9cc26-116">120 x 120</span><span class="sxs-lookup"><span data-stu-id="9cc26-116">120 x 120</span></span>             | <span data-ttu-id="9cc26-117">48 x 48</span><span class="sxs-lookup"><span data-stu-id="9cc26-117">48 x 48</span></span>                    |
| <span data-ttu-id="9cc26-118">100%</span><span class="sxs-lookup"><span data-stu-id="9cc26-118">100%</span></span>  | <span data-ttu-id="9cc26-119">150 x 150</span><span class="sxs-lookup"><span data-stu-id="9cc26-119">150 x 150</span></span>             | <span data-ttu-id="9cc26-120">64 x 64</span><span class="sxs-lookup"><span data-stu-id="9cc26-120">64 x 64</span></span>                    |
| <span data-ttu-id="9cc26-121">140%</span><span class="sxs-lookup"><span data-stu-id="9cc26-121">140%</span></span>  | <span data-ttu-id="9cc26-122">210 x 210</span><span class="sxs-lookup"><span data-stu-id="9cc26-122">210 x 210</span></span>             | <span data-ttu-id="9cc26-123">96 x 96</span><span class="sxs-lookup"><span data-stu-id="9cc26-123">96 x 96</span></span>                    |
| <span data-ttu-id="9cc26-124">180%</span><span class="sxs-lookup"><span data-stu-id="9cc26-124">180%</span></span>  | <span data-ttu-id="9cc26-125">270 x 270</span><span class="sxs-lookup"><span data-stu-id="9cc26-125">270 x 270</span></span>             | <span data-ttu-id="9cc26-126">128 x 128</span><span class="sxs-lookup"><span data-stu-id="9cc26-126">128 x 128</span></span>                  |



 

<span data-ttu-id="9cc26-127">DO：採用 Microsoft 設計原則。</span><span class="sxs-lookup"><span data-stu-id="9cc26-127">DO: Embrace the Microsoft design principles.</span></span> <span data-ttu-id="9cc26-128">圖示的新外觀和風格是平面的，因此，如果您想要為傳統型應用程式模仿 Windows Store 應用程式圖示，請考慮捨棄陰影等。</span><span class="sxs-lookup"><span data-stu-id="9cc26-128">The new look and feel for icons is flat, so if you want to mimic Windows Store app icons for your desktop app, consider taking out drop shadows and so on.</span></span>

<span data-ttu-id="9cc26-129">請勿：避免使用色彩。</span><span class="sxs-lookup"><span data-stu-id="9cc26-129">DON'T: Don't avoid the use of color.</span></span> <span data-ttu-id="9cc26-130">雖然 Windows Store 應用程式圖示有時是單色的，但我們建議使用桌面應用程式的色彩圖示。</span><span class="sxs-lookup"><span data-stu-id="9cc26-130">While Windows Store app icons are sometimes monochromatic, we recommend using color icons for desktop apps.</span></span> <span data-ttu-id="9cc26-131">這有助於區分工作列上的桌面應用程式，以及從開始畫面中的其他桌面應用程式磚，因為無法自訂桌面磚的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9cc26-131">This helps differentiate desktop applications on the taskbar, and from other desktop app tiles in the Start screen because the background color of desktop tiles can't be customized.</span></span> <span data-ttu-id="9cc26-132">請考慮使用更飽和的色彩。</span><span class="sxs-lookup"><span data-stu-id="9cc26-132">Do consider using more saturated colors.</span></span>

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a><span data-ttu-id="9cc26-133">決定要包含在開始畫面中的正確進入點</span><span class="sxs-lookup"><span data-stu-id="9cc26-133">Decide the right entry points to include in the Start screen</span></span>

<span data-ttu-id="9cc26-134">請在安裝應用程式時，在開始畫面中為每個應用程式新增一個快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-134">DO: Add one shortcut per app in the Start screen when the app is installed.</span></span> <span data-ttu-id="9cc26-135">這可確保人員可以直接從開始畫面或透過搜尋來啟動您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-135">This ensures that people can launch your app directly from the Start screen or through search.</span></span> <span data-ttu-id="9cc26-136">如果您未在開始畫面中加入快捷方式，您的應用程式就會變得很難啟動。</span><span class="sxs-lookup"><span data-stu-id="9cc26-136">If you do not include a shortcut in the Start screen, your app becomes difficult to launch.</span></span> <span data-ttu-id="9cc26-137">尤其是，請勿在桌面上新增快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-137">In particular, do not add a shortcut only on the desktop.</span></span> <span data-ttu-id="9cc26-138">使用者第一次登入時會看到開始畫面，因此只在桌面上放置快捷方式，並不如將它包含在開始畫面中一樣有效率。</span><span class="sxs-lookup"><span data-stu-id="9cc26-138">Users see the Start screen when they first login, and so placing a shortcut only on the desktop isn't as effective as including it in the Start screen.</span></span>

![顯示具有應用程式磚、維度和 ' Segoe U I Semilight 做 ' 之方格的圖表，以指出所使用的字型。](images/tiles-desktop-2.png)

<span data-ttu-id="9cc26-140">請勿：不提供相同應用程式的多個快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-140">DON'T: Don't provide multiple shortcuts to the same app.</span></span> <span data-ttu-id="9cc26-141">例如，在兩個不同的模式下都沒有啟動應用程式的兩個快捷方式，例如一個用於 Windows Internet Explorer，另一個用於沒有附加元件的 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="9cc26-141">For example, don't have two shortcuts that launch an app in two different modes, such as one for Windows Internet Explorer and one for Internet Explorer with no add-ons.</span></span>

<span data-ttu-id="9cc26-142">DO：將在安裝過程中新增的磚數目降至最低。</span><span class="sxs-lookup"><span data-stu-id="9cc26-142">DO: Minimize the number of tiles that are added as part of installation.</span></span> <span data-ttu-id="9cc26-143">請考慮將其他進入點公開給多餘的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-143">Consider exposing other entry points to the extraneous apps.</span></span> <span data-ttu-id="9cc26-144">例如，您不需要在主控台應用程式中包含個別的設定應用程式，而是透過主控台應用程式中的功能來存取設定。</span><span class="sxs-lookup"><span data-stu-id="9cc26-144">For example, instead of including a separate Settings app with a console app, access the settings through a feature in the console app.</span></span>

<span data-ttu-id="9cc26-145">不要：不要在開始畫面上放置下列專案的快捷方式：</span><span class="sxs-lookup"><span data-stu-id="9cc26-145">DON'T: Don't put shortcuts to the following items on the Start screen:</span></span>

-   <span data-ttu-id="9cc26-146">Uninstallers.</span><span class="sxs-lookup"><span data-stu-id="9cc26-146">Uninstallers.</span></span> <span data-ttu-id="9cc26-147">使用者可以透過主控台中的 [程式] 專案來存取 uninstallers。</span><span class="sxs-lookup"><span data-stu-id="9cc26-147">Users can access uninstallers through the Programs item in the Control Panel.</span></span>
-   <span data-ttu-id="9cc26-148">說明檔。</span><span class="sxs-lookup"><span data-stu-id="9cc26-148">Help files.</span></span> <span data-ttu-id="9cc26-149">直接在您的應用程式中包含說明主題。</span><span class="sxs-lookup"><span data-stu-id="9cc26-149">Include help topics directly in your app.</span></span>
-   <span data-ttu-id="9cc26-150">應用程式設定和選項。</span><span class="sxs-lookup"><span data-stu-id="9cc26-150">App settings and options.</span></span> <span data-ttu-id="9cc26-151">包含 UI 以設定應用程式內應用程式的設定，或建立主控台專案。</span><span class="sxs-lookup"><span data-stu-id="9cc26-151">Include UI to configure settings for an app within the app or create a Control Panel item.</span></span>
-   <span data-ttu-id="9cc26-152">網站。</span><span class="sxs-lookup"><span data-stu-id="9cc26-152">Web sites.</span></span> <span data-ttu-id="9cc26-153">直接在您的應用程式中提供任何適當的資訊連結，例如說明和技術支援網站。</span><span class="sxs-lookup"><span data-stu-id="9cc26-153">Provide any appropriate links to information like help and technical support sites directly in your app.</span></span>
-   <span data-ttu-id="9cc26-154">嚮導。</span><span class="sxs-lookup"><span data-stu-id="9cc26-154">Wizards.</span></span> <span data-ttu-id="9cc26-155">您應該從應用程式內啟動嚮導和其他一次性設定工作。</span><span class="sxs-lookup"><span data-stu-id="9cc26-155">Wizards and other one-time configuration tasks should be launched from within the app.</span></span>

<span data-ttu-id="9cc26-156">請勿：不要建立可從應用程式本身內啟動的功能或功能的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-156">DON'T: Don't create shortcuts to features or functionality that can be launched from within the app itself.</span></span> <span data-ttu-id="9cc26-157">例如，您可以從任何 Microsoft Office 應用程式設定語言設定，因此在開始畫面上也不需要有個別的語言設定進入點。</span><span class="sxs-lookup"><span data-stu-id="9cc26-157">For example, Language Settings can be configured from any Microsoft Office app, so it's unnecessary also to have a separate Language Settings entry point on the Start screen.</span></span>

<span data-ttu-id="9cc26-158">不要：不要對不是可執行檔的專案建立快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-158">DON'T: Don't create shortcuts to items that are not executable files.</span></span> <span data-ttu-id="9cc26-159">未對應到可執行檔的快捷方式（例如啟動網站或說明檔的快捷方式）會從開始畫面中篩選出來。</span><span class="sxs-lookup"><span data-stu-id="9cc26-159">Shortcuts that don't map to executables, such as shortcuts that launch web sites or help files, are filtered out of the Start screen.</span></span>

<span data-ttu-id="9cc26-160">DO：如果您安裝應用程式套件，而不是單一應用程式，請為套件中的每個應用程式新增一個快捷方式。</span><span class="sxs-lookup"><span data-stu-id="9cc26-160">DO: If you install a suite of apps rather than a single app, add one shortcut for each app in the suite.</span></span> <span data-ttu-id="9cc26-161">如前文所述，請避免建立協助工具的快捷方式，例如說明資訊、公用程式和設定。</span><span class="sxs-lookup"><span data-stu-id="9cc26-161">As mentioned above, avoid creating shortcuts to secondary functionality like help information, utilities, and settings.</span></span> <span data-ttu-id="9cc26-162">該功能應該包含在套件的相關應用程式 (s) 中。</span><span class="sxs-lookup"><span data-stu-id="9cc26-162">That functionality should be included in the relevant app(s) of the suite.</span></span>

<span data-ttu-id="9cc26-163">DO：為包含三個或更多磚的套件建立單一層級產品資料夾。</span><span class="sxs-lookup"><span data-stu-id="9cc26-163">DO: Create a single-level product folder for suites that contain three or more tiles.</span></span> <span data-ttu-id="9cc26-164">在開始畫面的 [應用程式] 視圖中，可從 [搜尋] 快速鍵存取應用程式，並依其最上層資料夾來分組。</span><span class="sxs-lookup"><span data-stu-id="9cc26-164">In the Apps view of the Start screen, accessible from the Search charm, applications are grouped by their top level folder.</span></span> <span data-ttu-id="9cc26-165">選擇描述性但精確的資料夾名稱;建議使用三個單字或更少。</span><span class="sxs-lookup"><span data-stu-id="9cc26-165">Choose a descriptive yet concise folder name; three words or fewer are recommended.</span></span> <span data-ttu-id="9cc26-166">請注意，當應用程式視圖群組磚並顯示資料夾名稱時，當磚釘選到開始畫面時，不會顯示此名稱，因此請讓您的磚名稱充分描述。</span><span class="sxs-lookup"><span data-stu-id="9cc26-166">Be aware that while the Apps view groups tiles and shows the folder name, this name isn't visible when a tile is pinned to the Start screen, so make your tile names sufficiently descriptive.</span></span>

<span data-ttu-id="9cc26-167">請勿：如果您的套件只包含單一快捷方式，請勿建立產品資料夾。</span><span class="sxs-lookup"><span data-stu-id="9cc26-167">DON'T: Don't create a product folder if your suite contains only a single shortcut.</span></span> <span data-ttu-id="9cc26-168">將快捷方式放在最上層的 [開始] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9cc26-168">Place your shortcut in the top-level Start folder.</span></span>

<span data-ttu-id="9cc26-169">DO：當安裝三個以上的應用程式套件時，請考慮是否有任何應用程式適用于次要、更不規則的用途，且不應釘選至開始畫面。</span><span class="sxs-lookup"><span data-stu-id="9cc26-169">DO: When installing a suite of more than three apps, consider whether any of those apps are for secondary, more irregular use and should not be pinned to the Start screen.</span></span> <span data-ttu-id="9cc26-170">如果是，可能的話，您可以根據上面的指導方針將這些磚完全移除，並從主要應用程式中啟動。</span><span class="sxs-lookup"><span data-stu-id="9cc26-170">If so, perhaps those tiles can be removed entirely, according to the guidance above, and launched from within a primary app.</span></span> <span data-ttu-id="9cc26-171">如果您無法移除磚，請考慮從開始畫面取消釘選。</span><span class="sxs-lookup"><span data-stu-id="9cc26-171">If you can't remove the tiles, consider unpinning them from the Start screen.</span></span> <span data-ttu-id="9cc26-172">如此一來，快捷方式仍會出現在 [ **所有應用程式** ] 中，但不會雜亂使用者的開始畫面。</span><span class="sxs-lookup"><span data-stu-id="9cc26-172">That way, the shortcuts still appear in the **All Apps** view but don't clutter the user's Start screen.</span></span>

<span data-ttu-id="9cc26-173">若要建立應用程式快捷方式，而不將它釘選到開始畫面，請在快捷方式上設定下列屬性： AppUserModel. StartPinOption = 1。</span><span class="sxs-lookup"><span data-stu-id="9cc26-173">To create add an app shortcut without pinning it to the Start screen, set the following property on the shortcut: System.AppUserModel.StartPinOption = 1.</span></span> <span data-ttu-id="9cc26-174">1的符號名稱是 APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL。</span><span class="sxs-lookup"><span data-stu-id="9cc26-174">The symbolic name for 1 is APPUSERMODEL\_STARTPINOPTION\_NOPINONINSTALL.</span></span>

<span data-ttu-id="9cc26-175">這可防止在開始畫面上顯示快捷方式，但仍然可以在 [ **所有應用程式** ] 視圖和搜尋結果中看到。</span><span class="sxs-lookup"><span data-stu-id="9cc26-175">This prevents the shortcut from being shown on the Start screen, but it can still be seen in the **All Apps** view and search results.</span></span> <span data-ttu-id="9cc26-176">只有使用者可以取消釘選現有的快捷方式，因此您必須在安裝期間或在將應用程式放在磁片上時，立即設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc26-176">Only the user can unpin existing shortcuts, so you must set this property during installation or immediately after placing the app on disk.</span></span>

<span data-ttu-id="9cc26-177">請勿：為應用程式（例如 Silverlight 或 JAVA）建立主機或執行時間的磚。</span><span class="sxs-lookup"><span data-stu-id="9cc26-177">DON'T: Don't create a tile for a host or runtime for applications, like Silverlight or Java.</span></span> <span data-ttu-id="9cc26-178">提供在 [新增/移除程式] 中卸載架構的進入點，並在主控台中提供任何設定進入點。</span><span class="sxs-lookup"><span data-stu-id="9cc26-178">Provide an entry point to uninstall the framework in Add/Remove Programs and provide any settings entry point in Control Panel.</span></span>

 

 



