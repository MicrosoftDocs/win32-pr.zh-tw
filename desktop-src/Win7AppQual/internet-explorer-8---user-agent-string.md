---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-使用者代理程式字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea44572f32e252a4e1d4dc2209e411834c12d4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314791"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="aa7d3-103">Internet Explorer 8-使用者代理程式字串</span><span class="sxs-lookup"><span data-stu-id="aa7d3-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="aa7d3-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="aa7d3-104">Affected Platforms</span></span>

 <span data-ttu-id="aa7d3-105">**客戶** 端-windows XP、windows Vista、windows 7</span><span class="sxs-lookup"><span data-stu-id="aa7d3-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="aa7d3-106">**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa7d3-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="aa7d3-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="aa7d3-107">Feature Impact</span></span>

<span data-ttu-id="aa7d3-108">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="aa7d3-108">**Severity** - Medium</span></span>  
<span data-ttu-id="aa7d3-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="aa7d3-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="aa7d3-110">描述</span><span class="sxs-lookup"><span data-stu-id="aa7d3-110">Description</span></span>

<span data-ttu-id="aa7d3-111">使用者代理字串是 Internet Explorer 的識別碼，可提供其版本和其他屬性的相關資料給 web 伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="aa7d3-112">許多 web 應用程式都依賴和操作 IE 使用者代理字串。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="aa7d3-113">這樣做並相依于較早的版本號碼將會受到影響。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="aa7d3-114">使用者代理程式字串現在包含字串 ' Trident/4.0 '，以便在 Internet Explorer 7 相容性檢視中執行時，允許 Internet Explorer 7 的使用者代理程式字串和 Internet Explorer 8 的使用者代理程式字串之間的差異。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="aa7d3-115">如需詳細資訊，請參閱瞭解使用者代理字串。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="aa7d3-116">影響的表現</span><span class="sxs-lookup"><span data-stu-id="aa7d3-116">Manifestation of Impact</span></span>

<span data-ttu-id="aa7d3-117">有兩個受影響的區域：</span><span class="sxs-lookup"><span data-stu-id="aa7d3-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="aa7d3-118">明確檢查使用者代理程式字串並不支援 Internet Explorer 8 使用者代理程式字串的網頁可能無法正常執行。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="aa7d3-119">在大部分的情況下，這表示頁面將會封鎖使用者嘗試存取的內容，或顯示不正確或格式不正確的內容。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="aa7d3-120">裝載 Trident (查看裝載和重複使用) 的應用程式，會使用 Web 選擇性元件預設為 Internet Explorer 7，但無法存取 Internet Explorer 8 功能。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="aa7d3-121">解決方法</span><span class="sxs-lookup"><span data-stu-id="aa7d3-121">Solution</span></span>

<span data-ttu-id="aa7d3-122">確定您的應用程式在使用者代理程式字串中正確處理新的 ' MSIE 8.0 ' 版本。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="aa7d3-123">您也可以根據 Internet Explorer 7，加入宣告這些應用程式的 Internet Explorer 7 相容性檢視。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="aa7d3-124">這可以透過中繼標記來完成。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-124">This can be done with meta tags.</span></span> <span data-ttu-id="aa7d3-125">如需詳細資訊，請參閱瞭解使用者代理字串的討論。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="aa7d3-126">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="aa7d3-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="aa7d3-127">在 Windows Vista 或 Windows XP 的 Internet Explorer 8 環境中執行您的應用程式和網頁，以確保它們會以預期的方式運作。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="aa7d3-128">或者，您可以使用應用程式相容性工具組所提供的 Internet Explorer 相容性測試控管 (IECTT)  (ACT) 找出因安全性功能更新而可能發生的任何問題。</span><span class="sxs-lookup"><span data-stu-id="aa7d3-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="aa7d3-129">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="aa7d3-129">Links to Other Resources</span></span>

-   <span data-ttu-id="aa7d3-130">[瞭解使用者代理程式字串](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa7d3-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="aa7d3-131">Internet Explorer 8 User-Agent 字串</span><span class="sxs-lookup"><span data-stu-id="aa7d3-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="aa7d3-132">使用者代理程式字串和版本向量</span><span class="sxs-lookup"><span data-stu-id="aa7d3-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="aa7d3-133">[裝載和重複使用](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa7d3-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="aa7d3-134">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="aa7d3-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="aa7d3-135">[已知 Internet Explorer 安全性功能問題](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="aa7d3-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
