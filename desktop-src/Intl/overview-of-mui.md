---
description: 本主題提供多語系消費者介面 (MUI) 技術的概念，以及它為啟用多語系使用者體驗所提供的平臺支援，以及它為 Windows 生態系統提供的優點。
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: MUI 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553139"
---
# <a name="overview-of-mui"></a><span data-ttu-id="91840-103">MUI 總覽</span><span class="sxs-lookup"><span data-stu-id="91840-103">Overview of MUI</span></span>

<span data-ttu-id="91840-104">本主題提供多語系消費者介面 (MUI) 技術的概念，以及它為啟用多語系使用者體驗所提供的平臺支援，以及它為 Windows 生態系統提供的優點。</span><span class="sxs-lookup"><span data-stu-id="91840-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="91840-105">在此頁面上：</span><span class="sxs-lookup"><span data-stu-id="91840-105">On this page:</span></span>

-   [<span data-ttu-id="91840-106">多語系計算的需求</span><span class="sxs-lookup"><span data-stu-id="91840-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="91840-107">MUI 在啟用多語系運算的角色</span><span class="sxs-lookup"><span data-stu-id="91840-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="91840-108">MUI 的核心概念</span><span class="sxs-lookup"><span data-stu-id="91840-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="91840-109">Windows 中的 MUI 記錄</span><span class="sxs-lookup"><span data-stu-id="91840-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="91840-110">MUI 技術的優點</span><span class="sxs-lookup"><span data-stu-id="91840-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="91840-111">多語系計算的需求</span><span class="sxs-lookup"><span data-stu-id="91840-111">The need for multilingual computing</span></span>

<span data-ttu-id="91840-112">為了受益于國際市場所呈現的成長機會，Microsoft 的平臺和應用程式支援比以往更多的語言、文化特性和市場。</span><span class="sxs-lookup"><span data-stu-id="91840-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="91840-113">除了增加全球化趨勢，語言、文化特性和市場細節仍與國際使用者非常相關。</span><span class="sxs-lookup"><span data-stu-id="91840-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="91840-114">下圖顯示非英文的喇叭仍占世界人口的91.5%。</span><span class="sxs-lookup"><span data-stu-id="91840-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![包含三個區段的圓形圖;標示為「非英文喇叭91.5%」的那個會大幅大於另二個組合](images/overview-of-mui-fig1.gif)

<span data-ttu-id="91840-116">全球有193個國家/地區，以及過去使用的6900種已知生活語言。</span><span class="sxs-lookup"><span data-stu-id="91840-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="91840-117">無論其角色是世界的商務語言，英文都只會以第一或第二種語言的世界人口8.5% 來說。</span><span class="sxs-lookup"><span data-stu-id="91840-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="91840-118">為了將原生資訊提供給全球人口的94%，這項資訊必須在 347 (大約有5% 的全球語言，且至少有一百萬個喇叭的 ) 。</span><span class="sxs-lookup"><span data-stu-id="91840-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="91840-119">這種情況更是如此，因為全球化趨勢已提高這些使用者對其市場的技術及其可用性的期望。</span><span class="sxs-lookup"><span data-stu-id="91840-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="91840-120">以更多語言當地語系化軟體的需要多年來，Microsoft 現在提供比以往更多語言的 Windows Vista 和其他產品。</span><span class="sxs-lookup"><span data-stu-id="91840-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="91840-121">這種演進功能對 Microsoft Windows 特別明顯，因為它已從使用 windows 98 支援30種語言到幾乎100版的 Windows Vista，如下列橫條圖所示。</span><span class="sxs-lookup"><span data-stu-id="91840-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![橫條圖顯示 windows vista 中比 windows 98 或 windows xp 更大的語言數目](images/overview-of-mui-fig2.gif)

<span data-ttu-id="91840-123">*圖 2-Microsoft Windows 版本支援的語言數目*</span><span class="sxs-lookup"><span data-stu-id="91840-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="91840-124">MUI 在啟用多語系運算的角色</span><span class="sxs-lookup"><span data-stu-id="91840-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="91840-125">如上一節所述， [全球化](glossary-for-understanding-mui.md) 和 [當地語系化](glossary-for-understanding-mui.md) 應用程式已成為更全球整合世界的必要項。</span><span class="sxs-lookup"><span data-stu-id="91840-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="91840-126">尤其是，當越來越多的企業在內部或透過其商業網路進行全球化時，多語言應用程式的需求會大幅增加。</span><span class="sxs-lookup"><span data-stu-id="91840-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="91840-127">這是這些公司目前在全球部署這些應用程式時所面臨的障礙。</span><span class="sxs-lookup"><span data-stu-id="91840-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="91840-128">為 windows 作業系統提供更多語言支援，以及為 Windows 平臺建立的軟體應用程式，都需要新的策略，讓所有主要案例都能以最基本的工程額外負荷來實行。</span><span class="sxs-lookup"><span data-stu-id="91840-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="91840-129">MUI 技術的目標物件是開發人員和 Isv，以建立並支援 Windows 平臺的多語系應用程式。</span><span class="sxs-lookup"><span data-stu-id="91840-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="91840-130">MUI 對 Oem 和企業來說也很重要，因為他們可以利用它來部署 Windows 作業系統，並透過單一映射部署將應用程式新增至不同語言的電腦。</span><span class="sxs-lookup"><span data-stu-id="91840-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="91840-131">MUI 的核心概念</span><span class="sxs-lookup"><span data-stu-id="91840-131">Core concepts of MUI</span></span>

<span data-ttu-id="91840-132">MUI 背後的基本概念是將可 [當地語系化資源的儲存區與應用程式原始程式碼分開](mui-fundamental-concepts-explained.md)，如此一來，就能將任何多語系應用程式設計成與語言中立的核心二進位檔和一組語言特定當地語系化資源檔的組合。</span><span class="sxs-lookup"><span data-stu-id="91840-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="91840-133">當應用程式原始程式碼與當地語系化的資源分開儲存之後，您就可以輕鬆地根據系統、使用者和應用層級的使用者介面語言設定，動態地針對指定的應用程式內容 [載入適當的當地語系化資源](mui-fundamental-concepts-explained.md) 。</span><span class="sxs-lookup"><span data-stu-id="91840-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="91840-134">這些 MUI 的基本屬性有助於加速商務案例，例如：</span><span class="sxs-lookup"><span data-stu-id="91840-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="91840-135">透過實體區隔應用程式原始程式碼和可當地語系化的資源，改善使用者介面和說明內容的當地語系化模型。</span><span class="sxs-lookup"><span data-stu-id="91840-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="91840-136">將可當地語系化的資源視為動態內容，並根據 UI 語言設定和回溯喜好設定來載入它們。</span><span class="sxs-lookup"><span data-stu-id="91840-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="91840-137">這可實現下列案例：</span><span class="sxs-lookup"><span data-stu-id="91840-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="91840-138">在執行時間從一個 UI 語言切換至另一個。</span><span class="sxs-lookup"><span data-stu-id="91840-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="91840-139">建立涵蓋一組適用于 Oem 和企業之語言的區域或全球單一部署映射。</span><span class="sxs-lookup"><span data-stu-id="91840-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="91840-140">Windows 中的 MUI 記錄</span><span class="sxs-lookup"><span data-stu-id="91840-140">History of MUI in Windows</span></span>

<span data-ttu-id="91840-141">針對 windows 作業系統層級的多語系使用者經驗，以及在 Windows 平臺上進行多語系應用程式開發的支援層級，在一段時間內和不同版本的 Windows 中都有演進。</span><span class="sxs-lookup"><span data-stu-id="91840-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="91840-142">[Windows Vista 之前](evolution-of-mui-support-across-windows-versions.md)的支援功能相當基本，具有單一語言的 windows 映射，以及在特定案例中附加元件多語系消費者介面套件的選項。</span><span class="sxs-lookup"><span data-stu-id="91840-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="91840-143">無語言應用程式的開發人員支援。</span><span class="sxs-lookup"><span data-stu-id="91840-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="91840-144">在[Windows vista](evolution-of-mui-support-across-windows-versions.md)中，MICROSOFT 對 mui 進行了大幅的投資，而 Windows vista 則是在 mui 平臺上從頭建立。</span><span class="sxs-lookup"><span data-stu-id="91840-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="91840-145">雖然這代表 Windows 當地語系化策略的主要進展，因為這是 Microsoft 在 windows 使用者、開發人員和客戶上提供更多語言的重要提供者，因此是最重要的一大步。</span><span class="sxs-lookup"><span data-stu-id="91840-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="91840-146">它提供數個主要優點，例如：</span><span class="sxs-lookup"><span data-stu-id="91840-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="91840-147">語言中立的作業系統，內建的 MUI 支援。</span><span class="sxs-lookup"><span data-stu-id="91840-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="91840-148">可設定的封裝、部署和安裝以支援多語系案例。</span><span class="sxs-lookup"><span data-stu-id="91840-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="91840-149">具有多種語言的單一映射部署。</span><span class="sxs-lookup"><span data-stu-id="91840-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="91840-150">改進的服務模型，可執行程式碼獨立于資源之外更新。</span><span class="sxs-lookup"><span data-stu-id="91840-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="91840-151">建立多語系應用程式的開發人員支援。</span><span class="sxs-lookup"><span data-stu-id="91840-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="91840-152">下表提供 MUI 的 Windows 平臺支援的詳細總覽：</span><span class="sxs-lookup"><span data-stu-id="91840-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91840-153">類別</span><span class="sxs-lookup"><span data-stu-id="91840-153">Category</span></span></th>
<th><span data-ttu-id="91840-154">支援</span><span class="sxs-lookup"><span data-stu-id="91840-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91840-155">支援的 Windows 版本 (OS 僅支援) </span><span class="sxs-lookup"><span data-stu-id="91840-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="91840-156">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="91840-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="91840-157">Windows 2000 伺服器系列</span><span class="sxs-lookup"><span data-stu-id="91840-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="91840-158">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="91840-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="91840-159">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="91840-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="91840-160">Windows Server 2003 系列</span><span class="sxs-lookup"><span data-stu-id="91840-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="91840-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="91840-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91840-162">支援的 Windows 版本 (OS & 應用程式支援) </span><span class="sxs-lookup"><span data-stu-id="91840-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="91840-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91840-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91840-164">不支援的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="91840-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="91840-165">Windows 9x</span><span class="sxs-lookup"><span data-stu-id="91840-165">Windows 9x</span></span></li>
<li><span data-ttu-id="91840-166">Windows Me</span><span class="sxs-lookup"><span data-stu-id="91840-166">Windows Me</span></span></li>
<li><span data-ttu-id="91840-167">Windows XP Home Edition</span><span class="sxs-lookup"><span data-stu-id="91840-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="91840-168">MUI 技術的優點</span><span class="sxs-lookup"><span data-stu-id="91840-168">Benefits of MUI technology</span></span>

<span data-ttu-id="91840-169">MUI 會積極影響 Windows 生態系統的多個層面：</span><span class="sxs-lookup"><span data-stu-id="91840-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="91840-170">[開發人員的優點](benefits-of-mui-explained.md)：有許多優點會透過 MUI API 支援的可用性提供給應用程式開發人員，以建立以與核心 Windows 作業系統本身的多語系支援相同準則為模型的多語系應用程式。</span><span class="sxs-lookup"><span data-stu-id="91840-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="91840-171">這些優點包括：</span><span class="sxs-lookup"><span data-stu-id="91840-171">These benefits include:</span></span>
    -   <span data-ttu-id="91840-172">提供與作業系統本身提供一致之顯示語言體驗的能力。</span><span class="sxs-lookup"><span data-stu-id="91840-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="91840-173">輕鬆擴充應用程式語言支援的能力。</span><span class="sxs-lookup"><span data-stu-id="91840-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="91840-174">輕鬆維護及服務應用程式的能力。</span><span class="sxs-lookup"><span data-stu-id="91840-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="91840-175">由 Oem 啟用應用程式的單一映射部署的能力。</span><span class="sxs-lookup"><span data-stu-id="91840-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="91840-176">[企業的優點](benefits-of-mui-explained.md)： MUI 為企業提供的主要優點是能夠透過單一安裝，在全球推出、支援及維護相同的多語系映射。</span><span class="sxs-lookup"><span data-stu-id="91840-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="91840-177">另一個重要的勝利是能夠支援多語系桌面，以提供與不同語言喜好設定的流暢互動。</span><span class="sxs-lookup"><span data-stu-id="91840-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="91840-178">[Oem 的優點](benefits-of-mui-explained.md)： oem 的主要優點是 MUI 啟用的單一映射安裝，支援多種語言，可讓您更有效地管理清查。</span><span class="sxs-lookup"><span data-stu-id="91840-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="91840-179">Oem 也受益于應用程式開發的 MUI 支援，因為它可讓它們在映射上提供加值應用程式，同時從單一映射安裝獲益，只要這些應用程式已啟用 MUI 即可。</span><span class="sxs-lookup"><span data-stu-id="91840-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 




