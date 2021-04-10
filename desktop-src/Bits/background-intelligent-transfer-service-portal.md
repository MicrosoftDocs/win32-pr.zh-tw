---
title: 背景智慧型傳送服務
description: 背景智慧型傳送服務 (BITS) 會在用戶端和伺服器之間傳輸檔案 (下載或上傳)，並提供有關傳輸的進度資訊。
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- 背景智慧型傳送服務
- 背景智慧型傳送服務，起始頁
- 'BITS (查看背景智慧型傳送服務) '
- 下載檔案位
- 背景檔案傳輸位元組
- 上傳檔案位
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933486"
---
# <a name="background-intelligent-transfer-service"></a><span data-ttu-id="12463-109">背景智慧型傳送服務</span><span class="sxs-lookup"><span data-stu-id="12463-109">Background Intelligent Transfer Service</span></span>

## <a name="purpose"></a><span data-ttu-id="12463-110">目的</span><span class="sxs-lookup"><span data-stu-id="12463-110">Purpose</span></span>

<span data-ttu-id="12463-111">程式設計師和系統管理員會使用背景智慧型傳送服務 (位) ，從檔案下載檔案或將檔案上傳至 HTTP 網頁伺服器和 SMB 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="12463-111">Background Intelligent Transfer Service (BITS) is used by programmers and system administrators to download files from or upload files to HTTP web servers and SMB file shares.</span></span> <span data-ttu-id="12463-112">BITS 會考慮傳送的費用，以及網路使用量，如此一來，使用者的前景工作就越不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="12463-112">BITS will take the cost of the transfer into consideration, as well as the network usage so that the user's foreground work has as little impact as possible.</span></span> <span data-ttu-id="12463-113">BITS 也會處理網路 interuptions、暫停和自動繼續傳輸，即使在重新開機後也一樣。</span><span class="sxs-lookup"><span data-stu-id="12463-113">BITS also handles network interuptions, pausing and automatically resuming transfers, even after a reboot.</span></span> <span data-ttu-id="12463-114">BITS 包含用於建立和管理傳輸以及 BitsAdmin 命令列公用程式的 PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12463-114">BITS includes PowerShell cmdlets for creating and managing transfers as well as the BitsAdmin command-line utility.</span></span>

> [!Note]  
> <span data-ttu-id="12463-115">Windows 可以使用 BITS 將更新下載至您的本機系統。</span><span class="sxs-lookup"><span data-stu-id="12463-115">BITS can be used by Windows to download updates to your local system.</span></span> <span data-ttu-id="12463-116">如果您是使用者搜尋如何針對 BITS 安裝進行疑難排解的方法，請參閱 [修正 Windows Update 問題](https://support.microsoft.com/help/10164/fix-windows-update-errors)。</span><span class="sxs-lookup"><span data-stu-id="12463-116">If you are an end-user searching for ways to troubleshoot your BITS installation, see [Fix Windows Update Issues](https://support.microsoft.com/help/10164/fix-windows-update-errors).</span></span> 
 

## <a name="where-applicable"></a><span data-ttu-id="12463-117">適用時</span><span class="sxs-lookup"><span data-stu-id="12463-117">Where applicable</span></span>

<span data-ttu-id="12463-118">針對需要下列動作的應用程式使用 BITS：</span><span class="sxs-lookup"><span data-stu-id="12463-118">Use BITS for applications that need to:</span></span>

-   <span data-ttu-id="12463-119">從檔案下載或上傳至 HTTP 或 REST web 伺服器或 SMB 檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="12463-119">Download from or upload files to an HTTP or REST web server or SMB file server.</span></span>
-   <span data-ttu-id="12463-120">在網路中斷連線並重新啟動電腦之後，自動繼續檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="12463-120">Automatically resume file transfers after network disconnects and computer restarts.</span></span>
-   <span data-ttu-id="12463-121">保留其他網路應用程式的回應性。</span><span class="sxs-lookup"><span data-stu-id="12463-121">Preserve the responsiveness of other network applications.</span></span>
-   <span data-ttu-id="12463-122">請注意網路成本，例如漫遊網路</span><span class="sxs-lookup"><span data-stu-id="12463-122">Be mindful of the network cost on e.g. roaming networks</span></span>
-   <span data-ttu-id="12463-123">選擇性地使用 [BranchCache](/windows-server/networking/branchcache/branchcache) 將廣域網路) 流量優化 (</span><span class="sxs-lookup"><span data-stu-id="12463-123">Optionally work with [BranchCache](/windows-server/networking/branchcache/branchcache) to optimize wide area network (WAN) traffic</span></span>

## <a name="developer-audience"></a><span data-ttu-id="12463-124">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="12463-124">Developer audience</span></span>

<span data-ttu-id="12463-125">BITS 是針對 C 和 c + + 開發人員所設計的 COM 介面，也可供 .NET 開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="12463-125">BITS is a COM interface designed for C and C++ developers that can also be used by .NET developers.</span></span> <span data-ttu-id="12463-126">UWP 開發人員應該使用 [Windows.networking.backgroundtransfer.contentprefetcher](/uwp/api/Windows.Networking.BackgroundTransfer) API，而不是 BITS api。</span><span class="sxs-lookup"><span data-stu-id="12463-126">UWP developers should use the [Windows.Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) API and not the BITS API.</span></span>

## <a name="bits-versions"></a><span data-ttu-id="12463-127">BITS 版本</span><span class="sxs-lookup"><span data-stu-id="12463-127">BITS versions</span></span>

<span data-ttu-id="12463-128">如需舊版作業系統的完整版本歷程記錄和資訊，請參閱 [新功能](what-s-new.md)。</span><span class="sxs-lookup"><span data-stu-id="12463-128">For complete version history and information on earlier operating system, see [What's New](what-s-new.md).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="12463-129">本節內容</span><span class="sxs-lookup"><span data-stu-id="12463-129">In this section</span></span>



| <span data-ttu-id="12463-130">主題</span><span class="sxs-lookup"><span data-stu-id="12463-130">Topic</span></span>                                                           | <span data-ttu-id="12463-131">描述</span><span class="sxs-lookup"><span data-stu-id="12463-131">Description</span></span>                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12463-132">關於 BITS</span><span class="sxs-lookup"><span data-stu-id="12463-132">About BITS</span></span>](about-bits.md)<br/>                         | <span data-ttu-id="12463-133">關於位的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="12463-133">General information about BITS.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="12463-134">使用 BITS</span><span class="sxs-lookup"><span data-stu-id="12463-134">Using BITS</span></span>](using-bits.md)<br/>                         | <span data-ttu-id="12463-135">開發在用戶端與伺服器之間傳輸檔案之 BITS 用戶端的程式指南。</span><span class="sxs-lookup"><span data-stu-id="12463-135">Procedural guide for developing BITS clients that transfer files between a client and server.</span></span><br/>                                                                        |
| [<span data-ttu-id="12463-136">BITS 參考</span><span class="sxs-lookup"><span data-stu-id="12463-136">BITS Reference</span></span>](bits-reference.md)<br/>                 | <span data-ttu-id="12463-137">BITS 程式設計介面的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="12463-137">Reference information for the BITS programming interfaces.</span></span> <span data-ttu-id="12463-138">也包含有關範例、工具、上傳作業的伺服器設定，以及上傳通訊協定的資訊。</span><span class="sxs-lookup"><span data-stu-id="12463-138">Also contains information about samples, tools, server settings for upload jobs, and the upload protocol.</span></span><br/> |
| [<span data-ttu-id="12463-139">最佳作法</span><span class="sxs-lookup"><span data-stu-id="12463-139">Best Practices</span></span>](best-practices-when-using-bits.md)<br/> | <span data-ttu-id="12463-140">設計使用 BITS 的應用程式時應考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="12463-140">Information to consider when designing an application that uses BITS.</span></span><br/>                                                                                                |



 

## <a name="additional-resources"></a><span data-ttu-id="12463-141">其他資源</span><span class="sxs-lookup"><span data-stu-id="12463-141">Additional resources</span></span>

<span data-ttu-id="12463-142">以下是其他資源。</span><span class="sxs-lookup"><span data-stu-id="12463-142">The following are additional resources.</span></span>


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12463-143">.NET 參考 DLL</span><span class="sxs-lookup"><span data-stu-id="12463-143">.NET Reference DLL</span></span>   | <span data-ttu-id="12463-144">如需使用參考 Dll 從 .NET 使用 BITS 的詳細資訊，請參閱 [使用參考 dll 從 .Net 呼叫位](/windows/desktop/Bits/bits-dot-net)</span><span class="sxs-lookup"><span data-stu-id="12463-144">For information on using BITS from .NET using reference DLLs, see [Calling into BITS from .NET using Reference DLLs](/windows/desktop/Bits/bits-dot-net)</span></span>      |
| <span data-ttu-id="12463-145">.NET 包裝函式</span><span class="sxs-lookup"><span data-stu-id="12463-145">.NET Wrapper</span></span>   | <span data-ttu-id="12463-146">若是其他適用于 BITS 的 .NET 包裝函式，您可以在 [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) 中搜尋以 bits 標記標記的專案。</span><span class="sxs-lookup"><span data-stu-id="12463-146">For other .NET wrappers for BITS, you can search [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) for projects tagged with the BITS tag.</span></span>        |



 

 

