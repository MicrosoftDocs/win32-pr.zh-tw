---
description: '遠端桌面服務 (Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) '
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: '遠端桌面服務 (Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116116"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="fa050-103">遠端桌面服務 (Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) </span><span class="sxs-lookup"><span data-stu-id="fa050-103">Remote Desktop Services (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fa050-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="fa050-104">Affected Platforms</span></span>

<span data-ttu-id="fa050-105">**伺服器** – windows server 2008 \| Windows server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa050-105">**Servers** – Windows Server 2008 \| Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="fa050-106">Description</span><span class="sxs-lookup"><span data-stu-id="fa050-106">Description</span></span>

<span data-ttu-id="fa050-107">遠端桌面服務 (之前稱為終端機服務) 可讓多個並行使用者存取 Windows Server，以使用 Microsoft 「展示虛擬化」技術來提供應用程式和資料裝載服務。</span><span class="sxs-lookup"><span data-stu-id="fa050-107">Remote Desktop Services (formerly known as Terminal Services) allows multiple concurrent users to access Windows Server in order to provide application and data hosting services using Microsoft "Presentation Virtualization" technology.</span></span>

<span data-ttu-id="fa050-108">雖然大部分的32位和64位應用程式都是以 Windows 遠端桌面服務的形式執行，但因為平臺 (多使用者環境中的差異、多位使用者的平行存取，以及) 的平行存取，所以許多其他應用程式不會如預期般執行。</span><span class="sxs-lookup"><span data-stu-id="fa050-108">While most 32-bit and 64-bit applications run as is on Windows Remote Desktop Services, several others do not perform as expected due to the difference in the platform (multi-user environment, concurrent access by multiple users, and so on).</span></span>

<span data-ttu-id="fa050-109">如需有關應用程式品質的詳細資訊，請參閱 *適用于終端機服務的應用程式就緒* 白皮書。</span><span class="sxs-lookup"><span data-stu-id="fa050-109">For further information regarding application quality, please read the *Application Readiness for Terminal Services* white paper.</span></span> <span data-ttu-id="fa050-110">造訪遠端桌面服務產品頁面，TS TechNet 網站深入瞭解遠端桌面服務。</span><span class="sxs-lookup"><span data-stu-id="fa050-110">Visit the Remote Desktop Services product page and the TS TechNet websites learn more about Remote Desktop Services.</span></span> <span data-ttu-id="fa050-111">若要深入瞭解如何開發遠端桌面服務的應用程式，請參閱 *終端機服務程式設計指導方針*。</span><span class="sxs-lookup"><span data-stu-id="fa050-111">To learn more about developing applications for Remote Desktop Services, review the *Terminal Services Programming Guidelines*.</span></span> <span data-ttu-id="fa050-112"> (這些資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="fa050-112">(These resources may not be available in some languages and countries/regions.)</span></span>

## <a name="manifestation-of-impacts-and-their-mitigations"></a><span data-ttu-id="fa050-113">影響因素及其緩和措施的表現</span><span class="sxs-lookup"><span data-stu-id="fa050-113">Manifestation of Impacts and Their Mitigations</span></span>

<span data-ttu-id="fa050-114">Windows 7 的三項變更會影響遠端桌面服務上的應用程式：</span><span class="sxs-lookup"><span data-stu-id="fa050-114">Three changes in Windows 7 affect applications on Remote Desktop Services:</span></span>

-   <span data-ttu-id="fa050-115">Windows Server 2008 R2 僅限64位</span><span class="sxs-lookup"><span data-stu-id="fa050-115">Windows Server 2008 R2 is 64-bit only</span></span>
-   <span data-ttu-id="fa050-116">每一會話 IP 虛擬化</span><span class="sxs-lookup"><span data-stu-id="fa050-116">Per-session IP Virtualization</span></span>
-   <span data-ttu-id="fa050-117">以 MSI 為基礎的部署–使用者特定的金鑰</span><span class="sxs-lookup"><span data-stu-id="fa050-117">MSI-based deployments – User-specific keys</span></span>

<span data-ttu-id="fa050-118">**僅限64位 Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fa050-118">**64-bit Only Windows Server 2008 R2**</span></span>

<span data-ttu-id="fa050-119">針對32位伺服器撰寫的應用程式將以 WoW 模式執行，而不是在 Windows Server 2008 R2 上以原生方式執行，因此遠端桌面服務。</span><span class="sxs-lookup"><span data-stu-id="fa050-119">Applications written for 32-bit server will run in WoW mode and not natively on the Windows Server 2008 R2 or, hence, on Remote Desktop Services.</span></span> <span data-ttu-id="fa050-120">如需詳細資訊，請參閱僅限 Windows 7 64-Bit 主題。</span><span class="sxs-lookup"><span data-stu-id="fa050-120">See the Windows 7 64-Bit Only topic for details.</span></span>

<span data-ttu-id="fa050-121">*僅限64位 Windows Server 2008 R2 的緩和措施*</span><span class="sxs-lookup"><span data-stu-id="fa050-121">*Mitigations for 64-bit only Windows Server 2008 R2*</span></span>

<span data-ttu-id="fa050-122">大部分針對32位撰寫的應用程式在 WoW 模式下將繼續正常運作。</span><span class="sxs-lookup"><span data-stu-id="fa050-122">Most applications written for 32-bit will continue to work as normal in WoW mode.</span></span> <span data-ttu-id="fa050-123">針對 Windows 7 遠端桌面服務撰寫的任何新應用程式，都應該針對64位平臺上的部署進行開發和測試。</span><span class="sxs-lookup"><span data-stu-id="fa050-123">Any new applications written for Windows 7 Remote Desktop Services should be developed and tested for deployment on 64-bit platforms.</span></span>

<span data-ttu-id="fa050-124">**IP 虛擬化**</span><span class="sxs-lookup"><span data-stu-id="fa050-124">**IP Virtualization**</span></span>

<span data-ttu-id="fa050-125">遠端桌面 IP 虛擬可讓使用者在每個會話或個別程式上，將 IP 位址指派給遠端桌面連線：</span><span class="sxs-lookup"><span data-stu-id="fa050-125">Remote Desktop IP Virtualization allows the user to assign IP addresses to remote desktop connections on a per-session or per-program basis:</span></span>

-   <span data-ttu-id="fa050-126">如果您在每個會話上指派 IP 位址，則所有應用程式都會使用會話 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fa050-126">If you assign IP addresses on a per-session basis, all of the applications will use the session IP address.</span></span>
-   <span data-ttu-id="fa050-127">如果您以個別程式為基礎指派 IP 位址，則只有指定的應用程式會使用會話 IP 位址，而且會話中的其餘應用程式不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="fa050-127">If you assign IP addresses on a per-program basis, only the specified applications will use the session IP address and the remaining applications in the session will not be affected.</span></span>
-   <span data-ttu-id="fa050-128">如果您指派多個程式的 IP 位址，它們會共用會話 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fa050-128">If you assign IP addresses for multiple programs, they will share a session IP address.</span></span>
-   <span data-ttu-id="fa050-129">如果電腦上有一個以上的網路介面卡，您也必須選擇其中一個網路介面卡進行遠端桌面 IP 虛擬。</span><span class="sxs-lookup"><span data-stu-id="fa050-129">If you have more than one network adapter on the computer, you must also choose one of them for Remote Desktop IP Virtualization.</span></span>

<span data-ttu-id="fa050-130">*IP 虛擬化的緩和措施*</span><span class="sxs-lookup"><span data-stu-id="fa050-130">*Mitigations for IP Virtualization*</span></span>

<span data-ttu-id="fa050-131">某些程式需要每個應用程式實例都有唯一的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fa050-131">Some programs require a unique IP address for each instance of the application.</span></span> <span data-ttu-id="fa050-132">在 Windows Server 2008 R2 之前，遠端桌面伺服器上的每個會話都會共用相同的 IP 位址，而導致這些應用程式的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="fa050-132">Prior to Windows Server 2008 R2, every session on a remote desktop server shared the same IP address, resulting in compatibility issues for these applications.</span></span> <span data-ttu-id="fa050-133">遠端桌面 IP 虛擬可讓這些應用程式在遠端桌面伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="fa050-133">Remote Desktop IP Virtualization allows these applications to run on a Remote Desktop Server.</span></span>

<span data-ttu-id="fa050-134">**以 MSI 為基礎的部署**</span><span class="sxs-lookup"><span data-stu-id="fa050-134">**MSI-based Deployments**</span></span>

<span data-ttu-id="fa050-135">Microsoft Installer RDS 相容性是 Windows Server 2008 R2 中遠端桌面服務隨附的新功能。</span><span class="sxs-lookup"><span data-stu-id="fa050-135">Microsoft Installer RDS Compatibility is a new feature included with Remote Desktop Services in Windows Server 2008 R2.</span></span> <span data-ttu-id="fa050-136">利用 Windows Server 2008 R2 中的遠端桌面服務，每個使用者的應用程式安裝會由遠端桌面伺服器排入佇列，然後由 Microsoft 安裝程式進行處理。</span><span class="sxs-lookup"><span data-stu-id="fa050-136">With Remote Desktop Services in Windows Server 2008 R2, per-user application installations are queued by the Remote Desktop Server and then handled by the Microsoft Installer.</span></span>

<span data-ttu-id="fa050-137">在 Windows Server 2008 R2 中，您可以在遠端桌面伺服器上安裝程式，就像在本機桌面上安裝程式一樣。</span><span class="sxs-lookup"><span data-stu-id="fa050-137">In Windows Server 2008 R2, you can install a program on the Remote Desktop Server just as you would install the program on a local desktop.</span></span> <span data-ttu-id="fa050-138">不過，請確定您為所有使用者安裝程式，並在遠端桌面伺服器本機上安裝程式的所有元件。</span><span class="sxs-lookup"><span data-stu-id="fa050-138">Ensure, however, that you install the program for all users and install all components of the program locally on the Remote Desktop Server.</span></span>

<span data-ttu-id="fa050-139">*以 MSI 為基礎的部署緩和措施*</span><span class="sxs-lookup"><span data-stu-id="fa050-139">*Mitigations for MSI based Deployments*</span></span>

<span data-ttu-id="fa050-140">在遠端桌面服務 Windows Server 2008 R2 版之前，Windows 一次只支援一個 Windows Installer 安裝。</span><span class="sxs-lookup"><span data-stu-id="fa050-140">Prior to the Windows Server 2008 R2 version of Remote Desktop Services, Windows supported only one Windows Installer installation at a time.</span></span> <span data-ttu-id="fa050-141">對於需要個別使用者設定的應用程式（例如 Microsoft Office Word），系統管理員必須先安裝應用程式，而應用程式開發人員需要在遠端桌面用戶端和遠端桌面工作階段主機上測試這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="fa050-141">For applications that required per-user configurations, such as Microsoft Office Word, an administrator needed to pre-install the application, and application developers needed to test these applications on both the remote desktop client and the Remote Desktop Session Host.</span></span> <span data-ttu-id="fa050-142">Windows Installer RDS 相容性功能可讓您同時識別和安裝多個使用者遺失的每個使用者設定，並讓應用程式安裝體驗在類似本機桌面上的遠端桌面伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fa050-142">Windows Installer RDS Compatibility feature allows identifying and installing missing per-user configurations for multiple users simultaneously and makes the application installation experience on Remote Desktop Server similar to that on a local desktop.</span></span>

<span data-ttu-id="fa050-143">**啟用 [遠端桌面服務](../termserv/terminal-services-portal.md) 角色的 Windows Server 2008 R2：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="fa050-143">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="fa050-144">如果啟用[遠端桌面服務](../termserv/terminal-services-portal.md)角色，使用[MsiEmbeddedChainer 資料表](../msi/msiembeddedchainer-table.md)的多個套件安裝將會失敗。</span><span class="sxs-lookup"><span data-stu-id="fa050-144">A multiple package installation using the [MsiEmbeddedChainer table](../msi/msiembeddedchainer-table.md) fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fa050-145">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="fa050-145">Links to Other Resources</span></span>

-   [<span data-ttu-id="fa050-146">終端機服務程式設計指導方針</span><span class="sxs-lookup"><span data-stu-id="fa050-146">Terminal Services Programming Guidelines</span></span>](../termserv/terminal-services-programming-guidelines.md)
-   [<span data-ttu-id="fa050-147">終端機服務產品首頁</span><span class="sxs-lookup"><span data-stu-id="fa050-147">Terminal Services product home page</span></span>](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [<span data-ttu-id="fa050-148">適用于終端機服務的應用程式就緒白皮書</span><span class="sxs-lookup"><span data-stu-id="fa050-148">Application Readiness for Terminal Services white paper</span></span>](/collaborate/connect-redirect)

> [!Note]  
> <span data-ttu-id="fa050-149">這些資源可能無法在某些語言及國家/地區中使用。</span><span class="sxs-lookup"><span data-stu-id="fa050-149">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
