---
description: 跨 Windows 版本的 MUI 支援演進
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: 跨 Windows 版本的 MUI 支援演進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983738"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="a34e5-103">跨 Windows 版本的 MUI 支援演進</span><span class="sxs-lookup"><span data-stu-id="a34e5-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="a34e5-104">Windows Vista 之前</span><span class="sxs-lookup"><span data-stu-id="a34e5-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="a34e5-105">Windows Vista 和其他</span><span class="sxs-lookup"><span data-stu-id="a34e5-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="a34e5-106">非語言相關/MUI 作業系統</span><span class="sxs-lookup"><span data-stu-id="a34e5-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="a34e5-107">部署案例完全以 MUI 為基礎</span><span class="sxs-lookup"><span data-stu-id="a34e5-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="a34e5-108">單一映射部署</span><span class="sxs-lookup"><span data-stu-id="a34e5-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="a34e5-109">改進的服務模型</span><span class="sxs-lookup"><span data-stu-id="a34e5-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="a34e5-110">MUI 基礎結構</span><span class="sxs-lookup"><span data-stu-id="a34e5-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="a34e5-111">語言管理</span><span class="sxs-lookup"><span data-stu-id="a34e5-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="a34e5-112">資源處理</span><span class="sxs-lookup"><span data-stu-id="a34e5-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="a34e5-113">Windows Vista 之前</span><span class="sxs-lookup"><span data-stu-id="a34e5-113">Before Windows Vista</span></span>

<span data-ttu-id="a34e5-114">在 Windows Vista 發行之前，Windows 隨附單一語言的映射，這表示每個當地語系化版本的 Windows 都包含單一語言的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="a34e5-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="a34e5-115">MUI 是英文版作業系統的附加元件，且多語系消費者介面套件只能新增至某些英文版的 Windows。</span><span class="sxs-lookup"><span data-stu-id="a34e5-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="a34e5-116">當安裝在英文版的 Windows 上時，MUI 允許根據個別使用者的喜好設定，將作業系統的使用者介面語言變更為其中一種支援的語言。</span><span class="sxs-lookup"><span data-stu-id="a34e5-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="a34e5-117">MUI 套件模型不會公開應用程式的 MUI 支援。</span><span class="sxs-lookup"><span data-stu-id="a34e5-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="a34e5-118">雖然開發人員可以建立多語言的應用程式，但他們必須建立自己的機制來進行。</span><span class="sxs-lookup"><span data-stu-id="a34e5-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="a34e5-119">Windows Vista 和其他</span><span class="sxs-lookup"><span data-stu-id="a34e5-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="a34e5-120">在 Windows Vista 中，Microsoft 對 MUI 進行了大幅的投資。</span><span class="sxs-lookup"><span data-stu-id="a34e5-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="a34e5-121">Windows Vista 是在 MUI 平臺上從頭建立。</span><span class="sxs-lookup"><span data-stu-id="a34e5-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="a34e5-122">雖然這代表 Windows 當地語系化策略的一大進展，因為這是 Microsoft 為了提供比以往更多語言的 Windows，這對 Windows 使用者和客戶而言是一項很好的進步。</span><span class="sxs-lookup"><span data-stu-id="a34e5-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="a34e5-123">非語言相關/MUI 作業系統</span><span class="sxs-lookup"><span data-stu-id="a34e5-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="a34e5-124">大部分的 Windows Vista 二進位檔都符合 MUI 規範，且可當地語系化的資料會與程式碼分開儲存。</span><span class="sxs-lookup"><span data-stu-id="a34e5-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="a34e5-125">這可提供彈性，因為您可以隨時新增不同的語言資料。</span><span class="sxs-lookup"><span data-stu-id="a34e5-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="a34e5-126">部署案例完全以 MUI 為基礎</span><span class="sxs-lookup"><span data-stu-id="a34e5-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="a34e5-127">Windows Vista 封裝和安裝設計是以 MUI 為基礎，所有可當地語系化的資料都封裝在特定語言的套件中，而且每個語言套件都可以在不同的案例中部署。</span><span class="sxs-lookup"><span data-stu-id="a34e5-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="a34e5-128">例如，雖然適用于 Windows Vista 的零售版 Dvd 包含單一語言版本，但最終版本的使用者可以下載其他的 MUI 語言套件，並可從 [ **地區及語言選項** ] 控制台切換 UI 語言。</span><span class="sxs-lookup"><span data-stu-id="a34e5-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="a34e5-129">Enterprise edition 授權會取得所有語言，而且可以部署任何語言。</span><span class="sxs-lookup"><span data-stu-id="a34e5-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="a34e5-130">單一映射部署</span><span class="sxs-lookup"><span data-stu-id="a34e5-130">Single image deployment</span></span>

<span data-ttu-id="a34e5-131">企業客戶和 Oem 現在可以減少需要維護的映射數目，以便透過單一映射部署將 Windows 和應用程式部署到不同地區設定的電腦上。</span><span class="sxs-lookup"><span data-stu-id="a34e5-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="a34e5-132">在 Windows Vista 上使用 MUI，可將一個包含多種語言的映射部署到任何語言使用者，且使用者可以在設定期間，或在電腦的初始「全新體驗」中，判斷其慣用語言)  (。</span><span class="sxs-lookup"><span data-stu-id="a34e5-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="a34e5-133">尤其是，Oem 可以在新電腦上放置許多 UI 語言，讓使用者從歡迎中心中選取一個。</span><span class="sxs-lookup"><span data-stu-id="a34e5-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="a34e5-134">因此，在具有多個語言套件的映射中，安裝程式會顯示可用語言的清單，並讓使用者挑選其中一種語言。</span><span class="sxs-lookup"><span data-stu-id="a34e5-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="a34e5-135">然後，所有國際設定會設定為符合選取的語言或地區設定。</span><span class="sxs-lookup"><span data-stu-id="a34e5-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="a34e5-136">改進的服務模型</span><span class="sxs-lookup"><span data-stu-id="a34e5-136">Improved servicing model</span></span>

<span data-ttu-id="a34e5-137">相同的 QFE 或安全性修正套件現在可以安裝在任何語言系統之上。</span><span class="sxs-lookup"><span data-stu-id="a34e5-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="a34e5-138">這一點很重要，因為它可以更快速地解決安全性問題，並讓所有的國際使用者都能從所有安全性修正程式的相同時間可用性獲得獲益。</span><span class="sxs-lookup"><span data-stu-id="a34e5-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="a34e5-139">MUI 基礎結構</span><span class="sxs-lookup"><span data-stu-id="a34e5-139">MUI infrastructure</span></span>

<span data-ttu-id="a34e5-140">從 Windows Vista 開始，MUI Api 可讓開發人員利用自己應用程式的 MUI 機制，而不需要建立自訂邏輯來處理資源和語言管理。</span><span class="sxs-lookup"><span data-stu-id="a34e5-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="a34e5-141">語言管理</span><span class="sxs-lookup"><span data-stu-id="a34e5-141">Language management</span></span>

<span data-ttu-id="a34e5-142">提供 UI 語言管理功能的基底 MUI Api 可做為 MUI 基礎結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="a34e5-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="a34e5-143">為了協助管理系統、使用者和應用層級的不同 UI 語言設定，MUI 會在內部將它們合併成單一優先順序的清單。</span><span class="sxs-lookup"><span data-stu-id="a34e5-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="a34e5-144">然後，MUI 會根據此優先順序清單來實行回溯機制，以允許部分當地語系化解決方案，同時為使用者提供適當的（如果不是慣用的）使用者介面語言體驗。</span><span class="sxs-lookup"><span data-stu-id="a34e5-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="a34e5-145">例如，執行西班牙文語言介面套件 (LIP) 安裝在基礎作業系統上的系統可支援下列行為：系統會先嘗試將其資源顯示在加泰羅尼亞文中，如果這些資源不適用於加泰羅尼亞文，則請改為提供使用者西班牙資源。</span><span class="sxs-lookup"><span data-stu-id="a34e5-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="a34e5-146">資源處理</span><span class="sxs-lookup"><span data-stu-id="a34e5-146">Resource handling</span></span>

<span data-ttu-id="a34e5-147">從 Windows Vista 開始提供的改良式 MUI 基礎結構，最常見的資源技術已啟用 MUI。</span><span class="sxs-lookup"><span data-stu-id="a34e5-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="a34e5-148">下表提供 Windows Vista 中可用資源處理支援的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a34e5-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a34e5-149">類別</span><span class="sxs-lookup"><span data-stu-id="a34e5-149">Category</span></span></th>
<th><span data-ttu-id="a34e5-150">支援</span><span class="sxs-lookup"><span data-stu-id="a34e5-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a34e5-151">支援的資源類型</span><span class="sxs-lookup"><span data-stu-id="a34e5-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="a34e5-152">Win32/非受控資源：。DLL/。EXE/。Ocx</span><span class="sxs-lookup"><span data-stu-id="a34e5-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="a34e5-153">Shell 相關的註冊</span><span class="sxs-lookup"><span data-stu-id="a34e5-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="a34e5-154">管理相關資源：事件記錄檔、嵌入式管理單元/SERVICES.MSC 檔案</span><span class="sxs-lookup"><span data-stu-id="a34e5-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="a34e5-155">WMI： MOF/MFL</span><span class="sxs-lookup"><span data-stu-id="a34e5-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="a34e5-156">群組原則： ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="a34e5-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="a34e5-157">受控 Resources.dll</span><span class="sxs-lookup"><span data-stu-id="a34e5-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a34e5-158">開發工具</span><span class="sxs-lookup"><span data-stu-id="a34e5-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="a34e5-159">若為 Win32： RC.exe、MUIRCT.exe 和 Visual Studio 2005 和更新版本</span><span class="sxs-lookup"><span data-stu-id="a34e5-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a34e5-160">有限的資源類型支援</span><span class="sxs-lookup"><span data-stu-id="a34e5-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="a34e5-161">\* .chm 說明檔</span><span class="sxs-lookup"><span data-stu-id="a34e5-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



