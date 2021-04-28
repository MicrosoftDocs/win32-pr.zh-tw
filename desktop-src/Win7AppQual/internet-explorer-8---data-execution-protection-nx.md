---
description: Internet Explorer 8-資料執行防止/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-資料執行防止/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088246"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="00e1d-103">Internet Explorer 8-資料執行防止/NX</span><span class="sxs-lookup"><span data-stu-id="00e1d-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="00e1d-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="00e1d-104">Affected Platforms</span></span>

 <span data-ttu-id="00e1d-105">**客戶** 端-windows XP、windows Vista、windows 7</span><span class="sxs-lookup"><span data-stu-id="00e1d-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="00e1d-106">**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00e1d-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="00e1d-107">Internet Explorer 8 將在具有最新 service pack 的作業系統上執行時，啟用 DEP/NX 保護。</span><span class="sxs-lookup"><span data-stu-id="00e1d-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="00e1d-108">在 Internet Explorer 8 中，windows XP SP3、Windows Server 2003 SP3、Windows Vista SP1 和 Windows Server 2008 都預設啟用 DEP/NX。</span><span class="sxs-lookup"><span data-stu-id="00e1d-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="00e1d-109">功能影響</span><span class="sxs-lookup"><span data-stu-id="00e1d-109">Feature Impact</span></span>

<span data-ttu-id="00e1d-110">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="00e1d-110">**Severity** - Medium</span></span>  
<span data-ttu-id="00e1d-111">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="00e1d-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="00e1d-112">一般來說，在 Internet Explorer 中執行且與 DEP/NX 不相容的任何應用程式都會在啟動時損毀，且無法運作。</span><span class="sxs-lookup"><span data-stu-id="00e1d-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="00e1d-113">如果安裝了不相容于 DEP/NX 的附加元件，Internet Explorer 可能會在啟動時損毀。</span><span class="sxs-lookup"><span data-stu-id="00e1d-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="00e1d-114">Description</span><span class="sxs-lookup"><span data-stu-id="00e1d-114">Description</span></span>

<span data-ttu-id="00e1d-115">DEP/NX 是一種安全性功能，可協助減輕記憶體相關弱點。</span><span class="sxs-lookup"><span data-stu-id="00e1d-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="00e1d-116">從 Internet Explorer 8，所有 Internet Explorer 進程預設都會啟用 DEP/NX 功能。</span><span class="sxs-lookup"><span data-stu-id="00e1d-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="00e1d-117">影響的表現</span><span class="sxs-lookup"><span data-stu-id="00e1d-117">Manifestation of Impact</span></span>

<span data-ttu-id="00e1d-118">Windows 核心會監視程式的執行。</span><span class="sxs-lookup"><span data-stu-id="00e1d-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="00e1d-119">如果核心偵測到嘗試從未標記為可執行檔的記憶體頁面執行程式碼，則核心會停止執行程式，並產生「損毀」。</span><span class="sxs-lookup"><span data-stu-id="00e1d-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="00e1d-120">這是一項安全性措施，可協助確保記憶體相關弱點 (例如，應用程式中的緩衝區溢位) 無法被惡意探索，以執行任意程式碼。</span><span class="sxs-lookup"><span data-stu-id="00e1d-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="00e1d-121">End-User 風險降低</span><span class="sxs-lookup"><span data-stu-id="00e1d-121">End-User Mitigation</span></span>

-   <span data-ttu-id="00e1d-122">安裝較新版本的附加元件或與 DEP/NX 相容的 framework。</span><span class="sxs-lookup"><span data-stu-id="00e1d-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="00e1d-123">以系統管理員的身分執行 Internet Explorer，然後在 [**網際網路選項**] 的 [選項] 索引標籤上，使用 [**啟用記憶體保護] 來防止線上攻擊** 核取方塊停用 DEP/NX  /   。</span><span class="sxs-lookup"><span data-stu-id="00e1d-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="00e1d-124">開發人員解決方案</span><span class="sxs-lookup"><span data-stu-id="00e1d-124">Developer Solution</span></span>

<span data-ttu-id="00e1d-125">使用與 DEP 相容的最新 framework 版本來編譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="00e1d-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="00e1d-126">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="00e1d-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="00e1d-127">使用/NXCOMPAT 連結器選項來指出 DEP/NX 相容性</span><span class="sxs-lookup"><span data-stu-id="00e1d-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="00e1d-128">將您的程式碼加入其他可用的防禦機制，例如 stack 防禦 (/GS) 、安全例外狀況處理 (/SafeSEH) 和 ASLR (/DynamicBase) </span><span class="sxs-lookup"><span data-stu-id="00e1d-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="00e1d-129">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="00e1d-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="00e1d-130">在 Windows Vista SP1 或更新版本上使用最新發行的 Internet Explorer 版本，以啟用 DEP/NX 測試您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="00e1d-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="00e1d-131">啟用 DEP/NX 選項之後，請在 Windows Vista 上使用 Internet Explorer 7 進行測試。</span><span class="sxs-lookup"><span data-stu-id="00e1d-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="00e1d-132">若要啟用 Internet Explorer 7 的 DEP/NX，請以系統管理員身分執行 Internet Explorer，然後在 [工具 > 的 [網際網路選項] > [Advanced] 索引標籤中，設定適當的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="00e1d-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="00e1d-133">使用應用程式相容性工具組所提供的 Internet Explorer 相容性測試控管 (IECTT)  (ACT) 找出因 DEP/NX 變更而產生的任何潛在問題。</span><span class="sxs-lookup"><span data-stu-id="00e1d-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="00e1d-134">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="00e1d-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="00e1d-135">Internet Explorer 8 安全性第 I 部： DEP/NX 記憶體保護</span><span class="sxs-lookup"><span data-stu-id="00e1d-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="00e1d-136">資料執行防止</span><span class="sxs-lookup"><span data-stu-id="00e1d-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="00e1d-137">新增至 Windows Vista SP1、Windows XP SP3 和 Windows Server 2008 R2 的新 NX Api</span><span class="sxs-lookup"><span data-stu-id="00e1d-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="00e1d-138">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="00e1d-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="00e1d-139">[已知 Internet Explorer 安全性功能問題](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="00e1d-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
