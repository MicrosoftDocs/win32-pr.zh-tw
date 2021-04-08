---
description: 本主題中的資訊會識別 Windows Installer&160; 5.0 中提供的新增和變更 \# 。
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Windows Installer 5.0 的新功能
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: ae7986cec60341127ab00ad08a3032aad80209bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847677"
---
# <a name="whats-new-in-windows-installer-50"></a><span data-ttu-id="7e0cc-103">Windows Installer 5.0 的新功能</span><span class="sxs-lookup"><span data-stu-id="7e0cc-103">What's New in Windows Installer 5.0</span></span>

<span data-ttu-id="7e0cc-104">本主題中的資訊會識別 Windows Installer 5.0 中可用的新增和變更。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-104">The information in this topic identifies the additions and changes that are available in Windows Installer 5.0.</span></span>

<span data-ttu-id="7e0cc-105">Windows Installer 5.0 隨附于下列版本的 Windows：</span><span class="sxs-lookup"><span data-stu-id="7e0cc-105">Windows Installer 5.0 is included with the following versions of Windows:</span></span>

* <span data-ttu-id="7e0cc-106">用戶端： Windows 7 和所有更新版本。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-106">Client: Windows 7 and all later versions.</span></span>
* <span data-ttu-id="7e0cc-107">伺服器： Windows Server 2008 R2 和所有更新版本。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-107">Server: Windows Server 2008 R2 and all later versions.</span></span>

> [!NOTE]
> <span data-ttu-id="7e0cc-108">Windows Installer 5.0 沒有可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-108">There is no redistributable for Windows Installer 5.0.</span></span> <span data-ttu-id="7e0cc-109">如需舊版 Windows Installer 可用可轉散發套件的清單，請參閱 [Windows Installer](windows-installer-redistributables.md)可轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-109">For a list of redistributables available for previous versions of Windows Installer, see [Windows Installer Redistributables](windows-installer-redistributables.md).</span></span> <span data-ttu-id="7e0cc-110">如需 Windows Installer 版本的完整清單，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-110">For a complete list of Windows Installer versions, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="7e0cc-111">本頁面是以檔的指南的形式提供。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-111">This page is provided as a guide to the documentation.</span></span> <span data-ttu-id="7e0cc-112">您應參閱主要參考頁面上的需求一節，以判斷實際的作業系統需求。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-112">You should refer to the Requirements section on the main reference pages to determine the actual operating system requirements.</span></span> <span data-ttu-id="7e0cc-113">從這個頁面未連結的部分 Windows Installer，可能會在另一個版本的 Windows Installer 中提供。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-113">Parts of the Windows Installer that are not linked to from this page may be available in another version of the Windows Installer.</span></span> <span data-ttu-id="7e0cc-114">如需其他 Windows Installer 版本的詳細資訊，請參閱 [Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-114">For information about other Windows Installer versions, see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

[<span data-ttu-id="7e0cc-115">標準動作</span><span class="sxs-lookup"><span data-stu-id="7e0cc-115">Standard Actions</span></span>](standard-actions.md)

-   [<span data-ttu-id="7e0cc-116">MsiConfigureServices</span><span class="sxs-lookup"><span data-stu-id="7e0cc-116">MsiConfigureServices</span></span>](msiconfigureservices-action.md)

[<span data-ttu-id="7e0cc-117">安裝程式函數</span><span class="sxs-lookup"><span data-stu-id="7e0cc-117">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="7e0cc-118">**MsiEnumComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-118">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [<span data-ttu-id="7e0cc-119">**MsiEnumClientsEx**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-119">**MsiEnumClientsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [<span data-ttu-id="7e0cc-120">**MsiGetComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-120">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[<span data-ttu-id="7e0cc-121">資料行資料類型</span><span class="sxs-lookup"><span data-stu-id="7e0cc-121">Column Data Types</span></span>](column-data-types.md)

-   [<span data-ttu-id="7e0cc-122">**FormattedSDDLText**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-122">**FormattedSDDLText**</span></span>](formattedsddltext.md)

[<span data-ttu-id="7e0cc-123">屬性</span><span class="sxs-lookup"><span data-stu-id="7e0cc-123">Properties</span></span>](properties.md)

-   [<span data-ttu-id="7e0cc-124">**MSIFASTINSTALL**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-124">**MSIFASTINSTALL**</span></span>](msifastinstall.md)
-   [<span data-ttu-id="7e0cc-125">**MSIINSTALLPERUSER**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-125">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)

[<span data-ttu-id="7e0cc-126">摘要資訊屬性</span><span class="sxs-lookup"><span data-stu-id="7e0cc-126">Summary Information Properties</span></span>](summary-information-stream-reference.md)

-   <span data-ttu-id="7e0cc-127">[**範本摘要**](template-summary.md)有新的值，指出資料庫與 Windows RT 或 Arm64 平臺相容。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-127">The [**Template Summary**](template-summary.md) has new values to indicate the database is compatible with Windows RT or the Arm64 platform.</span></span>

[<span data-ttu-id="7e0cc-128">資料庫資料表</span><span class="sxs-lookup"><span data-stu-id="7e0cc-128">Database Tables</span></span>](database-tables.md)

-   [<span data-ttu-id="7e0cc-129">MsiServiceConfig 資料表</span><span class="sxs-lookup"><span data-stu-id="7e0cc-129">MsiServiceConfig Table</span></span>](msiserviceconfig-table.md)
-   [<span data-ttu-id="7e0cc-130">MsiServiceConfigFailureActions 資料表</span><span class="sxs-lookup"><span data-stu-id="7e0cc-130">MsiServiceConfigFailureActions Table</span></span>](msiserviceconfigfailureactions-table.md)
-   [<span data-ttu-id="7e0cc-131">MsiShortcutProperty 資料表</span><span class="sxs-lookup"><span data-stu-id="7e0cc-131">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
-   [<span data-ttu-id="7e0cc-132">MsiLockPermissionsEx 資料表</span><span class="sxs-lookup"><span data-stu-id="7e0cc-132">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)

[<span data-ttu-id="7e0cc-133">事件</span><span class="sxs-lookup"><span data-stu-id="7e0cc-133">ControlEvents</span></span>](control-events.md)

-   [<span data-ttu-id="7e0cc-134">MsiPrint ControlEvent</span><span class="sxs-lookup"><span data-stu-id="7e0cc-134">MsiPrint ControlEvent</span></span>](msiprint-controlevent.md)
-   [<span data-ttu-id="7e0cc-135">MsiLaunchApp ControlEvent</span><span class="sxs-lookup"><span data-stu-id="7e0cc-135">MsiLaunchApp ControlEvent</span></span>](msilaunchapp-controlevent.md)

[<span data-ttu-id="7e0cc-136">控制項</span><span class="sxs-lookup"><span data-stu-id="7e0cc-136">Controls</span></span>](controls.md)

-   [<span data-ttu-id="7e0cc-137">超連結控制項</span><span class="sxs-lookup"><span data-stu-id="7e0cc-137">Hyperlink Control</span></span>](hyperlink-control.md)

[<span data-ttu-id="7e0cc-138">內部一致性評估工具-Ices-003</span><span class="sxs-lookup"><span data-stu-id="7e0cc-138">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="7e0cc-139">ICE101</span><span class="sxs-lookup"><span data-stu-id="7e0cc-139">ICE101</span></span>](ice-101.md)
-   [<span data-ttu-id="7e0cc-140">ICE102</span><span class="sxs-lookup"><span data-stu-id="7e0cc-140">ICE102</span></span>](ice-102.md)
-   [<span data-ttu-id="7e0cc-141">ICE103</span><span class="sxs-lookup"><span data-stu-id="7e0cc-141">ICE103</span></span>](ice-103.md)
-   [<span data-ttu-id="7e0cc-142">ICE104</span><span class="sxs-lookup"><span data-stu-id="7e0cc-142">ICE104</span></span>](ice-104.md)
-   [<span data-ttu-id="7e0cc-143">ICE105</span><span class="sxs-lookup"><span data-stu-id="7e0cc-143">ICE105</span></span>](ice-105.md)

[<span data-ttu-id="7e0cc-144">Automation 介面</span><span class="sxs-lookup"><span data-stu-id="7e0cc-144">Automation Interface</span></span>](automation-interface.md)

-   <span data-ttu-id="7e0cc-145">[**安裝程式物件** 的屬性](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="7e0cc-145">Properties of the [**Installer Object**](installer-object.md)</span></span>

    -   [<span data-ttu-id="7e0cc-146">**ClientsEx**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-146">**Installer.ClientsEx**</span></span>](installer-clientsex.md)
    -   [<span data-ttu-id="7e0cc-147">**ComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-147">**Installer.ComponentsEx**</span></span>](installer-componentsex.md)
    -   [<span data-ttu-id="7e0cc-148">**ComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-148">**Installer.ComponentPathEx**</span></span>](installer-componentpathex.md)

-   <span data-ttu-id="7e0cc-149">[**元件物件** 的屬性](components.md)</span><span class="sxs-lookup"><span data-stu-id="7e0cc-149">Properties of the [**Components Object**](components.md)</span></span>

    -   [<span data-ttu-id="7e0cc-150">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-150">**Components.ComponentCode**</span></span>](component-componentcode.md)
    -   [<span data-ttu-id="7e0cc-151">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-151">**Components.UserSID**</span></span>](component-usersid.md)
    -   [<span data-ttu-id="7e0cc-152">**元件。內容**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-152">**Components.Context**</span></span>](component-context.md)

-   <span data-ttu-id="7e0cc-153">[**用戶端物件** 的屬性](client.md)</span><span class="sxs-lookup"><span data-stu-id="7e0cc-153">Properties of the [**Client Object**](client.md)</span></span>

    -   [<span data-ttu-id="7e0cc-154">**用戶端. ProductCode**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-154">**Client.ProductCode**</span></span>](client-productcode.md)
    -   [<span data-ttu-id="7e0cc-155">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-155">**Client.ComponentCode**</span></span>](client-componentcode.md)
    -   [<span data-ttu-id="7e0cc-156">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-156">**Client.UserSID**</span></span>](client-usersid.md)
    -   [<span data-ttu-id="7e0cc-157">**用戶端。內容**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-157">**Client.Context**</span></span>](client-context.md)

-   <span data-ttu-id="7e0cc-158">[**ComponentInfo**](componentinfo.md)物件的屬性</span><span class="sxs-lookup"><span data-stu-id="7e0cc-158">Properties of the [**ComponentInfo**](componentinfo.md) Object</span></span>

    -   [<span data-ttu-id="7e0cc-159">**ComponentInfo.ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-159">**ComponentInfo.ComponentCode**</span></span>](componentinfo-componentcode.md)
    -   [<span data-ttu-id="7e0cc-160">**ComponentInfo 路徑**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-160">**ComponentInfo.Path**</span></span>](componentinfo-path.md)
    -   [<span data-ttu-id="7e0cc-161">**ComponentInfo。州**</span><span class="sxs-lookup"><span data-stu-id="7e0cc-161">**ComponentInfo.State**</span></span>](componentinfo-state.md)

## <a name="notes"></a><span data-ttu-id="7e0cc-162">備註</span><span class="sxs-lookup"><span data-stu-id="7e0cc-162">Notes</span></span>

<span data-ttu-id="7e0cc-163">安裝程式開發人員可以使用 Windows Installer 5.0 來撰寫單一安裝套件，以支援每一電腦安裝或應用程式的每個使用者安裝。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-163">Setup developers can use Windows Installer 5.0 to author a single installation package capable of either per-machine installation or per-user installation of the application.</span></span> <span data-ttu-id="7e0cc-164">如需詳細資訊，請參閱 [單一封裝撰寫](single-package-authoring.md)。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-164">For more information, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="7e0cc-165">內部一致性評估工具 [ICE105](ice-105.md) 會檢查封裝是否已撰寫成要安裝在每個使用者的內容中。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-165">The internal consistency evaluator [ICE105](ice-105.md) checks that the package has been authored to be installed in a per-user context.</span></span> <span data-ttu-id="7e0cc-166">不具特權的標準使用者可以安裝、更新、執行和移除的應用程式，也稱為 Per-User 應用程式 (PUA。 ) PUA 可以提供較佳的使用者體驗、將系統和其他電腦使用者的影響降到最低，以及將 UAC 提示保留在實際需要提高使用者權限的情況下。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-166">An application capable of being installed, updated, run, and removed by a standard user without elevation is called a Per-User Application (PUA.) A PUA can provide a better user experience, minimize effects on the system and other users of the computer, and reserves UAC prompting to situations that actually require the elevation of the user's privileges.</span></span> <span data-ttu-id="7e0cc-167">Windows Installer 5.0 的單一套件撰寫功能可協助開發 Per-User 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-167">The Single Package Authoring features of Windows Installer 5.0 can facilitate the development of Per-User Applications.</span></span>

<span data-ttu-id="7e0cc-168">服務設定選項可讓 Windows Installer 套件自訂電腦上的 [服務](../services/services.md) 。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-168">Services configuration options enable a Windows Installer package to customize the [services](../services/services.md) on a computer.</span></span> <span data-ttu-id="7e0cc-169">如需詳細資訊，請參閱 [使用服務](using-services-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-169">For more information, see [Using Services Configuration](using-services-configuration.md).</span></span>

<span data-ttu-id="7e0cc-170">從 Windows Installer 5.0 開始，Windows Installer 套件能夠保護新的帳戶、Windows [服務](../services/services.md)、檔案、資料夾和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-170">Beginning with Windows Installer 5.0, a Windows Installer package is capable to secure new accounts, Windows [services](../services/services.md), files, folders, and registry keys.</span></span> <span data-ttu-id="7e0cc-171">[MsiLockPermissionsEx](msilockpermissionsex-table.md)資料表可以指定拒絕許可權的安全描述項、指定父資源的許可權繼承，或指定新帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-171">The [MsiLockPermissionsEx](msilockpermissionsex-table.md) table can specify a security descriptor that denies permissions, specifies inheritance of permissions from a parent resource, or specifies the permissions of a new account.</span></span> <span data-ttu-id="7e0cc-172">如需詳細資訊，請參閱 [保護資源](securing-resources-.md)。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-172">For information, see [Securing Resources](securing-resources-.md).</span></span>

<span data-ttu-id="7e0cc-173">Windows Installer 5.0 可以列舉電腦上安裝的所有元件，並取得元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-173">Windows Installer 5.0 can enumerate all components installed on the computer and obtain the key path for the component.</span></span> <span data-ttu-id="7e0cc-174">如需詳細資訊，請參閱 [列舉元件](enumerating-components-.md)。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-174">For more information, see [Enumerating Components](enumerating-components-.md).</span></span>

<span data-ttu-id="7e0cc-175">在 Windows Server 2012 或 Windows 8 上執行的 Windows Installer 5.0 支援在 Windows RT 上安裝已核准的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-175">Windows Installer 5.0 running on Windows Server 2012 or Windows 8 supports the installation of approved apps on Windows RT.</span></span> <span data-ttu-id="7e0cc-176">未由 Microsoft 簽署的 Windows Installer 套件、修補程式或轉換，無法安裝在 Windows RT 上。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-176">A Windows Installer package, patch, or transform that has not been signed by Microsoft cannot be installed on Windows RT.</span></span> <span data-ttu-id="7e0cc-177">[ [**範本摘要**](template-summary.md) ] 屬性會指出與安裝資料庫相容的平臺，而且應該包含 Windows RT 的值。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-177">The [**Template Summary**](template-summary.md) property indicates the platform that is compatible with the installation database and should include the value for Windows RT.</span></span>

<span data-ttu-id="7e0cc-178">在 Arm64 處理器上的 Windows 10 上執行的 Windows Installer 5.0 支援安裝專門針對 Arm64 平臺編譯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-178">Windows Installer 5.0 running on Windows 10 on Arm64 processors supports the installation of applications compiled specifically for the Arm64 platform.</span></span>  <span data-ttu-id="7e0cc-179">這些套件的 [ [**範本摘要**](template-summary.md) ] 屬性必須包含值 Arm64。</span><span class="sxs-lookup"><span data-stu-id="7e0cc-179">The [**Template Summary**](template-summary.md) property of these packages needs to include the value Arm64.</span></span> 

 
