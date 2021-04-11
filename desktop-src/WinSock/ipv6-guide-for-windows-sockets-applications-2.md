---
description: 本指南提供您所需的資訊，讓您的 Microsoft Windows 應用程式能夠使用新一代的網際網路通訊協定第6版 (IPv6) 。
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: 適用于 Windows 通訊端應用程式的 IPv6 指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113053"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="e0b8f-103">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="e0b8f-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="e0b8f-104">本指南提供您所需的資訊，讓您的 Microsoft Windows 應用程式能夠使用新一代的網際網路通訊協定第6版 (IPv6) 。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="e0b8f-105">將 IPv6 功能新增至您的應用程式不一定是移植進程。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="e0b8f-106">若要移植應用程式，建議將程式碼修改為在不同平臺上運作，這表示離開先前的平臺。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="e0b8f-107">本指南的結構是專門用來協助將 IPv6 功能新增至應用程式，同時保留 IPv4 功能。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="e0b8f-108">本指南將討論新增 IPv6 功能的相關問題，然後以最受轉換影響的開發領域為目標。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="e0b8f-109">每個區域都可以完整說明要注意的陷阱、建議避免的策略，以及如何充分利用新的 [Windows 通訊端 2](what-s-new-for-windows-sockets-2.md) 程式設計項目 (函式和結構) 的秘訣。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="e0b8f-110">如需 IPv6 的詳細資訊，請參閱 [Ipv6 支援](ipv6-support-2.md)。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="e0b8f-111">本指南也提供程式碼範例，以提供您在修改應用程式時可能遇到之問題的實際操作體驗和視覺標記法。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="e0b8f-112">這些範例來自完整的實用 Windows 通訊端應用程式範例，該應用程式已修改為同時支援 IPv4 和 IPv6。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="e0b8f-113">這些工作範例的原始程式碼包含在本檔結尾的兩個附錄中： [附錄 A：「僅 IPv4](appendix-a-ipv4-only-source-code-2.md) 」的原始程式碼會包含應用程式的原始程式碼，然後才會將其修改為支援 IPv6; [附錄 B：](appendix-b-ip-version-agnostic-source-code-2.md) 在應用程式已啟用 IPv6 的情況下，IP 版本中立的原始程式碼會提供原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="e0b8f-114">Microsoft 提供一個稱為 Checkv4.exe 的公用程式，可協助您在應用程式程式碼中找出可能移植的程式碼，也會提出修正的建議。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="e0b8f-115">本檔會示範 Checkv4.exe 公用程式，並使用附錄中包含的範例應用程式，以及顯示 Checkv4.exe 公用程式所產生之輸出的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="e0b8f-116">如需詳細資訊，請參閱 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="e0b8f-117">本指南所討論的程式設計區域包括：</span><span class="sxs-lookup"><span data-stu-id="e0b8f-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="e0b8f-118">變更 IPv6 Winsock Html5 應用程式的資料結構</span><span class="sxs-lookup"><span data-stu-id="e0b8f-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="e0b8f-119">IPv6 Winsock 應用程式的函式呼叫</span><span class="sxs-lookup"><span data-stu-id="e0b8f-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="e0b8f-120">使用硬式編碼的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="e0b8f-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="e0b8f-121">IPv6 Winsock 應用程式的消費者介面問題</span><span class="sxs-lookup"><span data-stu-id="e0b8f-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="e0b8f-122">IPv6 Winsock 應用程式的基礎通訊協定</span><span class="sxs-lookup"><span data-stu-id="e0b8f-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="e0b8f-123">IPv6 Winsock 應用程式的雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="e0b8f-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="e0b8f-124">因為沒有任何統一的事件順序，所以解決 IPv6 啟用問題的區段不會依序排列，因此您隨時都可以參考任何區段。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="e0b8f-125">強烈建議您在將 IPv6 功能新增至應用程式時，仔細檢查每個區段。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="e0b8f-126">也建議您閱讀 Checkv4.exe 公用程式的相關資訊，因為它包含瞭解決 IPv6 啟用問題之順序的秘訣。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="e0b8f-127">若要查看 Checkv4.exe 公用程式，並檢查您在應用程式中處理移植程式的順序，請參閱 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="e0b8f-128">本節包含編譯時間旗標的相關資訊，該旗標會嚴格檢查與 IPv6 不相容的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="e0b8f-129">若要直接移至範例應用程式，請參閱 [附錄 A：僅限 IPv4 的原始程式碼](appendix-a-ipv4-only-source-code-2.md) 和 [附錄 B： IP 版本中立的原始程式碼](appendix-b-ip-version-agnostic-source-code-2.md)。</span><span class="sxs-lookup"><span data-stu-id="e0b8f-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0b8f-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0b8f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0b8f-131">網際網路通訊協定第6版 (IPv6) </span><span class="sxs-lookup"><span data-stu-id="e0b8f-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="e0b8f-132">IPv6 支援</span><span class="sxs-lookup"><span data-stu-id="e0b8f-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="e0b8f-133">適用于 Windows 2000 的 IPv6 技術預覽</span><span class="sxs-lookup"><span data-stu-id="e0b8f-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="e0b8f-134">使用 Checkv4.exe 公用程式</span><span class="sxs-lookup"><span data-stu-id="e0b8f-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="e0b8f-135">附錄 A：僅限 IPv4 的來源程式碼</span><span class="sxs-lookup"><span data-stu-id="e0b8f-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="e0b8f-136">附錄 B： IP 版本中立的原始程式碼</span><span class="sxs-lookup"><span data-stu-id="e0b8f-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



