---
description: 本主題提供獨立軟體廠商 (Isv) 提供在 Windows Vista 和更新版本中註冊及管理應用程式預設值所需步驟的快速指南。 提供有關每個章節主題的更深入文章的連結。
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: 管理預設應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40d6c80aae4005fc015c08ef7bf2907289e795
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849179"
---
# <a name="managing-default-applications"></a><span data-ttu-id="62f67-104">管理預設應用程式</span><span class="sxs-lookup"><span data-stu-id="62f67-104">Managing Default Applications</span></span>

<span data-ttu-id="62f67-105">[ **設定程式存取和電腦預設值** ] (SPAD) 功能已新增至 windows XP 和更新版本的 windows，以管理每部電腦的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-105">The **Set Program Access and Computer Defaults** (SPAD) feature was added to Windows XP and later versions of Windows to manage per-computer defaults.</span></span> <span data-ttu-id="62f67-106">除了 SPAD 之外，Windows Vista 還引進了每個使用者預設應用程式的概念，以及主控台中的 **預設程式** 專案。</span><span class="sxs-lookup"><span data-stu-id="62f67-106">In addition to SPAD, Windows Vista introduced the concept of per-user default applications and the **Default Programs** item in Control Panel.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62f67-107">本主題不適用於 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="62f67-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="62f67-108">預設檔案關聯在 Windows 10 中的運作方式有所變更。</span><span class="sxs-lookup"><span data-stu-id="62f67-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="62f67-109">如需詳細資訊，請參閱 [這篇文章](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/)中有關 **Windows 10 如何處理預設應用程式的變更** 一節。</span><span class="sxs-lookup"><span data-stu-id="62f67-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="62f67-110">每個使用者的預設設定是系統上個別使用者帳戶的特定設定。</span><span class="sxs-lookup"><span data-stu-id="62f67-110">Per-user default settings are specific to an individual user account on the system.</span></span> <span data-ttu-id="62f67-111">如果有個別使用者的預設設定，則會優先于該帳戶的相對應個別電腦預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-111">If per-user default settings are present, they take precedence over corresponding per-computer defaults for that account.</span></span> <span data-ttu-id="62f67-112">從 Windows 8 中，檔案類型和通訊協定預設值的擴充性系統會嚴格地依使用者和每一電腦的預設值加以忽略。</span><span class="sxs-lookup"><span data-stu-id="62f67-112">As of Windows 8, the extensibility system for file type and protocol defaults is strictly per-user and per-computer defaults are ignored.</span></span> <span data-ttu-id="62f67-113">SPAD 也會在 Windows 8 中變更，以設定每個使用者的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-113">SPAD also changed in Windows 8 to set per-user defaults.</span></span>

-   <span data-ttu-id="62f67-114">在執行早于 Windows 8 的 Windows 版本的系統上，新建立的使用者帳戶會收到每一電腦預設值，直到建立每個使用者的預設值為止。</span><span class="sxs-lookup"><span data-stu-id="62f67-114">On systems running versions of Windows earlier than Windows 8, a newly created user account receives per-computer defaults until per-user defaults are established.</span></span> <span data-ttu-id="62f67-115">在 Windows Vista 和更新版本中，使用者可以使用主控台中的 [ **預設程式** ] 專案來設定或變更其每個使用者預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-115">In Windows Vista and later, users can use the **Default Programs** item in Control Panel to set or change their per-user defaults.</span></span> <span data-ttu-id="62f67-116">此外，當應用程式第一次執行時，可以使用 [ [應用程式首次執行] 和 [預設值](#application-first-run-and-defaults) ] 區段中遵循的指導方針來設定每個使用者的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-116">In addition, when an application is run for the first time, per-user defaults can be set using the guidelines that follow in the [Application First Run and Defaults](#application-first-run-and-defaults) section.</span></span>
-   <span data-ttu-id="62f67-117">在執行 Windows 8 的系統上，新建立的使用者帳戶會依賴每位使用者的預設值，並在第一次執行時使用這些預設值，如 [應用程式第一次執行和預設值](#application-first-run-and-defaults) 一節中所述，不再支援。</span><span class="sxs-lookup"><span data-stu-id="62f67-117">On systems running Windows 8, a newly created user account relies on per-user defaults from the start and the setting of those defaults on first run as explained in the [Application First Run and Defaults](#application-first-run-and-defaults) section is no longer supported.</span></span>

<span data-ttu-id="62f67-118">應用程式必須同時註冊 SPAD 和預設程式功能，才能在 Windows Vista 和更新版本中提供作為預設程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-118">An application must register with both SPAD and the Default Programs feature to be offered as the default program in Windows Vista and later.</span></span>

<span data-ttu-id="62f67-119">本主題提供獨立軟體廠商 (Isv) 提供在 Windows Vista 和更新版本中註冊及管理應用程式預設值所需步驟的快速指南。</span><span class="sxs-lookup"><span data-stu-id="62f67-119">This topic provides independent software vendors (ISVs) with a quick guide to the steps necessary to register and manage application defaults in Windows Vista and later.</span></span> <span data-ttu-id="62f67-120">提供有關每個章節主題的更深入文章的連結。</span><span class="sxs-lookup"><span data-stu-id="62f67-120">Links are provided to more in-depth articles about each section's topic.</span></span>

-   [<span data-ttu-id="62f67-121">主控台中的預設程式專案</span><span class="sxs-lookup"><span data-stu-id="62f67-121">Default Programs Item in Control Panel</span></span>](#default-programs-item-in-control-panel)
-   [<span data-ttu-id="62f67-122">設定程式存取和電腦預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-122">Set Program Access and Computer Defaults</span></span>](#set-program-access-and-computer-defaults)
    -   [<span data-ttu-id="62f67-123">在 SPAD 中設定預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-123">Setting Defaults in SPAD</span></span>](#setting-defaults-in-spad)
    -   [<span data-ttu-id="62f67-124">隱藏 SPAD 中的存取權</span><span class="sxs-lookup"><span data-stu-id="62f67-124">Hide Access in SPAD</span></span>](#hide-access-in-spad)
-   [<span data-ttu-id="62f67-125">註冊應用程式進入點</span><span class="sxs-lookup"><span data-stu-id="62f67-125">Registering for Application Entry Points</span></span>](#registering-for-application-entry-points)
    -   [<span data-ttu-id="62f67-126">開啟方式</span><span class="sxs-lookup"><span data-stu-id="62f67-126">Open With</span></span>](#open-with)
    -   <span data-ttu-id="62f67-127">[[開始] 功能表和快速啟動 Bar](#start-menu-and-quick-launch-bar)</span><span class="sxs-lookup"><span data-stu-id="62f67-127">[Start Menu and Quick Launch Bar](#start-menu-and-quick-launch-bar)</span></span>
-   [<span data-ttu-id="62f67-128">應用程式安裝和預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-128">Application Installation and Defaults</span></span>](#application-installation-and-defaults)
-   [<span data-ttu-id="62f67-129">應用程式升級和預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-129">Application Upgrades and Defaults</span></span>](#application-upgrades-and-defaults)
-   [<span data-ttu-id="62f67-130">應用程式第一次執行和預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-130">Application First Run and Defaults</span></span>](#application-first-run-and-defaults)
-   [<span data-ttu-id="62f67-131">驗證預設值並要求使用者同意</span><span class="sxs-lookup"><span data-stu-id="62f67-131">Verifying Defaults and Asking for User Consent</span></span>](#verifying-defaults-and-asking-for-user-consent)
-   [<span data-ttu-id="62f67-132">應用程式相容性秘訣</span><span class="sxs-lookup"><span data-stu-id="62f67-132">Application Compatibility Tips</span></span>](#application-compatibility-tips)
    -   [<span data-ttu-id="62f67-133">避免觸發 Per-User 虛擬化</span><span class="sxs-lookup"><span data-stu-id="62f67-133">Avoid Triggering Per-User Virtualization</span></span>](#avoid-triggering-per-user-virtualization)
    -   [<span data-ttu-id="62f67-134">避免從程式相容性助理 AppCompat 警告或區塊</span><span class="sxs-lookup"><span data-stu-id="62f67-134">Avoid AppCompat Warnings or Blocks from the Program Compatibility Assistant</span></span>](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [<span data-ttu-id="62f67-135">舊版 Windows 作業系統的支援</span><span class="sxs-lookup"><span data-stu-id="62f67-135">Support for Previous Windows Operating System Versions</span></span>](#support-for-previous-windows-operating-system-versions)
-   [<span data-ttu-id="62f67-136">其他資源</span><span class="sxs-lookup"><span data-stu-id="62f67-136">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="62f67-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="62f67-137">Related topics</span></span>](#related-topics)

## <a name="default-programs-item-in-control-panel"></a><span data-ttu-id="62f67-138">主控台中的預設程式專案</span><span class="sxs-lookup"><span data-stu-id="62f67-138">Default Programs Item in Control Panel</span></span>

<span data-ttu-id="62f67-139">**預設程式** 是 Windows Vista 中引進的功能，可直接從 [ **開始** ] 功能表和主控台存取。</span><span class="sxs-lookup"><span data-stu-id="62f67-139">**Default Programs** is a feature introduced in Windows Vista, accessible directly from the **Start** menu as well as Control Panel.</span></span> <span data-ttu-id="62f67-140">它提供的新基礎結構可搭配標準使用者權限使用 () 不會提高許可權，而且是設計來讓使用者和應用程式管理每個使用者的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-140">It provides a new infrastructure that works with standard user privilege (not elevated) and is designed to enable users and applications to manage per-user defaults.</span></span> <span data-ttu-id="62f67-141">針對使用者，預設程式提供統一且容易存取的方式，來管理系統上所有應用程式的預設值、檔案關聯和自動播放設定。</span><span class="sxs-lookup"><span data-stu-id="62f67-141">For users, Default Programs provides a unified and easily accessible way to manage defaults, file associations, and Autoplay settings across all applications on the system.</span></span> <span data-ttu-id="62f67-142">針對應用程式，使用預設程式 Api 所提供的每個使用者範圍提供下列優點：</span><span class="sxs-lookup"><span data-stu-id="62f67-142">For applications, using the per-user scope provided by the Default Programs APIs offers the following advantages:</span></span>

-   <span data-ttu-id="62f67-143">**無提高許可權**</span><span class="sxs-lookup"><span data-stu-id="62f67-143">**No Elevation**</span></span>

    <span data-ttu-id="62f67-144">應用程式不需要將其許可權提升為宣告預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-144">An application does not have to elevate its privileges to claim defaults.</span></span>

-   <span data-ttu-id="62f67-145">**良好公民資格**</span><span class="sxs-lookup"><span data-stu-id="62f67-145">**Good Citizenship**</span></span>

    <span data-ttu-id="62f67-146">在多使用者電腦上，每個使用者都可以選取不同的預設應用程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-146">On a multiple-user computer, each user can select different default applications.</span></span>

-   <span data-ttu-id="62f67-147">**預設管理**</span><span class="sxs-lookup"><span data-stu-id="62f67-147">**Default Management**</span></span>

    <span data-ttu-id="62f67-148">預設程式 Api 提供可靠且一致的機制，可自行檢查預設狀態並回收遺失的設定，而不需要直接寫入登錄。</span><span class="sxs-lookup"><span data-stu-id="62f67-148">Default Programs APIs offer a reliable and consistent mechanism for self-checking the default status and reclaiming lost settings without resorting to writing directly to the registry.</span></span> <span data-ttu-id="62f67-149">不過，從 Windows 8，我們不建議應用程式查詢預設狀態，因為應用程式無法再變更預設設定，這些變更只能由使用者進行。</span><span class="sxs-lookup"><span data-stu-id="62f67-149">However, as of Windows 8, we do not recommended that applications query the default status because an application can no longer change the default settings—those changes can be made only by the user.</span></span>

<span data-ttu-id="62f67-150">若要讓您的應用程式有效率地管理預設值，您必須將應用程式註冊為可能的預設程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-150">To enable your application to manage defaults effectively, you must register your application as a potential default program.</span></span> <span data-ttu-id="62f67-151">如需註冊和使用預設程式 Api 的詳細資訊，請參閱 [預設程式](default-programs.md)。</span><span class="sxs-lookup"><span data-stu-id="62f67-151">For details on registering and using the Default Programs APIs, see [Default Programs](default-programs.md).</span></span>

<span data-ttu-id="62f67-152">預設程式也提供這兩種功能：</span><span class="sxs-lookup"><span data-stu-id="62f67-152">Default Programs also provides these two features:</span></span>

-   <span data-ttu-id="62f67-153">**可重複使用的預設 UI**</span><span class="sxs-lookup"><span data-stu-id="62f67-153">**Reusable Defaults UI**</span></span>

    <span data-ttu-id="62f67-154">程式預設值的 UI (**將預設程式設定**) 和檔案關聯 (將 **檔案類型或通訊協定與程式建立關聯**) 可以從應用程式內重複使用和呼叫。</span><span class="sxs-lookup"><span data-stu-id="62f67-154">The UI of both the program defaults (**Set your default programs**) and file associations (**Associate a file type or protocol with a program**) can be reused and called from within an application.</span></span> <span data-ttu-id="62f67-155">這可讓應用程式提供標準使用者體驗來管理預設值，並讓 Isv 不必開發自訂或對等的 UI。</span><span class="sxs-lookup"><span data-stu-id="62f67-155">This enables applications to provide a standard user experience for managing defaults and saves ISVs from having to develop a custom or equivalent UI.</span></span>

-   <span data-ttu-id="62f67-156">**包含 URL 和行銷資訊**</span><span class="sxs-lookup"><span data-stu-id="62f67-156">**Inclusion of URL and Marketing Information**</span></span>

    <span data-ttu-id="62f67-157">在主控台的 [**預設程式**] 專案的 [**設定預設程式**] 頁面中，應用程式可以提供行銷資訊和廠商網站的連結。</span><span class="sxs-lookup"><span data-stu-id="62f67-157">As part of the **Set your default programs** page of the **Default Programs** item in Control Panel, an application can provide marketing information and a link to the vendor's website.</span></span> <span data-ttu-id="62f67-158">此 URL 是從應用程式已簽署的 Authenticode 憑證所衍生。</span><span class="sxs-lookup"><span data-stu-id="62f67-158">This URL is derived from the Authenticode certificate that the application has been signed with.</span></span> <span data-ttu-id="62f67-159">這可防止誤用及未經授權地取代此連結。</span><span class="sxs-lookup"><span data-stu-id="62f67-159">This prevents misuse and unauthorized replacement of this link.</span></span> <span data-ttu-id="62f67-160">如果應用程式具有包含內嵌 URL 的 Authenticode 憑證，Windows UI 會顯示該內嵌 URL。</span><span class="sxs-lookup"><span data-stu-id="62f67-160">If an application has an Authenticode certificate that includes an embedded URL, Windows UI displays that embedded URL.</span></span> <span data-ttu-id="62f67-161">Isv 應該利用這項功能，將使用者導向其網站，以進行更新和其他下載。</span><span class="sxs-lookup"><span data-stu-id="62f67-161">ISVs should take advantage of this feature to direct users to their website for updates and other downloads.</span></span>

## <a name="set-program-access-and-computer-defaults"></a><span data-ttu-id="62f67-162">設定程式存取和電腦預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-162">Set Program Access and Computer Defaults</span></span>

<span data-ttu-id="62f67-163">**設定程式存取和電腦預設值** (SPAD) 可讓系統管理員管理整個電腦的所有新使用者所繼承的全電腦預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-163">**Set Program Access and Computer Defaults** (SPAD) enables administrators to manage computer-wide defaults that are inherited by all new users of that computer.</span></span> <span data-ttu-id="62f67-164">在 Windows 8 之前，SPAD 也可讓系統管理員在程式從系統移除時，修復檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="62f67-164">Prior to Windows 8, SPAD also enabled administrators to repair file associations should they become broken when programs were removed from the system.</span></span> <span data-ttu-id="62f67-165">不過，從 Windows 8 起，SPAD 只會影響使用者特定的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-165">However, as of Windows 8, SPAD affects only user-specific defaults.</span></span>

<span data-ttu-id="62f67-166">如需在 SPAD 中註冊應用程式的詳細資訊，請參閱使用 [設定程式存取和電腦預設值 (SPAD) ](cpl-setprogramaccess.md) 和 [使用用戶端類型註冊程式](reg-middleware-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="62f67-166">For more information on registering an application in SPAD, see [Working with Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and [Registering Programs with Client Types](reg-middleware-apps.md).</span></span> <span data-ttu-id="62f67-167">後續各節將討論特定的變更和新的建議。</span><span class="sxs-lookup"><span data-stu-id="62f67-167">Specific changes and new recommendations are discussed in the sections that follow.</span></span>

### <a name="setting-defaults-in-spad"></a><span data-ttu-id="62f67-168">在 SPAD 中設定預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-168">Setting Defaults in SPAD</span></span>

<span data-ttu-id="62f67-169">每一使用者預設會覆寫每部電腦的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-169">Per-user defaults override per-computer defaults.</span></span>

-   <span data-ttu-id="62f67-170">在 **Windows 8 之前**： SPAD (中設定的預設值) ，如果設定對應的每個使用者預設值，使用者就不會看到這些預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-170">**Before Windows 8**: Defaults set in SPAD (which are per-computer) will not be seen by users if corresponding per-user defaults are set.</span></span> <span data-ttu-id="62f67-171">如果使用者未設定每位使用者的預設值，系統會使用對應的電腦預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-171">If a user has not set a per-user default, the system uses the corresponding computer default.</span></span> <span data-ttu-id="62f67-172">電腦上的新使用者帳戶一開始會繼承電腦預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-172">New user accounts on a computer initially inherit the computer defaults.</span></span> <span data-ttu-id="62f67-173">使用者第一次執行應用程式時，應用程式應該會提示使用者指派其每個使用者預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-173">The first time a user runs an application, the application should prompt the user to assign their per-user defaults.</span></span> <span data-ttu-id="62f67-174">請參閱 [應用程式首次執行和預設值](#application-first-run-and-defaults)。</span><span class="sxs-lookup"><span data-stu-id="62f67-174">See [Application First Run and Defaults](#application-first-run-and-defaults).</span></span>
-   <span data-ttu-id="62f67-175">從 **Windows 8**：所有預設值都是依使用者，且會忽略任何個別電腦的預設設定。</span><span class="sxs-lookup"><span data-stu-id="62f67-175">**As of Windows 8**: All defaults are per-user and any per-computer default setting is ignored.</span></span> <span data-ttu-id="62f67-176">應用程式無法再設定預設選項，因此他們無法透過指派這些預設值來引導使用者。</span><span class="sxs-lookup"><span data-stu-id="62f67-176">Applications can no longer set default choices, so they cannot walk the user through their assigning of those defaults.</span></span>

<span data-ttu-id="62f67-177">當預先 Windows 8 的應用程式在 SPAD 中 **設定為預設值** 時，應該遵循下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="62f67-177">When a pre-Windows 8 application implements **Set as Default** in SPAD, these guidelines should be followed:</span></span>

-   <span data-ttu-id="62f67-178">應用程式應該只透過 SPAD 宣告電腦層級的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-178">Applications should claim only computer-level defaults through SPAD.</span></span>
-   <span data-ttu-id="62f67-179">應用程式 *不* 應該透過 SPAD 宣告每位使用者的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-179">Applications should *not* claim per-user defaults through SPAD.</span></span>

<span data-ttu-id="62f67-180">當 Windows 8 應用程式在 SPAD 中 **設定為預設值** 時，必須使用 SPAD 中使用的相同應用程式名稱，在 [預設程式](default-programs.md)中註冊其檔案類型和通訊協定。</span><span class="sxs-lookup"><span data-stu-id="62f67-180">When a Windows 8 application implements **Set as Default** in SPAD, they must register their file types and protocols in [Default Programs](default-programs.md), using the same application name used in SPAD.</span></span> <span data-ttu-id="62f67-181">這可讓 SPAD 中的變更反映為目前使用者的對應預設程式專案中的變更。</span><span class="sxs-lookup"><span data-stu-id="62f67-181">This allows a change in SPAD to reflect as a change in the corresponding Default Programs entry for the current user.</span></span>

### <a name="hide-access-in-spad"></a><span data-ttu-id="62f67-182">隱藏 SPAD 中的存取權</span><span class="sxs-lookup"><span data-stu-id="62f67-182">Hide Access in SPAD</span></span>

<span data-ttu-id="62f67-183">您可以使用下列兩種方式之一來存取 SPAD 中每個可能預設值的隱藏存取選項：</span><span class="sxs-lookup"><span data-stu-id="62f67-183">The hide access option for each possible default in SPAD is accessed in one of two ways:</span></span>

-   <span data-ttu-id="62f67-184">選擇 **非 microsoft** 的預設預設類別，這會移除所有 Microsoft 預設值的存取權。</span><span class="sxs-lookup"><span data-stu-id="62f67-184">Choose the **Non-Microsoft** category of defaults, which removes access to all Microsoft defaults.</span></span>
-   <span data-ttu-id="62f67-185">選擇 [ **自訂** ] 類別，並清除 [ **啟用對這個程式的存取** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="62f67-185">Choose the **Custom** category and clear the **Enable access to this program** check box.</span></span>

<span data-ttu-id="62f67-186">先前，將其中一項動作移除至系統上適當應用程式的所有進入點。</span><span class="sxs-lookup"><span data-stu-id="62f67-186">Previously, taking either of those actions removed all entry points to the appropriate applications on the system.</span></span> <span data-ttu-id="62f67-187">這種情況的特定指導方針，就是要從下列位置移除快速鍵和圖示：</span><span class="sxs-lookup"><span data-stu-id="62f67-187">Specific guidelines for this situation say to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="62f67-188">桌面</span><span class="sxs-lookup"><span data-stu-id="62f67-188">Desktop</span></span>
-   <span data-ttu-id="62f67-189">開始功能表</span><span class="sxs-lookup"><span data-stu-id="62f67-189">Start menu</span></span>
-   <span data-ttu-id="62f67-190">快速啟動 bar (Windows Vista 及更早版本) </span><span class="sxs-lookup"><span data-stu-id="62f67-190">Quick Launch bar (Windows Vista and earlier only)</span></span>
-   <span data-ttu-id="62f67-191">[通知] 區域</span><span class="sxs-lookup"><span data-stu-id="62f67-191">Notification area</span></span>
-   <span data-ttu-id="62f67-192">快顯功能表</span><span class="sxs-lookup"><span data-stu-id="62f67-192">Shortcut menus</span></span>
-   <span data-ttu-id="62f67-193">資料夾工作區</span><span class="sxs-lookup"><span data-stu-id="62f67-193">Folder task band</span></span>

<span data-ttu-id="62f67-194">建議廠商在應用程式的隱藏存取回呼函式中實施這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="62f67-194">Vendors are encouraged to implement these guidelines in the application's Hide Access callback function.</span></span>

### <a name="alternate-hide-access-method-in-spad"></a><span data-ttu-id="62f67-195">SPAD 中的替代隱藏存取方法</span><span class="sxs-lookup"><span data-stu-id="62f67-195">Alternate Hide Access Method in SPAD</span></span>

<span data-ttu-id="62f67-196">針對某些繼承應用程式，隱藏存取的完整執行可能不實用。</span><span class="sxs-lookup"><span data-stu-id="62f67-196">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="62f67-197">替代方法可達成相同的效果，但使用者不容易復原，而是將應用程式卸載。</span><span class="sxs-lookup"><span data-stu-id="62f67-197">An alternate method that achieves the same effect, but is not easily reversible by the user, is to uninstall the application.</span></span> <span data-ttu-id="62f67-198">以下顯示範例行為和執行此程式碼的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="62f67-198">The following shows sample behavior and example code to implement this.</span></span>

<span data-ttu-id="62f67-199">此替代方案的建議使用者體驗如下所示：</span><span class="sxs-lookup"><span data-stu-id="62f67-199">The recommended user experience for this alternative is as follows:</span></span>

-   <span data-ttu-id="62f67-200">當使用者清除 SPAD 中的 [ **啟用對這個程式的存取** ] 方塊時，會顯示下列的 UI。</span><span class="sxs-lookup"><span data-stu-id="62f67-200">When the user clears the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![關於隱藏程式存取權的 vista 對話方塊](images/hideaccessvista.png)

-   <span data-ttu-id="62f67-202">當使用者按一下 **[確定]** 時，會顯示主控台中的 [ **程式和功能** ] 專案，讓使用者可以卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-202">When the user clicks **OK**, the **Programs and Features** item in Control Panel is displayed so that the user can uninstall the application.</span></span>
-   <span data-ttu-id="62f67-203">Windows XP 使用者應該會看到下列對話方塊。</span><span class="sxs-lookup"><span data-stu-id="62f67-203">Windows XP users should be presented with the following dialog box.</span></span>

    ![關於隱藏程式存取權的 windows xp 對話方塊](images/hideaccessxp.png)

-   <span data-ttu-id="62f67-205">當 Windows XP 使用者按一下 **[確定]** 時，會顯示主控台中的 [ **新增或移除程式** ] 專案，讓使用者可以卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-205">When the Windows XP user clicks **OK**, the **Add or Remove Programs** item in Control Panel is displayed so that the user can uninstall the application.</span></span>

<span data-ttu-id="62f67-206">下列程式碼針對隱藏存取功能提供可重複使用的執行，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="62f67-206">The following code provides a reusable implementation for the Hide Access feature as outlined previously.</span></span> <span data-ttu-id="62f67-207">它可用於 Windows XP、Windows Vista 和 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="62f67-207">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



## <a name="registering-for-application-entry-points"></a><span data-ttu-id="62f67-208">註冊應用程式進入點</span><span class="sxs-lookup"><span data-stu-id="62f67-208">Registering for Application Entry Points</span></span>

<span data-ttu-id="62f67-209">應用程式在作業系統內可以有許多進入點。</span><span class="sxs-lookup"><span data-stu-id="62f67-209">An application can have many entry points within the operating system.</span></span> <span data-ttu-id="62f67-210">以下是進入點的建議位置：</span><span class="sxs-lookup"><span data-stu-id="62f67-210">The following are recommended locations for entry points:</span></span>

-   <span data-ttu-id="62f67-211">桌面</span><span class="sxs-lookup"><span data-stu-id="62f67-211">Desktop</span></span>
-   <span data-ttu-id="62f67-212">開始功能表</span><span class="sxs-lookup"><span data-stu-id="62f67-212">Start menu</span></span>
-   <span data-ttu-id="62f67-213">快速啟動 bar (Windows Vista 及更早版本) </span><span class="sxs-lookup"><span data-stu-id="62f67-213">Quick Launch bar (Windows Vista and earlier only)</span></span>
-   <span data-ttu-id="62f67-214">[通知] 區域</span><span class="sxs-lookup"><span data-stu-id="62f67-214">Notification area</span></span>
-   <span data-ttu-id="62f67-215">快顯功能表</span><span class="sxs-lookup"><span data-stu-id="62f67-215">Shortcut menus</span></span>
-   <span data-ttu-id="62f67-216">資料夾工作區</span><span class="sxs-lookup"><span data-stu-id="62f67-216">Folder task band</span></span>

<span data-ttu-id="62f67-217">本節著重于這些特定區域：</span><span class="sxs-lookup"><span data-stu-id="62f67-217">This section focuses on these specific areas:</span></span>

-   [<span data-ttu-id="62f67-218">開啟方式</span><span class="sxs-lookup"><span data-stu-id="62f67-218">Open With</span></span>](#open-with)
-   <span data-ttu-id="62f67-219">[[開始] 功能表和快速啟動 Bar](#start-menu-and-quick-launch-bar)</span><span class="sxs-lookup"><span data-stu-id="62f67-219">[Start Menu and Quick Launch Bar](#start-menu-and-quick-launch-bar)</span></span>

### <a name="open-with"></a><span data-ttu-id="62f67-220">開啟方式</span><span class="sxs-lookup"><span data-stu-id="62f67-220">Open With</span></span>

<span data-ttu-id="62f67-221">[ **開啟** 檔案] 快速鍵功能表可讓使用者選取可處理特定檔案類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-221">The **Open With** shortcut menu enables the user to select an application that can handle a specific file type.</span></span> <span data-ttu-id="62f67-222">**開啟** 時，可以用來開啟具有應用程式一次的檔案，也可以用來設定該副檔名的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-222">While **Open With** can be used to open a file with an application one time, it can also be used to set the default for that file name extension.</span></span> <span data-ttu-id="62f67-223">因此，應用程式應該一律註冊以 **開啟** ，讓使用者可以選擇使用該應用程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-223">Therefore, an application should always register for **Open With** so that users are presented with that application as a choice.</span></span> <span data-ttu-id="62f67-224">應用程式可以註冊的檔案類型和通訊協定，以供 **開啟**。</span><span class="sxs-lookup"><span data-stu-id="62f67-224">Applications can register both file types and protocols for **Open With**.</span></span> <span data-ttu-id="62f67-225">在預設程式架構中註冊通訊協定的應用程式，會自動新增至 [ **開啟]，** 以取得通訊協定。</span><span class="sxs-lookup"><span data-stu-id="62f67-225">Applications that register protocols in the Default Programs framework are automatically added to the **Open With** options for protocols.</span></span>

<span data-ttu-id="62f67-226">如需註冊 **Open With** 的詳細資訊，請參閱檔案 [關聯簡介](fa-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="62f67-226">For information on registering for **Open With**, see [Introduction to File Associations](fa-intro.md).</span></span>

### <a name="start-menu-and-quick-launch-bar"></a><span data-ttu-id="62f67-227">[開始] 功能表和快速啟動 Bar</span><span class="sxs-lookup"><span data-stu-id="62f67-227">Start Menu and Quick Launch Bar</span></span>

<span data-ttu-id="62f67-228">為了更容易找到使用者，應用程式可以在 Windows 中將快捷方式新增至不同的位置。</span><span class="sxs-lookup"><span data-stu-id="62f67-228">To become more discoverable to the user, applications can add shortcuts to various locations in Windows.</span></span> <span data-ttu-id="62f67-229">新增快捷方式最常見的地方就是 [ **開始** ] 功能表。</span><span class="sxs-lookup"><span data-stu-id="62f67-229">The most common place to add a shortcut is the **Start** menu.</span></span> <span data-ttu-id="62f67-230">在 Windows Vista 和更新版本中，應用程式會在隱藏的資料夾% ProgramData% Microsoft Windows [開始] 功能表程式中建立快捷方式， \\ \\ \\ \\ 以顯示在所有使用者的 [ **開始** ] 功能表的程式清單中。</span><span class="sxs-lookup"><span data-stu-id="62f67-230">In Windows Vista and later, an application creates a shortcut in the hidden folder %ProgramData%\\Microsoft\\Windows\\Start Menu\\Programs to appear in the **Start** menu's list of programs for all users.</span></span> <span data-ttu-id="62f67-231">通常，應用程式會新增包含快捷方式的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="62f67-231">Commonly, an application adds a subfolder that contains the shortcut.</span></span>

<span data-ttu-id="62f67-232">針對瀏覽器和電子郵件程式，Windows Vista [ **開始** ] 功能表也會在程式清單外面提供兩個專用連結，標準方式標題為 [ **網際網路** 及 **電子郵件**]。</span><span class="sxs-lookup"><span data-stu-id="62f67-232">For browser and email programs, the Windows Vista **Start** menu also presents two dedicated links outside of the program list, canonically titled **Internet** and **E-mail**.</span></span> <span data-ttu-id="62f67-233">在應用程式註冊這些類別之後，預設的程式架構可以管理透過這些連結啟動的專案。</span><span class="sxs-lookup"><span data-stu-id="62f67-233">After an application registers for those categories, the Default Programs framework can manage what is launched through those links.</span></span>

> [!Note]  
> <span data-ttu-id="62f67-234">從 Windows 7 開始， **網際網路** 和 **電子郵件** 專用的 [ **開始** ] 功能表連結不再存在。</span><span class="sxs-lookup"><span data-stu-id="62f67-234">The **Internet** and **E-mail** dedicated **Start** menu links are no longer present as of Windows 7.</span></span>

 

<span data-ttu-id="62f67-235">為了進一步提高可探索性，應用程式也可以將快捷方式新增至桌面和快速啟動 bar。</span><span class="sxs-lookup"><span data-stu-id="62f67-235">To further increase discoverability, applications can also add shortcuts to the desktop and the Quick Launch bar.</span></span> <span data-ttu-id="62f67-236">應用程式應該在安裝期間或第一次執行) 之前要求使用者提供許可權 (，然後再將圖示新增至 [ **開始** ] 功能表、桌面或快速啟動列。</span><span class="sxs-lookup"><span data-stu-id="62f67-236">Applications should ask the user for permission (usually during installation or on first run) before adding an icon to the **Start** menu, desktop, or Quick Launch bar.</span></span>

> [!Note]  
> <span data-ttu-id="62f67-237">Windows 7 不再提供快速啟動 bar。</span><span class="sxs-lookup"><span data-stu-id="62f67-237">The Quick Launch bar is no longer available as of Windows 7.</span></span> <span data-ttu-id="62f67-238">Windows 7 的替代方案是讓應用程式釘選到工作列，但是無法以程式設計方式進行釘選，因為這是使用者選擇的絕對選項。</span><span class="sxs-lookup"><span data-stu-id="62f67-238">The Windows 7 alternative is to have the application pinned to the Taskbar, but pinning cannot be done programmatically as it is strictly a user choice.</span></span>

 

<span data-ttu-id="62f67-239">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="62f67-239">For more information, see these topics:</span></span>

-   <span data-ttu-id="62f67-240">[如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)</span><span class="sxs-lookup"><span data-stu-id="62f67-240">[How to Register an Internet Browser or Email Client With the Windows Start Menu](start-menu-reg.md)</span></span>
-   [<span data-ttu-id="62f67-241">使用用戶端類型註冊程式</span><span class="sxs-lookup"><span data-stu-id="62f67-241">Registering Programs with Client Types</span></span>](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a><span data-ttu-id="62f67-242">應用程式安裝和預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-242">Application Installation and Defaults</span></span>

<span data-ttu-id="62f67-243">應用程式安裝程式在 Windows XP 之後根本沒有改變，但是執行的 Windows 版本高於 Windows 8 的系統有新的指導方針：在安裝時採用每一電腦的預設值，但在使用者第一次執行應用程式之前，並不會設定任何每個使用者的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-243">Application installation procedures have not fundamentally changed since Windows XP, with the exception of a new guideline for systems running versions of Windows older than Windows 8: take per-computer defaults at installation time but do not set any per-user defaults until that user first runs the application.</span></span> <span data-ttu-id="62f67-244"> (請參閱 [應用程式的第一次執行和預設值](#application-first-run-and-defaults)。 ) 應用程式在安裝期間不應設定依使用者的預設值，因為在某些情況下，安裝應用程式的人員不是預期的使用者。</span><span class="sxs-lookup"><span data-stu-id="62f67-244">(See [Application First Run and Defaults](#application-first-run-and-defaults).) Applications should not set per-user defaults during installation because there are situations in which the person installing the application is not the intended user.</span></span> <span data-ttu-id="62f67-245">從 Windows 8，不支援每部電腦預設值，而且應用程式無法變更每個使用者的預設設定。</span><span class="sxs-lookup"><span data-stu-id="62f67-245">As of Windows 8, per-computer defaults are not supported and applications cannot change per-user default settings.</span></span>

<span data-ttu-id="62f67-246">在安裝期間，應用程式應該將其二進位檔複製到硬碟，並將其 Progid 寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="62f67-246">During installation, an application should copy its binaries to the hard disk and write its ProgIDs to the registry.</span></span> <span data-ttu-id="62f67-247">應用程式也應該註冊預設程式，並針對每個檔案關聯 **開啟** ，以供處理它的候選項目。</span><span class="sxs-lookup"><span data-stu-id="62f67-247">The application should also register for Default Programs and **Open With** at this time for every file association it is a candidate to handle.</span></span> <span data-ttu-id="62f67-248">應用程式可以使用 **OpenWithProgIds** 子機碼來註冊 **Open with**。</span><span class="sxs-lookup"><span data-stu-id="62f67-248">The application can use the **OpenWithProgIds** subkey to register with **Open With**.</span></span>

<span data-ttu-id="62f67-249">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="62f67-249">For more information, see these topics:</span></span>

-   [<span data-ttu-id="62f67-250">預設程式</span><span class="sxs-lookup"><span data-stu-id="62f67-250">Default Programs</span></span>](default-programs.md)
-   [<span data-ttu-id="62f67-251">檔案關聯簡介</span><span class="sxs-lookup"><span data-stu-id="62f67-251">Introduction to File Associations</span></span>](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a><span data-ttu-id="62f67-252">應用程式升級和預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-252">Application Upgrades and Defaults</span></span>

<span data-ttu-id="62f67-253">許多應用程式都能夠隨著時間進行升級。</span><span class="sxs-lookup"><span data-stu-id="62f67-253">Many applications have the ability to upgrade themselves over time.</span></span> <span data-ttu-id="62f67-254">此升級程式不應變更每個使用者預設值的狀態，因為該變更對使用者而言不是預期的。</span><span class="sxs-lookup"><span data-stu-id="62f67-254">This upgrade procedure should not change the state of per-user defaults because that change would be unexpected to the user.</span></span> <span data-ttu-id="62f67-255">但是，應用程式可接受檢查電腦層級的檔案關聯，並在其損毀時加以修復。</span><span class="sxs-lookup"><span data-stu-id="62f67-255">However, it is acceptable for an application to check computer-level file associations and repair them if they have been corrupted.</span></span>

## <a name="application-first-run-and-defaults"></a><span data-ttu-id="62f67-256">應用程式第一次執行和預設值</span><span class="sxs-lookup"><span data-stu-id="62f67-256">Application First Run and Defaults</span></span>

> [!Note]  
> <span data-ttu-id="62f67-257">從 Windows 8，系統會代表所有應用程式處理此程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-257">As of Windows 8, the system handles this procedure on behalf of all applications.</span></span> <span data-ttu-id="62f67-258">應用程式本身無法再查詢及變更預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-258">Applications themselves can no longer query and change defaults.</span></span> <span data-ttu-id="62f67-259">只有使用者可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="62f67-259">Only the user can do that.</span></span> <span data-ttu-id="62f67-260">因此，應用程式不應該嘗試查詢目前的預設值，或透過任何機制變更預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-260">Therefore, applications should not attempt to query for the current default or change that default through any mechanism.</span></span> <span data-ttu-id="62f67-261">不過，應用程式可以藉由呼叫 [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)介面的 [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui)方法，在主控台中提供預設程式的進入點。</span><span class="sxs-lookup"><span data-stu-id="62f67-261">However, applications can provide an entry point to Default Programs in the Control Panel by calling the [**LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) method of the [**IApplicationAssociationRegistrationUI**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) interface.</span></span>

 

<span data-ttu-id="62f67-262">隨著 Windows Vista 中的每個使用者預設值的推出，以熱門的副檔名為比賽的應用程式必須提供一般使用者體驗來宣告這些延伸模組。</span><span class="sxs-lookup"><span data-stu-id="62f67-262">With the introduction of per-user defaults in Windows Vista, it is important that applications that contest for popular file name extensions all provide a common user experience to claim these extensions.</span></span> <span data-ttu-id="62f67-263">因為這些預設值現在是在使用者的內容中設定，所以只有在使用者于安裝之後執行程式時，才會將本身呈現為預設的可能性。</span><span class="sxs-lookup"><span data-stu-id="62f67-263">Because these defaults are now set in the context of the user, they should present themselves as a default possibility only when the user runs the program after installation.</span></span>

<span data-ttu-id="62f67-264">建立每個使用者預設值的指導方針如下：第一次執行特定使用者的應用程式時，該應用程式應該為其本身的預設值和檔案關聯要求使用者喜好設定。</span><span class="sxs-lookup"><span data-stu-id="62f67-264">The guideline for establishing per-user defaults is this: When an application is first run for a specific user, that application should request user preferences for defaults and file associations for itself.</span></span>

<span data-ttu-id="62f67-265">建議的 UI 應該為使用者提供兩個清楚的選擇：</span><span class="sxs-lookup"><span data-stu-id="62f67-265">The recommended UI should provide two clear choices to the user:</span></span>

1.  <span data-ttu-id="62f67-266">接受應用程式想要宣稱的所有預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-266">Accept all defaults that the application would like to claim.</span></span> <span data-ttu-id="62f67-267">此選項也可以設定應用程式的其他預設屬性，例如 [隱私權] 或 [自動更新] 設定。</span><span class="sxs-lookup"><span data-stu-id="62f67-267">This option might also set other default properties of the application such as privacy or automatic update settings.</span></span> <span data-ttu-id="62f67-268">此選項可讓應用程式宣告其所有已註冊的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-268">This option allows the application to claim all of its registered defaults.</span></span>
2.  <span data-ttu-id="62f67-269">藉由接受或不個別接受預設選項和程式設定來自訂。</span><span class="sxs-lookup"><span data-stu-id="62f67-269">Customize by accepting or not accepting default selections and program settings individually.</span></span> <span data-ttu-id="62f67-270">此選項會提供進一步的 UI，讓使用者可以針對其預設選項進行更細微的選擇。</span><span class="sxs-lookup"><span data-stu-id="62f67-270">This option presents further UI that enables the user to make granular choices for their default options.</span></span>

<span data-ttu-id="62f67-271">如需詳細資訊，請參閱 [預設程式](default-programs.md)。</span><span class="sxs-lookup"><span data-stu-id="62f67-271">For more information, see [Default Programs](default-programs.md).</span></span>

## <a name="verifying-defaults-and-asking-for-user-consent"></a><span data-ttu-id="62f67-272">驗證預設值並要求使用者同意</span><span class="sxs-lookup"><span data-stu-id="62f67-272">Verifying Defaults and Asking for User Consent</span></span>

> [!Note]  
> <span data-ttu-id="62f67-273">Windows 8 不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="62f67-273">This is not supported as of Windows 8.</span></span>

 

<span data-ttu-id="62f67-274">當應用程式在 Windows Vista 和更新版本中向預設程式註冊之後，應用程式就可以使用某些 Api。</span><span class="sxs-lookup"><span data-stu-id="62f67-274">After an application registers with Default Programs in Windows Vista and later, certain APIs become available to the application.</span></span> <span data-ttu-id="62f67-275">例如，應用程式可能需要檢查它是否為預設程式。</span><span class="sxs-lookup"><span data-stu-id="62f67-275">For instance, an application might need to check whether it is the default program.</span></span> <span data-ttu-id="62f67-276">[**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)介面會提供方法來進行此作業。</span><span class="sxs-lookup"><span data-stu-id="62f67-276">The [**IApplicationAssociationRegistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) interface provides methods to do this.</span></span>

<span data-ttu-id="62f67-277">任何想要宣告預設值的應用程式都必須先要求使用者，而且永遠不會宣告預設值（不含許可權）。</span><span class="sxs-lookup"><span data-stu-id="62f67-277">Any application that wants to claim defaults must first ask the user and never claim defaults without permission.</span></span> <span data-ttu-id="62f67-278">系統應詢問使用者是否要將應用程式設為預設值，或保留目前的預設值。</span><span class="sxs-lookup"><span data-stu-id="62f67-278">The user should be asked whether they want to make the application the default or leave the current default in place.</span></span> <span data-ttu-id="62f67-279">在使用者進行選擇後，應該也不會再詢問此問題。</span><span class="sxs-lookup"><span data-stu-id="62f67-279">There should also be an option not to be asked this question again after the user has made their choice.</span></span>

<span data-ttu-id="62f67-280">如需詳細資訊，請參閱 [預設程式](default-programs.md)。</span><span class="sxs-lookup"><span data-stu-id="62f67-280">For more information, see [Default Programs](default-programs.md).</span></span>

## <a name="application-compatibility-tips"></a><span data-ttu-id="62f67-281">應用程式相容性秘訣</span><span class="sxs-lookup"><span data-stu-id="62f67-281">Application Compatibility Tips</span></span>

<span data-ttu-id="62f67-282">本節提供一些與 Windows 中的預設程式經驗相關的應用程式相容性秘訣。</span><span class="sxs-lookup"><span data-stu-id="62f67-282">This section provides some application compatibility tips related to the Default Programs experience in Windows.</span></span>

### <a name="avoid-triggering-per-user-virtualization"></a><span data-ttu-id="62f67-283">避免觸發 Per-User 虛擬化</span><span class="sxs-lookup"><span data-stu-id="62f67-283">Avoid Triggering Per-User Virtualization</span></span>

<span data-ttu-id="62f67-284">使用「使用者帳戶控制」 (UAC) 環境中，應用程式一律會以標準使用者權限執行，以獲得最佳的客戶體驗。</span><span class="sxs-lookup"><span data-stu-id="62f67-284">With the user account control (UAC) environment, applications should always run with only standard user rights for the best customer experience.</span></span> <span data-ttu-id="62f67-285">基於安全性考慮，系統會封鎖具有標準使用者權限層級的應用程式，使其無法寫入登錄的特定部分和特定的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="62f67-285">For security reasons, applications with a standard user privilege level are blocked from writing to certain parts of the registry and to certain system files.</span></span> <span data-ttu-id="62f67-286">Windows Vista 和更新版本的 Windows (AppCompat) 層提供暫時性的應用程式相容性，以協助應用程式進行轉換。</span><span class="sxs-lookup"><span data-stu-id="62f67-286">Windows Vista and later versions of Windows provide a temporary application compatibility (AppCompat) layer to help applications make the transition.</span></span> <span data-ttu-id="62f67-287">封鎖寫入登錄或系統檔案的嘗試會「虛擬化」，讓應用程式繼續執行，但不會改變系統的機密區域。</span><span class="sxs-lookup"><span data-stu-id="62f67-287">Blocked attempts to write to the registry or to system files are "virtualized" so that the application continues to run, but the sensitive areas of the system are not altered.</span></span> <span data-ttu-id="62f67-288">不過，應用程式不應依賴 AppCompat 技術做為長期解決方案。</span><span class="sxs-lookup"><span data-stu-id="62f67-288">However, applications should not rely on the AppCompat technology as a long-term solution.</span></span> <span data-ttu-id="62f67-289">相反地，應用程式應該使用許多可用的工具來確認它們可以在標準使用者權限下順利執行。</span><span class="sxs-lookup"><span data-stu-id="62f67-289">Instead, applications should use the many available tools to verify that they can run successfully under standard user rights.</span></span> <span data-ttu-id="62f67-290">應用程式的某些 reprogramming 可能是完成這項工作的必要項，但它應該是以長期相容性的方式來完成。</span><span class="sxs-lookup"><span data-stu-id="62f67-290">Some reprogramming of the application might be required to accomplish this, but it should be done in the interest of long-term compatibility.</span></span>

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a><span data-ttu-id="62f67-291">避免從程式相容性助理 AppCompat 警告或區塊</span><span class="sxs-lookup"><span data-stu-id="62f67-291">Avoid AppCompat Warnings or Blocks from the Program Compatibility Assistant</span></span>

<span data-ttu-id="62f67-292">Windows Vista 和更新版本中提供「程式相容性助理」 (PCA) 。</span><span class="sxs-lookup"><span data-stu-id="62f67-292">The Program Compatibility Assistant (PCA) is provided in Windows Vista and later.</span></span> <span data-ttu-id="62f67-293">其目的是要提供自動化的方法，讓相容性問題較舊的程式更能運作。</span><span class="sxs-lookup"><span data-stu-id="62f67-293">Its purpose is to provide an automated method to make older programs with compatibility issues work better.</span></span> <span data-ttu-id="62f67-294">PCA 會監視程式的已知問題。</span><span class="sxs-lookup"><span data-stu-id="62f67-294">The PCA monitors programs for known issues.</span></span> <span data-ttu-id="62f67-295">如果偵測到問題，則會在使用者再次執行程式之前，通知使用者有問題，並提供可套用有效解決方案的供應專案。</span><span class="sxs-lookup"><span data-stu-id="62f67-295">If an issue is detected, it notifies the user of the problem and offers to apply effective solutions before the user runs the program again.</span></span> <span data-ttu-id="62f67-296">為了避免看到這些警告或區塊，Isv 應該使用許多可用的工具，以確保其應用程式與 Windows Vista、Windows 7 和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="62f67-296">To avoid seeing these warnings or blocks, ISVs should use the many available tools to ensure that their applications are compatible with Windows Vista, Windows 7, and later.</span></span>

### <a name="support-for-previous-windows-operating-system-versions"></a><span data-ttu-id="62f67-297">舊版 Windows 作業系統的支援</span><span class="sxs-lookup"><span data-stu-id="62f67-297">Support for Previous Windows Operating System Versions</span></span>

<span data-ttu-id="62f67-298">在 Windows Vista 之前，Windows 作業系統上無法使用預設程式基礎結構。</span><span class="sxs-lookup"><span data-stu-id="62f67-298">The Default Programs infrastructure is not available on any Windows operating system before Windows Vista.</span></span> <span data-ttu-id="62f67-299">因此，當應用程式移至新的預設程式基礎結構時，應該保留舊版的應用程式預設程式碼，以維持與舊版 Windows 的相容性。</span><span class="sxs-lookup"><span data-stu-id="62f67-299">Therefore, when applications move to the new Default Programs infrastructure, they should retain their older application-defaults code to maintain compatibility with older versions of Windows.</span></span> <span data-ttu-id="62f67-300">應用程式應該在安裝時執行作業系統版本檢查，以判斷要執行的應用程式預設程式碼。</span><span class="sxs-lookup"><span data-stu-id="62f67-300">An application should run an operating system version check as part of its installation to determine which application-defaults code to run.</span></span>

<span data-ttu-id="62f67-301">為了支援從 Windows XP 升級到 Windows Vista 或更新版本，應用程式應該新增預設程式所需的所有登錄專案，即使它們是安裝在執行 Windows XP 的電腦上也一樣。</span><span class="sxs-lookup"><span data-stu-id="62f67-301">To support an upgrade from Windows XP to Windows Vista or later, applications should add all the registry entries required for Default Programs even when they are installing on a computer running Windows XP.</span></span> <span data-ttu-id="62f67-302">註冊在執行 Windows XP 的電腦上不會有任何作用，但如果電腦稍後升級，應用程式將會註冊，而且能夠利用架構。</span><span class="sxs-lookup"><span data-stu-id="62f67-302">The registration will have no effect on a computer running Windows XP, but if the computer is later upgraded, the application will be already registered and able to take advantage of the framework.</span></span>

<span data-ttu-id="62f67-303">如需詳細資訊，請參閱 [**OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa)。</span><span class="sxs-lookup"><span data-stu-id="62f67-303">For more information, see [**OSVERSIONINFO**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62f67-304">其他資源</span><span class="sxs-lookup"><span data-stu-id="62f67-304">Additional Resources</span></span>

-   [<span data-ttu-id="62f67-305">檔案關聯簡介</span><span class="sxs-lookup"><span data-stu-id="62f67-305">Introduction to File Associations</span></span>](fa-intro.md)
-   <span data-ttu-id="62f67-306">[如何使用 Windows [開始] 功能表註冊網際網路瀏覽器或電子郵件客戶程式](start-menu-reg.md)</span><span class="sxs-lookup"><span data-stu-id="62f67-306">[How to Register an Internet Browser or Email Client With the Windows Start Menu](start-menu-reg.md)</span></span>
-   <span data-ttu-id="62f67-307">[將應用程式註冊至 URI 配置](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="62f67-307">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="62f67-308">相關主題</span><span class="sxs-lookup"><span data-stu-id="62f67-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f67-309">檔案關聯的最佳作法</span><span class="sxs-lookup"><span data-stu-id="62f67-309">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="62f67-310">檔案關聯範例案例</span><span class="sxs-lookup"><span data-stu-id="62f67-310">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="62f67-311">預設程式</span><span class="sxs-lookup"><span data-stu-id="62f67-311">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="62f67-312">使用設定程式存取和電腦預設值 (SPAD) </span><span class="sxs-lookup"><span data-stu-id="62f67-312">Working with Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
