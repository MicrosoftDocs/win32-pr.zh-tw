---
title: Microsoft 平臺就緒測試控管
description: Microsoft 平臺就緒測試控管
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683214"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="6a0e9-103">Microsoft 平臺就緒測試控管</span><span class="sxs-lookup"><span data-stu-id="6a0e9-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="6a0e9-104">平台</span><span class="sxs-lookup"><span data-stu-id="6a0e9-104">Platform</span></span>

 <span data-ttu-id="6a0e9-105">**伺服器** – windows server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a0e9-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="6a0e9-106">Description</span><span class="sxs-lookup"><span data-stu-id="6a0e9-106">Description</span></span>

<span data-ttu-id="6a0e9-107">Microsoft Platform Ready (MPR) 測試控管可用於平臺應用程式的就緒程度，以及驗證 Windows Server 2012 和 Windows Server 2012 R2 應用程式的認證需求是否符合規範。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="6a0e9-108">Microsoft 強烈建議您將 MPR 測試控管併入軟體組建和測試程式中，藉此確保在應用程式發行到市場之前，平臺已做好準備。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="6a0e9-109">MPR 測試控管也是建議的工具，用來測試企業營運應用程式，以及評估伺服器產品的平臺相容性，然後再進行購買決策。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a0e9-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a0e9-110">Requirements</span></span>

<span data-ttu-id="6a0e9-111">MPR 測試控管包含的自動化測試：</span><span class="sxs-lookup"><span data-stu-id="6a0e9-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="6a0e9-112">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6a0e9-112">Windows Installer</span></span>
-   <span data-ttu-id="6a0e9-113">設定和主要功能</span><span class="sxs-lookup"><span data-stu-id="6a0e9-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="6a0e9-114">驅動程式和安全性</span><span class="sxs-lookup"><span data-stu-id="6a0e9-114">Drivers and Security</span></span>
-   <span data-ttu-id="6a0e9-115">最佳做法</span><span class="sxs-lookup"><span data-stu-id="6a0e9-115">Best Practices</span></span>

<span data-ttu-id="6a0e9-116">針對大部分的伺服器應用程式，自行測試及提交結果應該花費2小時或更少的時間。更複雜的應用程式可能需要大約4小時的時間。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="6a0e9-117">所有驅動程式必須個別通過 Windows 硬體認證測試，並由 Microsoft 為 Windows Server 2012 進行簽署。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="6a0e9-118">使用方式</span><span class="sxs-lookup"><span data-stu-id="6a0e9-118">Usage</span></span>

<span data-ttu-id="6a0e9-119">若要測試您的應用程式：</span><span class="sxs-lookup"><span data-stu-id="6a0e9-119">To test your apps:</span></span>

1.  <span data-ttu-id="6a0e9-120">安裝最新的 Windows Server 2012 最小設定 (完整伺服器 GUI、基本伺服器介面或 Server Core) ，視您的應用程式需求而來。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="6a0e9-121">檢查認證需求。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="6a0e9-122">在乾淨的系統上，以完整的 UI 模式或命令列模式執行 MPR 測試控管。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="6a0e9-123">完成自我引導的測試程式。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="6a0e9-124">查看結果，並視需要修正您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="6a0e9-125">登入，並將成功的結果上傳至 Microsoft Platform Ready 入口網站，以在標誌的 Windows Server Catalog 和使用中列出。</span><span class="sxs-lookup"><span data-stu-id="6a0e9-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="6a0e9-126">資源</span><span class="sxs-lookup"><span data-stu-id="6a0e9-126">Resources</span></span>

-   [<span data-ttu-id="6a0e9-127">Windows Server 應用程式認證方案的需求</span><span class="sxs-lookup"><span data-stu-id="6a0e9-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="6a0e9-128">Microsoft Platform Ready (MPR) 測試控管</span><span class="sxs-lookup"><span data-stu-id="6a0e9-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="6a0e9-129">Windows Server 2012 應用程式認證計畫</span><span class="sxs-lookup"><span data-stu-id="6a0e9-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="6a0e9-130">Windows Server 標誌意見反應</span><span class="sxs-lookup"><span data-stu-id="6a0e9-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 