---
description: 多語系消費者介面 (MUI) 是一種技術，可為使用者提供全球化應用程式的當地語系化使用者介面，以及 Windows 作業系統中的使用者介面語言資源管理。
ms.assetid: 1982931c-fce9-418f-a35d-439b7b886fd9
title: 關於多語系消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2971533310878e40049c591ae6537e43aa4f666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985210"
---
# <a name="about-multilingual-user-interface"></a><span data-ttu-id="2c713-103">關於多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="2c713-103">About Multilingual User Interface</span></span>

<span data-ttu-id="2c713-104">多語系消費者介面 (MUI) 是一種技術，可為使用者提供全球化應用程式的當地語系化使用者介面，以及 Windows 作業系統中的使用者介面語言資源管理。</span><span class="sxs-lookup"><span data-stu-id="2c713-104">Multilingual User Interface (MUI) is a technology that provides users a localized user interface for globalized applications and user interface language resource management in the Windows operating system.</span></span> <span data-ttu-id="2c713-105">提供支援，可將 MUI 功能新增至全球化應用程式，以在 Windows Vista 和更新版本上執行，以及許多 Windows Vista 之前的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2c713-105">Support is provided for adding MUI functionality to globalized applications to run on Windows Vista and later, as well as many pre-Windows Vista operating systems.</span></span> <span data-ttu-id="2c713-106">MUI 當地語系化和資源管理模型可增強對全球化軟體的開發、測試和支援。</span><span class="sxs-lookup"><span data-stu-id="2c713-106">The MUI localization and resource management models enhance development, testing, and support for world-ready software.</span></span>

<span data-ttu-id="2c713-107">MUI 技術的功能包括：</span><span class="sxs-lookup"><span data-stu-id="2c713-107">Features of MUI technology include:</span></span>

-   <span data-ttu-id="2c713-108">簡化軟體當地語系化的語言管理。</span><span class="sxs-lookup"><span data-stu-id="2c713-108">Simplified language management for software localization.</span></span> <span data-ttu-id="2c713-109">MUI 允許根據使用者喜好設定，將作業系統的語言設定變更為支援的語言。</span><span class="sxs-lookup"><span data-stu-id="2c713-109">MUI allows the language settings for the operating system to be changed to a supported language according to user preferences.</span></span>
-   <span data-ttu-id="2c713-110">以語言資源檔中的應用程式程式碼二進位檔分割為基礎的創新資源技術。</span><span class="sxs-lookup"><span data-stu-id="2c713-110">An innovative resource technology based on the splitting of the application code binary from language resource files.</span></span> <span data-ttu-id="2c713-111">您可以新增其他語言的資源，而不需要重新編譯或重新連結您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c713-111">You can add resources for an additional language without needing to recompile or relink your application.</span></span> <span data-ttu-id="2c713-112">其他當地語系化的資源會變成選用的增益集。</span><span class="sxs-lookup"><span data-stu-id="2c713-112">Additional localized resources become optional add-ins.</span></span>
-   <span data-ttu-id="2c713-113"> (API) 的完整應用程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="2c713-113">Complete application programming interface (API).</span></span> <span data-ttu-id="2c713-114">Windows Vista 和更新版本會公開 MUI API，供您用來將 MUI 功能新增至全球化應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c713-114">Windows Vista and later expose the MUI API for you to use in adding MUI functionality to globalized applications.</span></span> <span data-ttu-id="2c713-115">語言管理功能可讓您的應用程式支援各種不同的使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="2c713-115">Language management functions enable your applications to support a wide variety of user interface languages.</span></span> <span data-ttu-id="2c713-116">此 API 也包含資源載入功能，可讓資源載入器載入 Windows Vista 和更新版本的資源，以及 Windows Vista 之前的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2c713-116">The API also includes resource loading functions that enable the resource loader to load resources on Windows Vista and later, as well as pre-Windows Vista operating systems.</span></span>
-   <span data-ttu-id="2c713-117">一組語言套件管理工具，可在國際部署映射管理中提供彈性。</span><span class="sxs-lookup"><span data-stu-id="2c713-117">A set of language pack management tools that provide flexibility in international deployment image management.</span></span> <span data-ttu-id="2c713-118">這些工具並非以開發人員為目標，因此不會涵蓋在 SDK 中。</span><span class="sxs-lookup"><span data-stu-id="2c713-118">These tools are not targeted at developers and thus are not covered in the SDK.</span></span> <span data-ttu-id="2c713-119">如需詳細資訊，請參閱 Technet 上提供的 Windows 自動化安裝套件。</span><span class="sxs-lookup"><span data-stu-id="2c713-119">More information can be found in the Windows Automated Installation Kit available on Technet.</span></span>

<span data-ttu-id="2c713-120">MUI 最明顯的優點是，多個使用者可以共用相同的工作站，並以不同的語言來查看使用者介面。</span><span class="sxs-lookup"><span data-stu-id="2c713-120">The most visible benefit of MUI is that multiple users can share the same workstation and view the user interface in different languages.</span></span> <span data-ttu-id="2c713-121">公司和 Oem 將受益于使用單一安裝來推出、支援及維護多語系映射所需的功能。</span><span class="sxs-lookup"><span data-stu-id="2c713-121">Corporations and OEMs will benefit from the capability they have to roll out, support, and maintain multilingual images with a single installation.</span></span> <span data-ttu-id="2c713-122">但是，MUI 的主要優點是開發、建立及服務應用程式時所獲得的效率。</span><span class="sxs-lookup"><span data-stu-id="2c713-122">But perhaps the main benefit of MUI comes in the efficiencies gained when developing, building and servicing your application.</span></span> <span data-ttu-id="2c713-123">您可以提供一個適用于所有平臺的核心功能二進位檔，其與 UI 語言無關，可大幅減少開發和測試工作。</span><span class="sxs-lookup"><span data-stu-id="2c713-123">You can ship one core functionality binary applicable to all platforms, independent of UI language, which significantly reduces development and testing efforts.</span></span> <span data-ttu-id="2c713-124">如果您必須發行更新或 service pack，則會套用至所有支援的語言，而不需要額外的工程工作。</span><span class="sxs-lookup"><span data-stu-id="2c713-124">If you have to issue an update or a service pack, it will apply to all supported languages with no additional engineering effort.</span></span> <span data-ttu-id="2c713-125">後續對其他語言的支援會成為當地語系化專案，而不是完整的軟體發展專案。</span><span class="sxs-lookup"><span data-stu-id="2c713-125">Later support for additional languages becomes a localization project instead of a full software development project.</span></span>

<span data-ttu-id="2c713-126">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="2c713-126">This section covers the following topics:</span></span>

-   [<span data-ttu-id="2c713-127">瞭解 MUI</span><span class="sxs-lookup"><span data-stu-id="2c713-127">Understanding MUI</span></span>](understanding-mui.md)
-   [<span data-ttu-id="2c713-128">MUI 的可用性</span><span class="sxs-lookup"><span data-stu-id="2c713-128">Availability of MUI</span></span>](availability-of-mui.md)
-   [<span data-ttu-id="2c713-129">MUI 資源管理</span><span class="sxs-lookup"><span data-stu-id="2c713-129">MUI Resource Management</span></span>](mui-resource-management.md)
-   [<span data-ttu-id="2c713-130">消費者介面語言管理</span><span class="sxs-lookup"><span data-stu-id="2c713-130">User Interface Language Management</span></span>](user-interface-language-management.md)
-   [<span data-ttu-id="2c713-131">開發 MUI 應用程式</span><span class="sxs-lookup"><span data-stu-id="2c713-131">Development of MUI Applications</span></span>](development-of-mui-applications.md)
-   [<span data-ttu-id="2c713-132">應用程式部署</span><span class="sxs-lookup"><span data-stu-id="2c713-132">Application Deployment</span></span>](application-deployment.md)

 

 



