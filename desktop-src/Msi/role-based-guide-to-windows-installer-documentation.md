---
description: Windows Installer 是在 Windows 上安裝和設定應用程式的建議解決方案。
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Windows Installer 檔的以角色為基礎的指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026432"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="2a664-103">Windows Installer 檔的以角色為基礎的指南</span><span class="sxs-lookup"><span data-stu-id="2a664-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="2a664-104">Windows Installer 是在 Windows 上安裝和設定應用程式的建議解決方案。</span><span class="sxs-lookup"><span data-stu-id="2a664-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="2a664-105">因此，此 SDK 中包含的部分資訊會對各式各樣的軟體發展和 IT 專業人員感興趣。</span><span class="sxs-lookup"><span data-stu-id="2a664-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="2a664-106">這一節是以讀者的指南來提供，想要看到依專業角色和一般工作案例組織的主題連結。</span><span class="sxs-lookup"><span data-stu-id="2a664-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="2a664-107">因為組織之間的角色可能會有極大的差異，所以必須將下列群組視為要開始搜尋所需資訊的位置指南。</span><span class="sxs-lookup"><span data-stu-id="2a664-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="2a664-108">應用程式開發人員</span><span class="sxs-lookup"><span data-stu-id="2a664-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="2a664-109">設定作者</span><span class="sxs-lookup"><span data-stu-id="2a664-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="2a664-110">IT 專業人員</span><span class="sxs-lookup"><span data-stu-id="2a664-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="2a664-111">基礎結構開發人員</span><span class="sxs-lookup"><span data-stu-id="2a664-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="2a664-112">本檔適用于想要讓應用程式使用 Windows Installer 的軟體發展人員。</span><span class="sxs-lookup"><span data-stu-id="2a664-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="2a664-113">SDK 是安裝程式參考資料的主要來源，提供安裝套件和安裝程式服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a664-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="2a664-114">它包含應用程式開發介面的完整描述 (API) 和安裝程式資料庫的元素。</span><span class="sxs-lookup"><span data-stu-id="2a664-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="2a664-115">如需詳細資訊，請參閱 [Windows Installer 資訊的其他來源](other-sources-of-windows-installer-information.md)。</span><span class="sxs-lookup"><span data-stu-id="2a664-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="2a664-116">應用程式開發人員</span><span class="sxs-lookup"><span data-stu-id="2a664-116">Application Developers</span></span>

<span data-ttu-id="2a664-117">應用程式開發人員建立的應用程式會呼叫 Windows Installer 應用程式開發介面，並在執行時間安裝 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="2a664-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="2a664-118">Windows Installer 可以在應用程式中工作，例如自行修復和隨選安裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="2a664-119">一般來說，應用程式開發人員會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="2a664-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="2a664-120">在執行時間從另一個應用程式中啟用應用程式的隨選安裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="2a664-121">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-122">使用安裝程式函數</span><span class="sxs-lookup"><span data-stu-id="2a664-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="2a664-123">安裝程式函數參考</span><span class="sxs-lookup"><span data-stu-id="2a664-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-124">隨選安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="2a664-125">元件管理</span><span class="sxs-lookup"><span data-stu-id="2a664-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="2a664-126">編輯安裝程式快捷方式</span><span class="sxs-lookup"><span data-stu-id="2a664-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="2a664-127">**OLEAdvtSupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="2a664-128">廣告的平臺支援</span><span class="sxs-lookup"><span data-stu-id="2a664-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="2a664-129">在執行時間視需要重新安裝元件，以啟用應用程式的自我修復。</span><span class="sxs-lookup"><span data-stu-id="2a664-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="2a664-130">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-131">使用安裝程式函數</span><span class="sxs-lookup"><span data-stu-id="2a664-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="2a664-132">安裝程式函數參考</span><span class="sxs-lookup"><span data-stu-id="2a664-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-133">復原</span><span class="sxs-lookup"><span data-stu-id="2a664-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="2a664-134">來源復原</span><span class="sxs-lookup"><span data-stu-id="2a664-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="2a664-135">搜尋中斷的功能或元件</span><span class="sxs-lookup"><span data-stu-id="2a664-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="2a664-136">取代現有的檔案</span><span class="sxs-lookup"><span data-stu-id="2a664-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="2a664-137">顯示使用者介面，以便在第一次安裝或執行應用程式時，收集使用者資訊和設定喜好設定。</span><span class="sxs-lookup"><span data-stu-id="2a664-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="2a664-138">使用者介面必須由 Windows Installer 套件的安裝程式作者加入。</span><span class="sxs-lookup"><span data-stu-id="2a664-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="2a664-139">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-140">使用安裝程式函數</span><span class="sxs-lookup"><span data-stu-id="2a664-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="2a664-141">初始化應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="2a664-142">Firstrun.cmd 對話方塊</span><span class="sxs-lookup"><span data-stu-id="2a664-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="2a664-143">關於消費者介面</span><span class="sxs-lookup"><span data-stu-id="2a664-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="2a664-144">建立應用程式，使用間接模型來參考具有平行功能的元件。</span><span class="sxs-lookup"><span data-stu-id="2a664-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="2a664-145">Windows Installer 套件的安裝程式作者必須加入限定的元件類別。</span><span class="sxs-lookup"><span data-stu-id="2a664-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="2a664-146">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-147">合格元件</span><span class="sxs-lookup"><span data-stu-id="2a664-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="2a664-148">使用限定元件</span><span class="sxs-lookup"><span data-stu-id="2a664-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="2a664-149">使用私用和並存元件來隔離應用程式並減少 DLL 衝突。</span><span class="sxs-lookup"><span data-stu-id="2a664-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="2a664-150">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-151">組件</span><span class="sxs-lookup"><span data-stu-id="2a664-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="2a664-152">Windows Installer 所寫入的元件登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="2a664-153">在 Windows XP 上安裝適用于並存共用的 Win32 元件</span><span class="sxs-lookup"><span data-stu-id="2a664-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="2a664-154">在 Windows XP 上安裝 Win32 元件以私用應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="2a664-155">MsiAssembly 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="2a664-156">MsiAssemblyName 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="2a664-157">**MsiProvideAssembly**</span><span class="sxs-lookup"><span data-stu-id="2a664-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="2a664-158">**MsiWin32AssemblySupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="2a664-159">**MsiNetAssemblySupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="2a664-160">**隔離的元件**</span><span class="sxs-lookup"><span data-stu-id="2a664-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="2a664-161">準備應用程式來安裝自己的完整主要升級。</span><span class="sxs-lookup"><span data-stu-id="2a664-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="2a664-162">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-163">修補和升級</span><span class="sxs-lookup"><span data-stu-id="2a664-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2a664-164">主要升級</span><span class="sxs-lookup"><span data-stu-id="2a664-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="2a664-165">**UpgradeCode 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="2a664-166">**使用 UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="2a664-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="2a664-167">防止舊套件安裝在較新的版本上</span><span class="sxs-lookup"><span data-stu-id="2a664-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="2a664-168">準備應用程式以安裝自己的次要升級、小型更新或修正。</span><span class="sxs-lookup"><span data-stu-id="2a664-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="2a664-169">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-170">修補和升級</span><span class="sxs-lookup"><span data-stu-id="2a664-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2a664-171">小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="2a664-172">次要升級</span><span class="sxs-lookup"><span data-stu-id="2a664-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="2a664-173">將應用程式資源組織成可搭配 Windows Installer 使用的元件。</span><span class="sxs-lookup"><span data-stu-id="2a664-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="2a664-174">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-175">Windows Installer 元件</span><span class="sxs-lookup"><span data-stu-id="2a664-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="2a664-176">使用功能和元件</span><span class="sxs-lookup"><span data-stu-id="2a664-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="2a664-177">使用可轉移的元件</span><span class="sxs-lookup"><span data-stu-id="2a664-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="2a664-178">如果元件規則中斷，會發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="2a664-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="2a664-179">將應用程式組織成元件</span><span class="sxs-lookup"><span data-stu-id="2a664-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="2a664-180">隔離的元件</span><span class="sxs-lookup"><span data-stu-id="2a664-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="2a664-181">合格元件</span><span class="sxs-lookup"><span data-stu-id="2a664-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="2a664-182">設定作者</span><span class="sxs-lookup"><span data-stu-id="2a664-182">Setup Authors</span></span>

<span data-ttu-id="2a664-183">安裝程式作者會建立 ( .msi 檔案) 的 Windows Installer 封裝，其中包含安裝應用程式所需的安裝程式邏輯和資訊。</span><span class="sxs-lookup"><span data-stu-id="2a664-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="2a664-184">它們通常會使用撰寫工具（例如 [Orca.exe](orca-exe.md) ），以安裝程式邏輯和資訊填入 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="2a664-185">一般而言，安裝程式作者會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="2a664-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="2a664-186">判斷不同 Windows Installer 版本所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="2a664-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="2a664-187">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-188">判斷 Windows Installer 版本</span><span class="sxs-lookup"><span data-stu-id="2a664-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="2a664-189">Windows Installer 的發行版本</span><span class="sxs-lookup"><span data-stu-id="2a664-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="2a664-190">Windows Installer 的新功能</span><span class="sxs-lookup"><span data-stu-id="2a664-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="2a664-191">將應用程式資源組織成 Windows Installer 元件。</span><span class="sxs-lookup"><span data-stu-id="2a664-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="2a664-192">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-193">Windows Installer 元件</span><span class="sxs-lookup"><span data-stu-id="2a664-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="2a664-194">將應用程式組織成元件</span><span class="sxs-lookup"><span data-stu-id="2a664-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="2a664-195">變更元件程式碼</span><span class="sxs-lookup"><span data-stu-id="2a664-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="2a664-196">如果元件規則中斷，會發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="2a664-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="2a664-197">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-198">使用協力廠商 Windows Installer 套件撰寫工具或 SDK 工具（例如 [Orca.exe](orca-exe.md) ）來填入安裝資料庫，並建立 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="2a664-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="2a664-199">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-200">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="2a664-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="2a664-201">安裝套件，關於安裝程式資料庫</span><span class="sxs-lookup"><span data-stu-id="2a664-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="2a664-202">Windows Installer 副檔名</span><span class="sxs-lookup"><span data-stu-id="2a664-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="2a664-203">資料庫資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="2a664-204">封裝碼</span><span class="sxs-lookup"><span data-stu-id="2a664-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="2a664-205">撰寫大型封裝</span><span class="sxs-lookup"><span data-stu-id="2a664-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="2a664-206">64位作業系統上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2a664-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="2a664-207">命名自訂資料表、屬性和動作</span><span class="sxs-lookup"><span data-stu-id="2a664-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="2a664-208">資料流程的 OLE 限制</span><span class="sxs-lookup"><span data-stu-id="2a664-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="2a664-209">資料行定義格式</span><span class="sxs-lookup"><span data-stu-id="2a664-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="2a664-210">減少 .msi 檔案的大小</span><span class="sxs-lookup"><span data-stu-id="2a664-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="2a664-211">撰寫 Windows Installer 資料庫以安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="2a664-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="2a664-212">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-213">核心資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2a664-214">檔案資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="2a664-215">FileTable</span><span class="sxs-lookup"><span data-stu-id="2a664-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="2a664-216">檔案搜尋</span><span class="sxs-lookup"><span data-stu-id="2a664-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="2a664-217">檔案成本</span><span class="sxs-lookup"><span data-stu-id="2a664-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="2a664-218">檔案安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="2a664-219">隨附檔案</span><span class="sxs-lookup"><span data-stu-id="2a664-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="2a664-220">檔案版本控制規則</span><span class="sxs-lookup"><span data-stu-id="2a664-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="2a664-221">預設檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="2a664-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="2a664-222">取代現有的檔案</span><span class="sxs-lookup"><span data-stu-id="2a664-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="2a664-223">使用封包和壓縮的來源</span><span class="sxs-lookup"><span data-stu-id="2a664-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="2a664-224">移除擱置的檔案</span><span class="sxs-lookup"><span data-stu-id="2a664-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="2a664-225">安裝永久元件、檔案、字型、登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="2a664-226">FileSFPCatalog 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="2a664-227">搜尋檔案並建立保存檔案路徑的屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="2a664-228">搜尋目錄和目錄中的檔案</span><span class="sxs-lookup"><span data-stu-id="2a664-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="2a664-229">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-230">撰寫安裝目錄結構和資料夾的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="2a664-231">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-232">核心資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2a664-233">檔案資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="2a664-234">元件資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="2a664-235">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="2a664-236">使用目錄資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="2a664-237">使用路徑中的目錄屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="2a664-238">系統資料夾屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="2a664-239">CreateFolder 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="2a664-240">LockPermissions 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="2a664-241">MsiLockPermissionsEx 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="2a664-242">變更目錄的目標位置</span><span class="sxs-lookup"><span data-stu-id="2a664-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="2a664-243">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-244">撰寫會安裝登錄機碼的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="2a664-245">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-246">核心資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2a664-247">登錄資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="2a664-248">登錄資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="2a664-249">修改登錄</span><span class="sxs-lookup"><span data-stu-id="2a664-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="2a664-250">在安裝或移除元件時新增或移除登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="2a664-251">新增和移除應用程式，而不在登錄中保留任何追蹤</span><span class="sxs-lookup"><span data-stu-id="2a664-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="2a664-252">安裝永久元件、檔案、字型、登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="2a664-253">搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案</span><span class="sxs-lookup"><span data-stu-id="2a664-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="2a664-254">搜尋登錄專案，並建立保存登錄值的屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="2a664-255">Windows Installer 所寫入的元件登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="2a664-256">卸載登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="2a664-257">SelfReg 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="2a664-258">指定自我註冊的順序</span><span class="sxs-lookup"><span data-stu-id="2a664-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="2a664-259">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-260">撰寫安裝服務的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="2a664-261">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-262">ServiceInstall 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="2a664-263">ServiceControl 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="2a664-264">元件資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="2a664-265">撰寫可安裝隔離元件或 COM 元件的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="2a664-266">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-267">登錄資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="2a664-268">類別資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="2a664-269">Complus 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="2a664-270">隔離的元件</span><span class="sxs-lookup"><span data-stu-id="2a664-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="2a664-271">使用隔離的元件</span><span class="sxs-lookup"><span data-stu-id="2a664-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="2a664-272">獨立元件的安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="2a664-273">重新安裝隔離的元件</span><span class="sxs-lookup"><span data-stu-id="2a664-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="2a664-274">移除隔離的元件</span><span class="sxs-lookup"><span data-stu-id="2a664-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="2a664-275">將 COM 元件安裝至私用位置</span><span class="sxs-lookup"><span data-stu-id="2a664-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="2a664-276">使現有封裝中的 COM 元件成為私用</span><span class="sxs-lookup"><span data-stu-id="2a664-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="2a664-277">安裝具有 Windows Installer 的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="2a664-278">將非 COM 元件安裝至私用位置</span><span class="sxs-lookup"><span data-stu-id="2a664-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="2a664-279">將現有封裝中的非 COM 元件設為私用</span><span class="sxs-lookup"><span data-stu-id="2a664-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="2a664-280">撰寫安裝元件的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="2a664-281">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-282">MsiAssembly 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="2a664-283">MsiAssemblyName 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="2a664-284">組件</span><span class="sxs-lookup"><span data-stu-id="2a664-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="2a664-285">Windows Installer 所寫入的元件登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="2a664-286">Win32 元件的安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="2a664-287">撰寫安裝 ODBC 驅動程式和轉譯程式的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="2a664-288">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-289">ODBCAttribute 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="2a664-290">ODBCDriver 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="2a664-291">ODBCTranslator 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="2a664-292">ODBCDataSource 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="2a664-293">ODBCSourceAttribute 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="2a664-294">撰寫可安裝 MIME 的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="2a664-295">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-296">MIME 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="2a664-297">延伸模組資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="2a664-298">修改登錄</span><span class="sxs-lookup"><span data-stu-id="2a664-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="2a664-299">撰寫會安裝環境變數的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="2a664-300">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-301">環境資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="2a664-302">撰寫可安裝快速鍵的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="2a664-303">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-304">快速鍵資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="2a664-305">MsiShortcutProperty 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="2a664-306">編輯安裝程式快捷方式</span><span class="sxs-lookup"><span data-stu-id="2a664-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="2a664-307">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-308">撰寫安裝多個應用程式實例的 Windows Installer 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2a664-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="2a664-309">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-310">安裝多個產品和修補程式實例</span><span class="sxs-lookup"><span data-stu-id="2a664-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="2a664-311">使用實例轉換撰寫多個實例</span><span class="sxs-lookup"><span data-stu-id="2a664-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="2a664-312">使用實例轉換安裝多個實例</span><span class="sxs-lookup"><span data-stu-id="2a664-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="2a664-313">指定預設功能選取狀態和選項。</span><span class="sxs-lookup"><span data-stu-id="2a664-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="2a664-314">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-315">核心資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="2a664-316">元件資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="2a664-317">功能資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="2a664-318">FeatureComponents 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="2a664-319">控制特徵選取狀態</span><span class="sxs-lookup"><span data-stu-id="2a664-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="2a664-320">功能安裝選項屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="2a664-321">指定必須符合才能安裝應用程式或選定元件的條件。</span><span class="sxs-lookup"><span data-stu-id="2a664-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="2a664-322">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-323">條件資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="2a664-324">LaunchCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="2a664-325">元件資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="2a664-326">在條件陳述式中使用屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="2a664-327">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="2a664-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="2a664-328">要在移除期間執行的調節動作</span><span class="sxs-lookup"><span data-stu-id="2a664-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="2a664-329">條件陳述式語法的範例</span><span class="sxs-lookup"><span data-stu-id="2a664-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="2a664-330">撰寫用來安裝應用程式的動作順序。</span><span class="sxs-lookup"><span data-stu-id="2a664-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="2a664-331">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-332">使用順序資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="2a664-333">安裝程式資料表群組</span><span class="sxs-lookup"><span data-stu-id="2a664-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="2a664-334">順序資料表詳細範例</span><span class="sxs-lookup"><span data-stu-id="2a664-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="2a664-335">具有排序限制的動作</span><span class="sxs-lookup"><span data-stu-id="2a664-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="2a664-336">沒有排序限制的動作</span><span class="sxs-lookup"><span data-stu-id="2a664-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="2a664-337">在條件陳述式中使用屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="2a664-338">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="2a664-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="2a664-339">條件陳述式語法的範例</span><span class="sxs-lookup"><span data-stu-id="2a664-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="2a664-340">要在移除期間執行的調節動作</span><span class="sxs-lookup"><span data-stu-id="2a664-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="2a664-341">標準動作</span><span class="sxs-lookup"><span data-stu-id="2a664-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="2a664-342">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-343">準備應用程式的安裝套件，以便日後 Windows Installer 服務升級應用程式。</span><span class="sxs-lookup"><span data-stu-id="2a664-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="2a664-344">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-345">修補和升級</span><span class="sxs-lookup"><span data-stu-id="2a664-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2a664-346">準備應用程式以進行未來的主要升級</span><span class="sxs-lookup"><span data-stu-id="2a664-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="2a664-347">使用 UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="2a664-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="2a664-348">升級資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="2a664-349">**UpgradeCode 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="2a664-350">防止舊套件安裝在較新的版本上</span><span class="sxs-lookup"><span data-stu-id="2a664-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="2a664-351">變更產品代碼</span><span class="sxs-lookup"><span data-stu-id="2a664-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="2a664-352">更新組件</span><span class="sxs-lookup"><span data-stu-id="2a664-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="2a664-353">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2a664-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="2a664-354">針對開發中的 Windows Installer 套件進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="2a664-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="2a664-355">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-356">套件驗證</span><span class="sxs-lookup"><span data-stu-id="2a664-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="2a664-357">內部一致性評估工具-Ices-003</span><span class="sxs-lookup"><span data-stu-id="2a664-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="2a664-358">Windows Installer 記錄</span><span class="sxs-lookup"><span data-stu-id="2a664-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="2a664-359">檢查功能、元件、檔案的安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="2a664-360">撰寫大型封裝</span><span class="sxs-lookup"><span data-stu-id="2a664-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="2a664-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="2a664-362">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="2a664-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="2a664-363">驗證合併模組</span><span class="sxs-lookup"><span data-stu-id="2a664-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="2a664-364">驗證安裝資料庫</span><span class="sxs-lookup"><span data-stu-id="2a664-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="2a664-365">驗證安裝升級</span><span class="sxs-lookup"><span data-stu-id="2a664-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="2a664-366">搜尋中斷的功能或元件</span><span class="sxs-lookup"><span data-stu-id="2a664-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="2a664-367">Windows Installer 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="2a664-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="2a664-368">重新開機要求的記錄</span><span class="sxs-lookup"><span data-stu-id="2a664-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="2a664-369">確保應用程式的安全安裝和安裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="2a664-370">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-371">撰寫安全安裝的指導方針</span><span class="sxs-lookup"><span data-stu-id="2a664-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="2a664-372">保護自訂動作的指導方針</span><span class="sxs-lookup"><span data-stu-id="2a664-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="2a664-373">自訂動作安全性</span><span class="sxs-lookup"><span data-stu-id="2a664-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="2a664-374">在鎖定的電腦上保護套件安全的指導方針</span><span class="sxs-lookup"><span data-stu-id="2a664-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="2a664-375">使用自動化撰寫經過完整驗證的已簽署安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="2a664-376">以 URL 為基礎的 Windows Installer 安裝範例</span><span class="sxs-lookup"><span data-stu-id="2a664-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="2a664-377">撰寫密碼輸入的消費者介面</span><span class="sxs-lookup"><span data-stu-id="2a664-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="2a664-378">數位簽章和 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2a664-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="2a664-379">搭配使用 Windows Installer 與 UAC</span><span class="sxs-lookup"><span data-stu-id="2a664-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="2a664-380"> (UAC) 修補的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="2a664-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="2a664-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="2a664-382">**AdminUser 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="2a664-383">**具有特殊許可權的屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="2a664-384">**SecureCustomProperties 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="2a664-385">建立使用者介面，以顯示設定安裝的選項，並向使用者取得擱置安裝程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a664-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="2a664-386">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-387">關於消費者介面</span><span class="sxs-lookup"><span data-stu-id="2a664-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="2a664-388">加入控制項和文字</span><span class="sxs-lookup"><span data-stu-id="2a664-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="2a664-389">撰寫 ProgressBar 控制項</span><span class="sxs-lookup"><span data-stu-id="2a664-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="2a664-390">撰寫磁片提示訊息</span><span class="sxs-lookup"><span data-stu-id="2a664-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="2a664-391">撰寫條件式「請稍候 ...」訊息方塊</span><span class="sxs-lookup"><span data-stu-id="2a664-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="2a664-392">預覽消費者介面</span><span class="sxs-lookup"><span data-stu-id="2a664-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="2a664-393">加入儲存在屬性中的文字</span><span class="sxs-lookup"><span data-stu-id="2a664-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="2a664-394">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="2a664-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="2a664-395">建立外部使用者介面來呈現自訂使用者介面，以設定安裝並從使用者取得有關擱置安裝程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="2a664-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="2a664-396">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-397">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="2a664-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="2a664-398">使用 MsiSetExternalUIRecord 監視安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="2a664-399">剖析 Windows Installer 訊息</span><span class="sxs-lookup"><span data-stu-id="2a664-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="2a664-400">從外部消費者介面處理常式傳回值</span><span class="sxs-lookup"><span data-stu-id="2a664-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="2a664-401">INSTALLUI \_ 處理常式</span><span class="sxs-lookup"><span data-stu-id="2a664-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="2a664-402">使用 MsiSetExternalUI 處理進度訊息</span><span class="sxs-lookup"><span data-stu-id="2a664-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="2a664-403">使用 MsiSetExternalUI 監視安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="2a664-404">在 [ **新增/移除程式** ] (ARP 中設定應用程式的資訊 ) </span><span class="sxs-lookup"><span data-stu-id="2a664-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="2a664-405">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-406">使用 Windows Installer 設定新增/移除程式</span><span class="sxs-lookup"><span data-stu-id="2a664-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="2a664-407">新增和移除應用程式，而不在登錄中保留任何追蹤</span><span class="sxs-lookup"><span data-stu-id="2a664-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="2a664-408">卸載登錄機碼</span><span class="sxs-lookup"><span data-stu-id="2a664-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="2a664-409">撰寫自訂動作來處理 Windows Installer 原本就不支援的安裝邏輯。</span><span class="sxs-lookup"><span data-stu-id="2a664-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="2a664-410">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-411">自訂動作</span><span class="sxs-lookup"><span data-stu-id="2a664-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="2a664-412">所有自訂動作類型的摘要清單</span><span class="sxs-lookup"><span data-stu-id="2a664-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="2a664-413">保護自訂動作的指導方針</span><span class="sxs-lookup"><span data-stu-id="2a664-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="2a664-414">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="2a664-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="2a664-415">使用自訂動作在本機電腦上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="2a664-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="2a664-416">使用自訂動作在安裝結束時啟動已安裝的檔案</span><span class="sxs-lookup"><span data-stu-id="2a664-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="2a664-417">從自訂動作內部存取資料庫或會話</span><span class="sxs-lookup"><span data-stu-id="2a664-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="2a664-418">從自訂動作內部存取目前的安裝程式會話</span><span class="sxs-lookup"><span data-stu-id="2a664-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="2a664-419">使用自訂動作變更系統狀態</span><span class="sxs-lookup"><span data-stu-id="2a664-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="2a664-420">在使用者的電腦上啟動 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="2a664-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="2a664-421">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-422">引導</span><span class="sxs-lookup"><span data-stu-id="2a664-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="2a664-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="2a664-424">網際網路下載啟動載入</span><span class="sxs-lookup"><span data-stu-id="2a664-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="2a664-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="2a664-426">以 URL 為基礎的 Windows Installer 安裝範例</span><span class="sxs-lookup"><span data-stu-id="2a664-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="2a664-427">設定 Setup.exe 資源</span><span class="sxs-lookup"><span data-stu-id="2a664-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="2a664-428">從網際網路下載安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="2a664-429">撰寫 Windows Installer 封裝時，請遵循 Active Accessibility 的指導方針。</span><span class="sxs-lookup"><span data-stu-id="2a664-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="2a664-430">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-431">協助工具</span><span class="sxs-lookup"><span data-stu-id="2a664-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="2a664-432">為應用程式設定的國際化做好準備。</span><span class="sxs-lookup"><span data-stu-id="2a664-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="2a664-433">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="2a664-434">[準備 Windows Installer 套件進行當地語系化](preparing-a-windows-installer-package-for-localization.md)，</span><span class="sxs-lookup"><span data-stu-id="2a664-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="2a664-435">當地語系化 Windows Installer 套件</span><span class="sxs-lookup"><span data-stu-id="2a664-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="2a664-436">程式字碼頁處理 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="2a664-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="2a664-437">新增當地語系化的資源</span><span class="sxs-lookup"><span data-stu-id="2a664-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="2a664-438">當地語系化範例</span><span class="sxs-lookup"><span data-stu-id="2a664-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="2a664-439">將錯誤和 ActionText 表當地語系化</span><span class="sxs-lookup"><span data-stu-id="2a664-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="2a664-440">當地語系化資料庫資料行</span><span class="sxs-lookup"><span data-stu-id="2a664-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="2a664-441">使用中性字碼頁建立資料庫</span><span class="sxs-lookup"><span data-stu-id="2a664-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="2a664-442">匯入和匯出資料表的字碼頁處理</span><span class="sxs-lookup"><span data-stu-id="2a664-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="2a664-443">將對話方塊所顯示的語言當地語系化</span><span class="sxs-lookup"><span data-stu-id="2a664-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="2a664-444">匯入當地語系化的錯誤和 ActionText 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="2a664-445">更新 ProductLanguage 和 ProductCode 屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="2a664-446">更新摘要資訊資料流程</span><span class="sxs-lookup"><span data-stu-id="2a664-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="2a664-447">合格元件</span><span class="sxs-lookup"><span data-stu-id="2a664-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="2a664-448">UIText 資料表</span><span class="sxs-lookup"><span data-stu-id="2a664-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="2a664-449">管理語言和字碼頁</span><span class="sxs-lookup"><span data-stu-id="2a664-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="2a664-450">檢查安裝資料庫字碼頁</span><span class="sxs-lookup"><span data-stu-id="2a664-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="2a664-451">建立32位和64位平臺 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="2a664-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="2a664-452">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-453">64位作業系統上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2a664-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="2a664-454">64位自訂動作</span><span class="sxs-lookup"><span data-stu-id="2a664-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="2a664-455">使用64位自訂動作</span><span class="sxs-lookup"><span data-stu-id="2a664-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="2a664-456">使用64位合併模組</span><span class="sxs-lookup"><span data-stu-id="2a664-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="2a664-457">將共用的 Windows Installer 元件和設定邏輯轉散發為合併模組。</span><span class="sxs-lookup"><span data-stu-id="2a664-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="2a664-458">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-459">合併模組</span><span class="sxs-lookup"><span data-stu-id="2a664-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="2a664-460">撰寫多個語言合併模組的語言轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="2a664-461">套用可設定的合併模組與自訂</span><span class="sxs-lookup"><span data-stu-id="2a664-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="2a664-462">排程或隱藏 Windows Installer 安裝期間的重新開機。</span><span class="sxs-lookup"><span data-stu-id="2a664-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="2a664-463">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-464">系統重新開機</span><span class="sxs-lookup"><span data-stu-id="2a664-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="2a664-465">重新開機要求的記錄</span><span class="sxs-lookup"><span data-stu-id="2a664-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="2a664-466">藉由建立修補程式來為現有的應用程式建立更新或修正。</span><span class="sxs-lookup"><span data-stu-id="2a664-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="2a664-467">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-468">建立小型更新修補程式</span><span class="sxs-lookup"><span data-stu-id="2a664-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="2a664-469">小型更新修補範例</span><span class="sxs-lookup"><span data-stu-id="2a664-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="2a664-470">撰寫一個可針對目前使用者或電腦的所有使用者安裝應用程式的雙重用途套件。</span><span class="sxs-lookup"><span data-stu-id="2a664-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="2a664-471">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-472">安裝內容</span><span class="sxs-lookup"><span data-stu-id="2a664-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="2a664-473">單一套件撰寫</span><span class="sxs-lookup"><span data-stu-id="2a664-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="2a664-474">單一套件撰寫範例</span><span class="sxs-lookup"><span data-stu-id="2a664-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="2a664-475">使用 Windows Installer 自訂電腦上的服務。</span><span class="sxs-lookup"><span data-stu-id="2a664-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="2a664-476">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-477">使用服務設定</span><span class="sxs-lookup"><span data-stu-id="2a664-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="2a664-478">使用 Windows Installer 保護電腦上的資源。</span><span class="sxs-lookup"><span data-stu-id="2a664-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="2a664-479">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-480">撰寫安全安裝的指導方針</span><span class="sxs-lookup"><span data-stu-id="2a664-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="2a664-481">保護資源</span><span class="sxs-lookup"><span data-stu-id="2a664-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="2a664-482">列舉電腦上安裝的所有元件，並取得元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="2a664-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="2a664-483">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-484">列舉元件</span><span class="sxs-lookup"><span data-stu-id="2a664-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="2a664-485">使用 [*交易處理*](t-gly.md)來安裝多個封裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="2a664-486">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-487">多套件安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="2a664-488">在 Windows Installer 套件中內嵌自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="2a664-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="2a664-489">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-490">使用使用者介面</span><span class="sxs-lookup"><span data-stu-id="2a664-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="2a664-491">使用內嵌 UI</span><span class="sxs-lookup"><span data-stu-id="2a664-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="2a664-492">IT 專業人員</span><span class="sxs-lookup"><span data-stu-id="2a664-492">IT Professionals</span></span>

<span data-ttu-id="2a664-493">IT 專業人員和系統管理員會自訂及部署現有的 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="2a664-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="2a664-494">這些使用者會將現有應用程式的安裝程式重新封裝成 Windows Installer 安裝套件，並安裝和維護網路上 Windows Installer 安裝的系統管理映射。</span><span class="sxs-lookup"><span data-stu-id="2a664-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="2a664-495">藉由產生和套用 Windows Installer 轉換來自訂應用程式和設定</span><span class="sxs-lookup"><span data-stu-id="2a664-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="2a664-496">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-497">自訂</span><span class="sxs-lookup"><span data-stu-id="2a664-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="2a664-498">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="2a664-499">自訂轉換範例</span><span class="sxs-lookup"><span data-stu-id="2a664-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="2a664-500">合併和轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="2a664-501">使用轉換來新增資源</span><span class="sxs-lookup"><span data-stu-id="2a664-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="2a664-502">產生轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="2a664-503">命令列選項</span><span class="sxs-lookup"><span data-stu-id="2a664-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="2a664-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="2a664-505">套用轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="2a664-506">查看轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="2a664-507">查看兩個資料庫之間的差異</span><span class="sxs-lookup"><span data-stu-id="2a664-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="2a664-508">修補自訂應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="2a664-509">部署 Windows Installer 安裝套件、更新或修補程式。</span><span class="sxs-lookup"><span data-stu-id="2a664-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="2a664-510">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-511">安裝應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="2a664-512">修補和升級</span><span class="sxs-lookup"><span data-stu-id="2a664-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="2a664-513">轉換</span><span class="sxs-lookup"><span data-stu-id="2a664-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="2a664-514">以較高的許可權安裝非系統管理員的封裝</span><span class="sxs-lookup"><span data-stu-id="2a664-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="2a664-515">藉由修補產品的本機安裝來套用主要升級</span><span class="sxs-lookup"><span data-stu-id="2a664-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="2a664-516">藉由安裝產品來套用主要升級</span><span class="sxs-lookup"><span data-stu-id="2a664-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="2a664-517">藉由修補產品的本機安裝來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="2a664-518">重新安裝產品以套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="2a664-519">藉由修補系統管理映射來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="2a664-520">修補初始安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="2a664-521">命令列選項</span><span class="sxs-lookup"><span data-stu-id="2a664-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="2a664-522">針對 Windows Installer 套件進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="2a664-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="2a664-523">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-524">Windows Installer 記錄</span><span class="sxs-lookup"><span data-stu-id="2a664-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="2a664-525">檢查功能、元件、檔案的安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="2a664-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="2a664-527">搜尋中斷的功能或元件</span><span class="sxs-lookup"><span data-stu-id="2a664-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="2a664-528">Windows Installer 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="2a664-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="2a664-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="2a664-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="2a664-530">使用腳本來查詢 Windows Installer 套件，以取得產品的相關資訊並修改安裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="2a664-531">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-532">Automation 介面</span><span class="sxs-lookup"><span data-stu-id="2a664-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="2a664-533">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="2a664-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="2a664-534">搭配使用 Windows Installer 與 WMI</span><span class="sxs-lookup"><span data-stu-id="2a664-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="2a664-535">建立和維護系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="2a664-536">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-537">系統管理安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="2a664-538">命令列選項</span><span class="sxs-lookup"><span data-stu-id="2a664-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="2a664-539">**AdminProperties 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="2a664-540">藉由修補系統管理映射來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="2a664-541">將修補套件套用至系統管理安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="2a664-542">動作執行順序</span><span class="sxs-lookup"><span data-stu-id="2a664-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="2a664-543">**IsAdminPackage 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="2a664-544">屬性優先順序的順序</span><span class="sxs-lookup"><span data-stu-id="2a664-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="2a664-545">**AdminProperties 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="2a664-546">將應用程式提供給電腦的所有使用者或僅供指定的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="2a664-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="2a664-547">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-548">安裝內容</span><span class="sxs-lookup"><span data-stu-id="2a664-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="2a664-549">**ALLUSERS 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="2a664-550">使用命令列來解讀套件、安裝產品和設定功能選項。</span><span class="sxs-lookup"><span data-stu-id="2a664-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="2a664-551">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-552">命令列選項</span><span class="sxs-lookup"><span data-stu-id="2a664-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="2a664-553">在命令列上設定公用屬性值</span><span class="sxs-lookup"><span data-stu-id="2a664-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="2a664-554">取得和設定屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="2a664-555">重新安裝功能或應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="2a664-556">藉由修補產品的本機安裝來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="2a664-557">重新安裝產品以套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="2a664-558">變更目錄的目標位置</span><span class="sxs-lookup"><span data-stu-id="2a664-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="2a664-559">藉由修補系統管理映射來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="2a664-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="2a664-560">藉由安裝產品來套用主要升級</span><span class="sxs-lookup"><span data-stu-id="2a664-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="2a664-561">設定屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="2a664-562">功能安裝選項屬性</span><span class="sxs-lookup"><span data-stu-id="2a664-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="2a664-563">使用原則來管理存取權和許可權。</span><span class="sxs-lookup"><span data-stu-id="2a664-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="2a664-564">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="2a664-565">[電腦原則](machine-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2a664-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="2a664-566">[使用者原則](user-policies.md)</span><span class="sxs-lookup"><span data-stu-id="2a664-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="2a664-567">以較高的許可權安裝非系統管理員的封裝</span><span class="sxs-lookup"><span data-stu-id="2a664-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="2a664-568">廣告以較高的許可權安裝的 Per-User 應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="2a664-569">使用自訂動作在本機電腦上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="2a664-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="2a664-570">**AdminUser 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="2a664-571">**具有特殊許可權的屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="2a664-572">**EnableUserControl 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="2a664-573">**UserSID 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="2a664-574">**SecureCustomProperties 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="2a664-575">使用 [*交易處理*](t-gly.md)來安裝多個封裝。</span><span class="sxs-lookup"><span data-stu-id="2a664-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="2a664-576">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-577">多套件安裝</span><span class="sxs-lookup"><span data-stu-id="2a664-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="2a664-578">在 Windows Installer 套件中內嵌自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="2a664-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="2a664-579">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-580">使用使用者介面</span><span class="sxs-lookup"><span data-stu-id="2a664-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="2a664-581">使用內嵌 UI</span><span class="sxs-lookup"><span data-stu-id="2a664-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="2a664-582">基礎結構開發人員</span><span class="sxs-lookup"><span data-stu-id="2a664-582">Infrastructure Developers</span></span>

<span data-ttu-id="2a664-583">基礎結構開發人員可以建立統一的平臺，以部署和管理使用 Windows Installer 服務的軟體。</span><span class="sxs-lookup"><span data-stu-id="2a664-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="2a664-584">他們可以使用 Windows Installer 程式設計介面來查詢、管理及散發系統上的應用程式、修補程式和來源。</span><span class="sxs-lookup"><span data-stu-id="2a664-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="2a664-585">找出、清查和查詢元件的狀態、資訊和用戶端。</span><span class="sxs-lookup"><span data-stu-id="2a664-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="2a664-586">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-587">元件特定函式</span><span class="sxs-lookup"><span data-stu-id="2a664-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-588">系統狀態函數</span><span class="sxs-lookup"><span data-stu-id="2a664-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-589">安裝程式物件</span><span class="sxs-lookup"><span data-stu-id="2a664-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="2a664-590">Product 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2a664-591">Patch 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2a664-592">清查和查詢資訊以及產品和功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a664-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="2a664-593">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-594">清查產品和修補程式</span><span class="sxs-lookup"><span data-stu-id="2a664-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="2a664-595">系統狀態函數</span><span class="sxs-lookup"><span data-stu-id="2a664-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-596">產品查詢函數</span><span class="sxs-lookup"><span data-stu-id="2a664-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-597">安裝程式物件</span><span class="sxs-lookup"><span data-stu-id="2a664-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="2a664-598">Product 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2a664-599">Patch 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2a664-600">使用 Windows Installer 清查、查詢和修改應用程式、升級和修補程式的來源清單，以改善來源復原。</span><span class="sxs-lookup"><span data-stu-id="2a664-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="2a664-601">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-602">**SOURCELIST 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="2a664-603">**來源復原**</span><span class="sxs-lookup"><span data-stu-id="2a664-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="2a664-604">安裝和設定功能</span><span class="sxs-lookup"><span data-stu-id="2a664-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-605">安裝程式物件</span><span class="sxs-lookup"><span data-stu-id="2a664-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="2a664-606">Product 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2a664-607">Patch 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2a664-608">使用 Windows Installer 清查、查詢和修改媒體來源，改善來源復原。</span><span class="sxs-lookup"><span data-stu-id="2a664-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="2a664-609">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-610">**SOURCELIST 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="2a664-611">來源復原</span><span class="sxs-lookup"><span data-stu-id="2a664-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="2a664-612">安裝和設定功能</span><span class="sxs-lookup"><span data-stu-id="2a664-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-613">Product 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="2a664-614">Patch 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2a664-615">清查和查詢資訊和修補程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a664-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="2a664-616">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-617">清查產品和修補程式</span><span class="sxs-lookup"><span data-stu-id="2a664-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="2a664-618">安裝程式函數參考</span><span class="sxs-lookup"><span data-stu-id="2a664-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="2a664-619">Patch 物件</span><span class="sxs-lookup"><span data-stu-id="2a664-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="2a664-620">使用原則來管理存取權和許可權。</span><span class="sxs-lookup"><span data-stu-id="2a664-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="2a664-621">如需詳細資訊，請參閱下列：</span><span class="sxs-lookup"><span data-stu-id="2a664-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="2a664-622">電腦原則</span><span class="sxs-lookup"><span data-stu-id="2a664-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="2a664-623">使用者原則</span><span class="sxs-lookup"><span data-stu-id="2a664-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="2a664-624">以較高的許可權安裝非系統管理員的封裝</span><span class="sxs-lookup"><span data-stu-id="2a664-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="2a664-625">廣告以較高的許可權安裝的 Per-User 應用程式</span><span class="sxs-lookup"><span data-stu-id="2a664-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="2a664-626">使用自訂動作在本機電腦上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="2a664-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="2a664-627">**AdminUser 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="2a664-628">**具有特殊許可權的屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="2a664-629">**EnableUserControl 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="2a664-630">**UserSID 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="2a664-631">**SecureCustomProperties 屬性**</span><span class="sxs-lookup"><span data-stu-id="2a664-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



