---
description: 使用多語系消費者介面
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: 使用多語系消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195432"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="6da94-103">使用多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="6da94-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="6da94-104">本節說明如何使用多語系消費者介面 (MUI) 功能來設計和執行您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6da94-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="6da94-105">以下是在應用程式生命週期的大部分階段中將扮演的 MUI 技術層面。</span><span class="sxs-lookup"><span data-stu-id="6da94-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="6da94-106">應用程式開發，包括資源準備、應用程式語言喜好設定的設定、尋找和載入資源</span><span class="sxs-lookup"><span data-stu-id="6da94-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="6da94-107">建立和當地語系化應用程式</span><span class="sxs-lookup"><span data-stu-id="6da94-107">Building and localizing the application</span></span>
-   <span data-ttu-id="6da94-108">部署應用程式</span><span class="sxs-lookup"><span data-stu-id="6da94-108">Deploying the application</span></span>

<span data-ttu-id="6da94-109">以下是設計和執行 MUI 應用程式時要考慮的一些問題。</span><span class="sxs-lookup"><span data-stu-id="6da94-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="6da94-110">應用程式將支援哪些 Windows 版本？</span><span class="sxs-lookup"><span data-stu-id="6da94-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="6da94-111">應用程式在哪些語言中會當地語系化？</span><span class="sxs-lookup"><span data-stu-id="6da94-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="6da94-112">應用程式語言設定是否應該一律遵循作業系統的語言設定，或應用程式使用者是否可以設定特定語言？</span><span class="sxs-lookup"><span data-stu-id="6da94-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="6da94-113">應用程式使用何種類型的使用者介面資源，以及它們的儲存位置為何？</span><span class="sxs-lookup"><span data-stu-id="6da94-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="6da94-114">本節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="6da94-114">This section includes the following topics.</span></span> <span data-ttu-id="6da94-115">描述會假設以 Windows Vista 和更新版本為目標的 MUI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6da94-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="6da94-116">此應用程式的資源是 Win32 資源，其特定語言的資源和可執行程式碼位於不同的 Win32 PE 檔案中。</span><span class="sxs-lookup"><span data-stu-id="6da94-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="6da94-117">針對 Windows Vista 前版作業系統或不同資源類型的支援，會視需要新增特殊的考慮。</span><span class="sxs-lookup"><span data-stu-id="6da94-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="6da94-118">準備資源</span><span class="sxs-lookup"><span data-stu-id="6da94-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="6da94-119">設定應用程式語言喜好設定</span><span class="sxs-lookup"><span data-stu-id="6da94-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="6da94-120">尋找 Win32 PE 資源</span><span class="sxs-lookup"><span data-stu-id="6da94-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="6da94-121">尋找非 Win32 PE 資源</span><span class="sxs-lookup"><span data-stu-id="6da94-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="6da94-122">當地語系化資源和建立應用程式</span><span class="sxs-lookup"><span data-stu-id="6da94-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="6da94-123">MUI：系統設定應用程式範例</span><span class="sxs-lookup"><span data-stu-id="6da94-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="6da94-124">MUI： (Windows Vista) 的 Application-Specific 設定範例 </span><span class="sxs-lookup"><span data-stu-id="6da94-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="6da94-125">MUI： (Windows Vista 之前的 Application-Specific 設定範例) </span><span class="sxs-lookup"><span data-stu-id="6da94-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



