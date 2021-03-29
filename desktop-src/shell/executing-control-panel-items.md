---
description: 討論針對 Windows Vista 和更新版本的系統開啟主控台專案，以及涵蓋舊版主控台命令的方法。
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: 執行主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991690"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="21da0-103">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="21da0-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="21da0-104">如果您要尋找主控台專案的標準和模組名稱清單，請參閱 [主控台專案](controlpanel-canonical-names.md)的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="21da0-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="21da0-105">有兩種方式可以開啟主控台專案：</span><span class="sxs-lookup"><span data-stu-id="21da0-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="21da0-106">使用者可以開啟主控台然後按一下或按兩下專案的圖示來開啟專案。</span><span class="sxs-lookup"><span data-stu-id="21da0-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="21da0-107">使用者或應用程式可以直接從命令列提示字元中執行，以啟動主控台專案。</span><span class="sxs-lookup"><span data-stu-id="21da0-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="21da0-108">應用程式可以使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) 函數，以程式設計方式開啟主控台。</span><span class="sxs-lookup"><span data-stu-id="21da0-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="21da0-109">下列範例顯示應用程式如何使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)函式來啟動名為 **MyCpl.cpl** 的主控台專案。</span><span class="sxs-lookup"><span data-stu-id="21da0-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="21da0-110">透過命令列開啟主控台專案時，您可以指示它開啟至專案中的特定索引標籤。</span><span class="sxs-lookup"><span data-stu-id="21da0-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="21da0-111">由於某些 Windows Vista 主控台專案中的特定索引標籤的新增和移除，因此在 Windows XP 中，索引標籤的編號可能已變更。</span><span class="sxs-lookup"><span data-stu-id="21da0-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="21da0-112">例如，下列範例會在 Windows XP 上的系統專案和 Windows Vista 的第三個索引標籤上啟動第四個索引標籤。</span><span class="sxs-lookup"><span data-stu-id="21da0-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="21da0-113">本主題將討論下列內容：</span><span class="sxs-lookup"><span data-stu-id="21da0-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="21da0-114">Windows Vista 標準名稱</span><span class="sxs-lookup"><span data-stu-id="21da0-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="21da0-115">Windows Vista 的新命令</span><span class="sxs-lookup"><span data-stu-id="21da0-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="21da0-116">舊版主控台命令</span><span class="sxs-lookup"><span data-stu-id="21da0-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="21da0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="21da0-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="21da0-118">Windows Vista 標準名稱</span><span class="sxs-lookup"><span data-stu-id="21da0-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="21da0-119">在 Windows Vista 和更新版本中，從命令列啟動主控台專案的慣用方法是使用主控台專案的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="21da0-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="21da0-120">標準名稱是主控台專案在登錄中宣告的非當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="21da0-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="21da0-121">使用標準名稱的值，是它會將主控台專案的模組名稱抽象化。</span><span class="sxs-lookup"><span data-stu-id="21da0-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="21da0-122">專案可以在 .dll 中執行，稍後以 .exe 的形式根據或變更其模組名稱。</span><span class="sxs-lookup"><span data-stu-id="21da0-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="21da0-123">只要正式名稱維持不變，就不需要更新使用該正式名稱開啟該名稱的任何程式。</span><span class="sxs-lookup"><span data-stu-id="21da0-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="21da0-124">依照慣例，正式名稱的格式為 "CorporationName. ControlPanelItemName"。</span><span class="sxs-lookup"><span data-stu-id="21da0-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="21da0-125">下列範例顯示應用程式如何使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)來啟動主控台專案 **Windows Update** 。</span><span class="sxs-lookup"><span data-stu-id="21da0-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="21da0-126">若要使用其正式名稱啟動主控台專案，請使用： "% systemroot% \\ system32 \\control.exe/name *canonicalName*"</span><span class="sxs-lookup"><span data-stu-id="21da0-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="21da0-127">若要在專案中開啟特定的子頁面，或使用其他參數開啟它，請使用： "% systemroot% \\ system32 \\control.exe/name **canonicalName** /page **pageName**"</span><span class="sxs-lookup"><span data-stu-id="21da0-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="21da0-128">應用程式也可以執行 [**IOpenControlPanel：： open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) 方法來啟動主控台專案，包括開啟特定子頁面的能力。</span><span class="sxs-lookup"><span data-stu-id="21da0-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="21da0-129">如需主控台專案標準名稱的完整清單，請參閱 [主控台專案的正式名稱](controlpanel-canonical-names.md)。</span><span class="sxs-lookup"><span data-stu-id="21da0-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="21da0-130">Windows Vista 的新命令</span><span class="sxs-lookup"><span data-stu-id="21da0-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="21da0-131">在 Windows Vista 中，Windows XP 上的 cpl 模組所存取的某些選項現在會實作為 .exe 檔。</span><span class="sxs-lookup"><span data-stu-id="21da0-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="21da0-132">這可讓標準使用者在嘗試啟動檔案時提供系統管理員認證，以提供額外的安全性。</span><span class="sxs-lookup"><span data-stu-id="21da0-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="21da0-133">不需要額外安全性的選項，是透過 Windows XP 中使用的相同命令列來存取。</span><span class="sxs-lookup"><span data-stu-id="21da0-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="21da0-134">以下是 Windows Vista 中用來存取主控台專案特定索引標籤的命令清單：</span><span class="sxs-lookup"><span data-stu-id="21da0-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="21da0-135">個人化</span><span class="sxs-lookup"><span data-stu-id="21da0-135">Personalization</span></span>

-   <span data-ttu-id="21da0-136">字型大小和 DPI：% windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="21da0-137">螢幕解析度：% windir% \\ system32 \\control.exe desk.cpl，設定，@Settings</span><span class="sxs-lookup"><span data-stu-id="21da0-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="21da0-138">顯示設定：% windir% \\ system32 \\control.exe desk.cpl，設定，@Settings</span><span class="sxs-lookup"><span data-stu-id="21da0-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="21da0-139">主題：% windir% \\ system32 \\control.exe desk.cpl，主題，@Themes</span><span class="sxs-lookup"><span data-stu-id="21da0-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="21da0-140">螢幕保護裝置：% windir% \\ system32 \\control.exe desk.cpl、螢幕保護裝置程式@screensaver</span><span class="sxs-lookup"><span data-stu-id="21da0-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="21da0-141">多重監視器：% windir% \\ system32 \\control.exe desk.cpl，監視，@Monitor</span><span class="sxs-lookup"><span data-stu-id="21da0-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="21da0-142">色彩配置：% windir% \\ system32 \\control.exe/name Microsoft. 個人化/page pageColorization</span><span class="sxs-lookup"><span data-stu-id="21da0-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="21da0-143">桌面背景：% windir% \\ system32 \\control.exe/name Microsoft. 個人化/page pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="21da0-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="21da0-144">Starter 和 Basic 版本不支援 control.exe/name Microsoft 個人化命令。</span><span class="sxs-lookup"><span data-stu-id="21da0-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="21da0-145">系統</span><span class="sxs-lookup"><span data-stu-id="21da0-145">System</span></span>

-   <span data-ttu-id="21da0-146">效能：% windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="21da0-147">遠端存取：% windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="21da0-148">電腦名稱稱：% windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="21da0-149">系統保護：% windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="21da0-150">Advanced system properties：% windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="21da0-151">[程式和功能]</span><span class="sxs-lookup"><span data-stu-id="21da0-151">Programs and Features</span></span>

-   <span data-ttu-id="21da0-152">新增或移除程式：% windir% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="21da0-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="21da0-153">Windows 功能：% windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="21da0-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="21da0-154">地區及語言選項</span><span class="sxs-lookup"><span data-stu-id="21da0-154">Regional and Language Options</span></span>

-   <span data-ttu-id="21da0-155">鍵盤：% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p： "鍵盤"</span><span class="sxs-lookup"><span data-stu-id="21da0-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="21da0-156">位置：% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p： "location"</span><span class="sxs-lookup"><span data-stu-id="21da0-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="21da0-157">系統管理：% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p： "系統管理"</span><span class="sxs-lookup"><span data-stu-id="21da0-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="21da0-158">資料夾選項</span><span class="sxs-lookup"><span data-stu-id="21da0-158">Folder Options</span></span>

-   <span data-ttu-id="21da0-159">資料夾搜尋：% windir% \\ system32 \\rundll32.exe shell32.dll，選項 \_ RunDLL 2</span><span class="sxs-lookup"><span data-stu-id="21da0-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="21da0-160">檔案關聯：% windir% \\ system32 \\control.exe/name Microsoft. DefaultPrograms/page pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="21da0-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="21da0-161">View：% windir% \\ system32 \\rundll32.exe shell32.dll，Options \_ RunDLL 7</span><span class="sxs-lookup"><span data-stu-id="21da0-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="21da0-162">一般：% windir% \\ system32 \\rundll32.exe shell32.dll，選項 \_ RunDLL 0</span><span class="sxs-lookup"><span data-stu-id="21da0-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="21da0-163">電源選項</span><span class="sxs-lookup"><span data-stu-id="21da0-163">Power Options</span></span>

-   <span data-ttu-id="21da0-164">編輯目前的計畫設定：% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="21da0-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="21da0-165">系統設定：% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="21da0-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="21da0-166">建立電源計劃：% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="21da0-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="21da0-167">[Advanced Settings] 頁面沒有標準命令，它會以較舊的方式存取：% windir% \\ system32 \\control.exe powercfg.cpl，，3</span><span class="sxs-lookup"><span data-stu-id="21da0-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="21da0-168">舊版主控台命令</span><span class="sxs-lookup"><span data-stu-id="21da0-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="21da0-169">當您使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) 函數時，系統可以辨識特殊的主控台命令。</span><span class="sxs-lookup"><span data-stu-id="21da0-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="21da0-170">這些命令會早 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="21da0-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21da0-171">control.exe 桌面</span><span class="sxs-lookup"><span data-stu-id="21da0-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="21da0-172">啟動 <strong>顯示內容</strong> 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="21da0-173">Starter 和 Basic 版本不支援此命令。</span><span class="sxs-lookup"><span data-stu-id="21da0-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21da0-174">control.exe 色彩</span><span class="sxs-lookup"><span data-stu-id="21da0-174">control.exe color</span></span></td>
<td><span data-ttu-id="21da0-175">啟動已預先選取 [<strong>外觀</strong>] 索引標籤的 [<strong>顯示內容</strong>] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21da0-176">control.exe 日期/時間</span><span class="sxs-lookup"><span data-stu-id="21da0-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="21da0-177">啟動 [ <strong>日期和時間] 屬性</strong> 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21da0-178">control.exe 國際</span><span class="sxs-lookup"><span data-stu-id="21da0-178">control.exe international</span></span></td>
<td><span data-ttu-id="21da0-179">啟動 [ <strong>地區及語言選項</strong> ] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21da0-180">control.exe 滑鼠</span><span class="sxs-lookup"><span data-stu-id="21da0-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="21da0-181">啟動 <strong>滑鼠 [屬性</strong> ] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21da0-182">control.exe 鍵盤</span><span class="sxs-lookup"><span data-stu-id="21da0-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="21da0-183">啟動 [ <strong>鍵盤屬性</strong> ] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21da0-184">control.exe 印表機</span><span class="sxs-lookup"><span data-stu-id="21da0-184">control.exe printers</span></span></td>
<td><span data-ttu-id="21da0-185">顯示 [ <strong>印表機和傳真</strong> ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="21da0-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21da0-186">control.exe 字型</span><span class="sxs-lookup"><span data-stu-id="21da0-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="21da0-187">顯示 [ <strong>字型</strong> ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="21da0-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="21da0-188">針對 Windows 2000 和更新版本的系統：</span><span class="sxs-lookup"><span data-stu-id="21da0-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="21da0-189">control.exe 資料夾</span><span class="sxs-lookup"><span data-stu-id="21da0-189">control.exe folders</span></span>        | <span data-ttu-id="21da0-190">啟動 [ **資料夾選項** ] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="21da0-191">control.exe netware</span><span class="sxs-lookup"><span data-stu-id="21da0-191">control.exe netware</span></span>        | <span data-ttu-id="21da0-192">如果已安裝) ，則啟動 **Novell NetWare** 視窗 (。</span><span class="sxs-lookup"><span data-stu-id="21da0-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="21da0-193">control.exe 電話語音</span><span class="sxs-lookup"><span data-stu-id="21da0-193">control.exe telephony</span></span>      | <span data-ttu-id="21da0-194">啟動 [ **電話和數據機選項** ] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="21da0-195">control.exe admintools</span><span class="sxs-lookup"><span data-stu-id="21da0-195">control.exe admintools</span></span>     | <span data-ttu-id="21da0-196">顯示 [系統 **管理工具** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="21da0-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="21da0-197">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="21da0-197">control.exe schedtasks</span></span>     | <span data-ttu-id="21da0-198">顯示 [ **排定** 的工作] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="21da0-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="21da0-199">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="21da0-199">control.exe netconnections</span></span> | <span data-ttu-id="21da0-200">顯示 [ **網路連接** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="21da0-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="21da0-201">control.exe 紅外線</span><span class="sxs-lookup"><span data-stu-id="21da0-201">control.exe infrared</span></span>       | <span data-ttu-id="21da0-202">如果已安裝) ，會啟動 [ **紅外線監視器** ] 視窗 (。</span><span class="sxs-lookup"><span data-stu-id="21da0-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="21da0-203">control.exe userpasswords</span><span class="sxs-lookup"><span data-stu-id="21da0-203">control.exe userpasswords</span></span>  | <span data-ttu-id="21da0-204">啟動 [ **使用者帳戶** ] 視窗。</span><span class="sxs-lookup"><span data-stu-id="21da0-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="21da0-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="21da0-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21da0-206">主控台專案</span><span class="sxs-lookup"><span data-stu-id="21da0-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="21da0-207">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="21da0-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="21da0-208">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="21da0-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="21da0-209">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="21da0-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="21da0-210">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="21da0-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="21da0-211">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="21da0-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="21da0-212">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="21da0-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="21da0-213">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="21da0-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="21da0-214">在 Windows Vista 下存取安全模式下的主控台</span><span class="sxs-lookup"><span data-stu-id="21da0-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
