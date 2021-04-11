---
description: .
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: 在遷移至 Internet Explorer 8 時解決應用程式相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab869be07e5578d265db2e8e85147c213e1e17e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195239"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="ce13e-103">在遷移至 Internet Explorer 8 時解決應用程式相容性問題</span><span class="sxs-lookup"><span data-stu-id="ce13e-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="ce13e-104">本節概述如何測試應用程式相容性問題，以及如何在 Windows Internet Explorer 8 的 web 應用程式中解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="ce13e-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="ce13e-105">下列主題描述 Internet Explorer 8 的變更，以及用來確保應用程式相容性的工具和技術。</span><span class="sxs-lookup"><span data-stu-id="ce13e-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="ce13e-106">區段</span><span class="sxs-lookup"><span data-stu-id="ce13e-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="ce13e-107">描述</span><span class="sxs-lookup"><span data-stu-id="ce13e-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce13e-108">簡介</span><span class="sxs-lookup"><span data-stu-id="ce13e-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="ce13e-109">提供 Internet Explorer 8 相容性考慮的總覽。</span><span class="sxs-lookup"><span data-stu-id="ce13e-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="ce13e-110">瞭解應用程式相容性挑戰</span><span class="sxs-lookup"><span data-stu-id="ce13e-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="ce13e-111">提供有關 Internet Explorer 8 相容性的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="ce13e-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="ce13e-112">Web 標準和應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="ce13e-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="ce13e-113">提供有關 web 標準為何重要的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="ce13e-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="ce13e-114">設計影響瀏覽器相容性的更新</span><span class="sxs-lookup"><span data-stu-id="ce13e-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="ce13e-115">提供影響相容性之設計更新的主題資訊。</span><span class="sxs-lookup"><span data-stu-id="ce13e-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="ce13e-116">修正 Web 應用程式和附加元件的相容性問題</span><span class="sxs-lookup"><span data-stu-id="ce13e-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="ce13e-117">提供解決 web 應用程式與附加元件相容性問題的建議。</span><span class="sxs-lookup"><span data-stu-id="ce13e-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="ce13e-118">用於調試 Web 應用程式和附加元件的工具</span><span class="sxs-lookup"><span data-stu-id="ce13e-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="ce13e-119">列出可用於調試 web 應用程式和附加元件的工具。</span><span class="sxs-lookup"><span data-stu-id="ce13e-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="ce13e-120">附錄1： Internet Explorer 6 至 Internet Explorer 8 瀏覽器變更</span><span class="sxs-lookup"><span data-stu-id="ce13e-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="ce13e-121">列出 Microsoft Internet Explorer 6 到 Internet Explorer 8 的變更。</span><span class="sxs-lookup"><span data-stu-id="ce13e-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="ce13e-122">附錄2：測試腳本案例</span><span class="sxs-lookup"><span data-stu-id="ce13e-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="ce13e-123">列出測試網站相容性的建議案例。</span><span class="sxs-lookup"><span data-stu-id="ce13e-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



