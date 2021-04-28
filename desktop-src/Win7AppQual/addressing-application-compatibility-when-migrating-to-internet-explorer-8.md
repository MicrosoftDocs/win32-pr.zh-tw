---
description: 在遷移至 Internet Explorer 8 時解決應用程式相容性問題
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: 在遷移至 Internet Explorer 8 時解決應用程式相容性問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24fb4b0cbfb946f2385ddbd13ddc697987e659d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088766"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="1dcfb-103">在遷移至 Internet Explorer 8 時解決應用程式相容性問題</span><span class="sxs-lookup"><span data-stu-id="1dcfb-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="1dcfb-104">本節概述如何測試應用程式相容性問題，以及如何在 Windows Internet Explorer 8 的 web 應用程式中解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="1dcfb-105">下列主題描述 Internet Explorer 8 的變更，以及用來確保應用程式相容性的工具和技術。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="1dcfb-106">區段</span><span class="sxs-lookup"><span data-stu-id="1dcfb-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="1dcfb-107">描述</span><span class="sxs-lookup"><span data-stu-id="1dcfb-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dcfb-108">簡介</span><span class="sxs-lookup"><span data-stu-id="1dcfb-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="1dcfb-109">提供 Internet Explorer 8 相容性考慮的總覽。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="1dcfb-110">瞭解應用程式相容性挑戰</span><span class="sxs-lookup"><span data-stu-id="1dcfb-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="1dcfb-111">提供有關 Internet Explorer 8 相容性的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="1dcfb-112">Web 標準和應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="1dcfb-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="1dcfb-113">提供有關 web 標準為何重要的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="1dcfb-114">設計影響瀏覽器相容性的更新</span><span class="sxs-lookup"><span data-stu-id="1dcfb-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="1dcfb-115">提供影響相容性之設計更新的主題資訊。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="1dcfb-116">修正 Web 應用程式和附加元件的相容性問題</span><span class="sxs-lookup"><span data-stu-id="1dcfb-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="1dcfb-117">提供解決 web 應用程式與附加元件相容性問題的建議。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="1dcfb-118">用於調試 Web 應用程式和附加元件的工具</span><span class="sxs-lookup"><span data-stu-id="1dcfb-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="1dcfb-119">列出可用於調試 web 應用程式和附加元件的工具。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="1dcfb-120">附錄1： Internet Explorer 6 至 Internet Explorer 8 瀏覽器變更</span><span class="sxs-lookup"><span data-stu-id="1dcfb-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="1dcfb-121">列出 Microsoft Internet Explorer 6 到 Internet Explorer 8 的變更。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="1dcfb-122">附錄2：測試腳本案例</span><span class="sxs-lookup"><span data-stu-id="1dcfb-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="1dcfb-123">列出測試網站相容性的建議案例。</span><span class="sxs-lookup"><span data-stu-id="1dcfb-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



