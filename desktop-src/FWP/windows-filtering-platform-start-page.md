---
title: Windows 篩選平台
description: Windows 篩選平台 (WFP) 是一組 API 和系統服務，可提供建立網路篩選應用程式的平臺。
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Windows 篩選平台
- Windows 篩選平台起始頁面、起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106965045"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="1320b-105">Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="1320b-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="1320b-106">目的</span><span class="sxs-lookup"><span data-stu-id="1320b-106">Purpose</span></span>

<span data-ttu-id="1320b-107">Windows 篩選平台 (WFP) 是一組 API 和系統服務，可提供建立網路篩選應用程式的平臺。</span><span class="sxs-lookup"><span data-stu-id="1320b-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="1320b-108">WFP API 可讓開發人員撰寫程式碼，該程式碼會與在作業系統網路堆疊的數個層級上發生的封包處理進行互動。</span><span class="sxs-lookup"><span data-stu-id="1320b-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="1320b-109">您可以篩選網路資料，也可以在到達目的地之前加以修改。</span><span class="sxs-lookup"><span data-stu-id="1320b-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="1320b-110">藉由提供更簡單的開發平臺，WFP 是設計來取代先前的封包篩選技術，例如傳輸驅動程式介面 (TDI) 篩選器、網路驅動程式介面規格 (NDIS) 篩選器，以及 (LSP) 的 Winsock 分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1320b-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="1320b-111">從 Windows Server 2008 和 Windows Vista 開始，防火牆攔截和篩選器攔截驅動程式無法使用;使用這些驅動程式的應用程式應該改用 WFP。</span><span class="sxs-lookup"><span data-stu-id="1320b-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="1320b-112">使用 WFP API，開發人員可以執行防火牆、入侵偵測系統、防毒程式、網路監視工具和家長監護。</span><span class="sxs-lookup"><span data-stu-id="1320b-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="1320b-113">WFP 與整合，並根據應用程式使用通訊端 API (以應用程式為基礎的原則) ，來提供防火牆功能的支援，例如已驗證的通訊和動態防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="1320b-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="1320b-114">WFP 也提供 IPsec 原則管理、變更通知、網路診斷和具狀態篩選的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="1320b-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="1320b-115">Windows 篩選平台是開發平臺，而不是防火牆本身。</span><span class="sxs-lookup"><span data-stu-id="1320b-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="1320b-116">內建于 Windows Vista、Windows Server 2008 和更新版本作業系統的 Windows 防火牆（具有 Advanced Security (WFAS) 的防火牆應用程式是使用 WFP 來執行。</span><span class="sxs-lookup"><span data-stu-id="1320b-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="1320b-117">因此，使用 WFP API 或 [WFAS api](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) 開發的應用程式會使用內建于 wfp 的一般篩選仲裁邏輯。</span><span class="sxs-lookup"><span data-stu-id="1320b-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="1320b-118">WFP API 是由使用者模式 API 和核心模式 API 所組成。</span><span class="sxs-lookup"><span data-stu-id="1320b-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="1320b-119">本節提供整個 WFP 的總覽，並詳細說明 WFP API 的使用者模式部分。</span><span class="sxs-lookup"><span data-stu-id="1320b-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="1320b-120">如需核心模式 WFP API 的詳細說明，請參閱 [Windows 驅動程式套件](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) 線上說明。</span><span class="sxs-lookup"><span data-stu-id="1320b-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1320b-121">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="1320b-121">Developer audience</span></span>

<span data-ttu-id="1320b-122">Windows 篩選平台 API 是設計來供程式設計人員使用 C/c + + 開發軟體。</span><span class="sxs-lookup"><span data-stu-id="1320b-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="1320b-123">程式設計人員應該熟悉網路概念，以及使用使用者模式和核心模式元件的系統設計。</span><span class="sxs-lookup"><span data-stu-id="1320b-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1320b-124">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="1320b-124">Run-time requirements</span></span>

<span data-ttu-id="1320b-125">執行 windows Vista 和更新版本的用戶端，以及執行 Windows Server 2008 和更新版本的伺服器上，都支援 Windows 篩選平台。</span><span class="sxs-lookup"><span data-stu-id="1320b-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="1320b-126">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="1320b-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="1320b-127">本節內容</span><span class="sxs-lookup"><span data-stu-id="1320b-127">In this section</span></span>



| <span data-ttu-id="1320b-128">主題</span><span class="sxs-lookup"><span data-stu-id="1320b-128">Topic</span></span>                                                                                               | <span data-ttu-id="1320b-129">描述</span><span class="sxs-lookup"><span data-stu-id="1320b-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1320b-130">Windows 篩選平台的新功能</span><span class="sxs-lookup"><span data-stu-id="1320b-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="1320b-131">Windows 篩選平台中新功能和 Api 的資訊。</span><span class="sxs-lookup"><span data-stu-id="1320b-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="1320b-132">關於 Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="1320b-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="1320b-133">Windows 篩選平台的總覽。</span><span class="sxs-lookup"><span data-stu-id="1320b-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="1320b-134">使用 Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="1320b-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="1320b-135">使用 Windows 篩選平台 API 的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="1320b-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="1320b-136">Windows 篩選平台 API 參考</span><span class="sxs-lookup"><span data-stu-id="1320b-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="1320b-137">Windows 篩選平台函數、結構和常數的檔。</span><span class="sxs-lookup"><span data-stu-id="1320b-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="1320b-138">其他資源</span><span class="sxs-lookup"><span data-stu-id="1320b-138">Additional resources</span></span>

<span data-ttu-id="1320b-139">若要詢問問題並取得有關使用 WFP API 的討論，請造訪 [Windows 篩選平台論壇](https://social.msdn.microsoft.com/forums/wfp/threads/)。</span><span class="sxs-lookup"><span data-stu-id="1320b-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1320b-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="1320b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1320b-141">核心模式 Windows 篩選平台 API-設計指南</span><span class="sxs-lookup"><span data-stu-id="1320b-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="1320b-142">核心模式 Windows 篩選平台 API-參考</span><span class="sxs-lookup"><span data-stu-id="1320b-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="1320b-143">具有進階安全性的 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="1320b-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="1320b-144">WFP 診斷可延伸 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="1320b-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="1320b-145">Winsock 安全通訊端擴充功能</span><span class="sxs-lookup"><span data-stu-id="1320b-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

