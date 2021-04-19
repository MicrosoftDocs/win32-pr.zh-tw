---
title: 關於 Windows 篩選平台
description: Windows 篩選平台 (WFP) 是一種網路流量處理平臺，其設計目的是取代 Windows XP 和 Windows Server 2003 網路流量篩選介面。
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969903"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="84106-103">關於 Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="84106-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="84106-104">Windows 篩選平台 (WFP) 是一種網路流量處理平臺，其設計目的是取代 Windows XP 和 Windows Server 2003 網路流量篩選介面。</span><span class="sxs-lookup"><span data-stu-id="84106-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="84106-105">WFP 是由一組網路堆疊的勾點所組成，以及一個可協調網路堆疊互動的篩選引擎。</span><span class="sxs-lookup"><span data-stu-id="84106-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="84106-106">WFP 元件</span><span class="sxs-lookup"><span data-stu-id="84106-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="84106-107">篩選引擎</span><span class="sxs-lookup"><span data-stu-id="84106-107">Filter Engine</span></span>

<span data-ttu-id="84106-108">核心多層篩選基礎結構（裝載于核心模式和使用者模式）會取代 Windows XP 和 Windows Server 2003 網路子系統中的多個篩選模組。</span><span class="sxs-lookup"><span data-stu-id="84106-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="84106-109">針對填充碼可以提供的任何資料欄位，篩選系統中任何層級的網路流量。</span><span class="sxs-lookup"><span data-stu-id="84106-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="84106-110">藉由在分類期間叫用標注來執行「標注」篩選。</span><span class="sxs-lookup"><span data-stu-id="84106-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="84106-111">將「允許」或「封鎖」動作傳回給叫用它以強制執行的填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="84106-112">提供不同原則來源之間的仲裁。</span><span class="sxs-lookup"><span data-stu-id="84106-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="84106-113">例如，當應用程式設定為保護任何與其相關的網路流量時，會決定優先順序，但會設定本機防火牆以防止應用程式安全的流量。</span><span class="sxs-lookup"><span data-stu-id="84106-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="84106-114">基礎篩選引擎 (BFE) </span><span class="sxs-lookup"><span data-stu-id="84106-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="84106-115">控制 Windows 篩選平台操作的服務。</span><span class="sxs-lookup"><span data-stu-id="84106-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="84106-116">它會執行下列工作。</span><span class="sxs-lookup"><span data-stu-id="84106-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="84106-117">接受平臺的篩選器和其他設定。</span><span class="sxs-lookup"><span data-stu-id="84106-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="84106-118">報告系統目前的狀態，包括統計資料。</span><span class="sxs-lookup"><span data-stu-id="84106-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="84106-119">強制執行在平臺中接受設定的安全性模型。</span><span class="sxs-lookup"><span data-stu-id="84106-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="84106-120">例如，本機系統管理員可以新增篩選器，但其他使用者只能查看這些篩選器。</span><span class="sxs-lookup"><span data-stu-id="84106-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="84106-121">將 configuration 設定連接至系統中的其他模組。</span><span class="sxs-lookup"><span data-stu-id="84106-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="84106-122">例如，IPsec 協商原則會移至 IKE/AuthIP 加密模組，篩選器會移至篩選引擎。</span><span class="sxs-lookup"><span data-stu-id="84106-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="84106-123">墊片</span><span class="sxs-lookup"><span data-stu-id="84106-123">Shims</span></span>

<span data-ttu-id="84106-124">位於網路堆疊與篩選引擎之間的核心模式元件。</span><span class="sxs-lookup"><span data-stu-id="84106-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="84106-125">填充碼會對篩選引擎進行分類，藉以進行篩選決定。</span><span class="sxs-lookup"><span data-stu-id="84106-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="84106-126">以下是可用的填充碼清單。</span><span class="sxs-lookup"><span data-stu-id="84106-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="84106-127">應用層強制 (ALE) 填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="84106-128">傳輸層模組填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="84106-129">網路層模組填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="84106-130">網際網路控制訊息通訊協定 (ICMP) 錯誤填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="84106-131">捨棄填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-131">Discard shim.</span></span>
-   <span data-ttu-id="84106-132">串流填充碼。</span><span class="sxs-lookup"><span data-stu-id="84106-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="84106-133">圖說文字</span><span class="sxs-lookup"><span data-stu-id="84106-133">Callouts</span></span>

<span data-ttu-id="84106-134">驅動程式所公開並用於特殊篩選的函式集合。</span><span class="sxs-lookup"><span data-stu-id="84106-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="84106-135">除了「允許」和「封鎖」的基本動作之外，標注還可以修改和保護輸入和輸出網路流量。</span><span class="sxs-lookup"><span data-stu-id="84106-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="84106-136">如需有關注解的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 檔中的 [Windows 篩選平台標注驅動程式](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) 主題。</span><span class="sxs-lookup"><span data-stu-id="84106-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="84106-137">WFP 提供內建的標注，可完成下列工作。</span><span class="sxs-lookup"><span data-stu-id="84106-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="84106-138">執行 IPsec 處理。</span><span class="sxs-lookup"><span data-stu-id="84106-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="84106-139">調整具狀態的篩選行為。</span><span class="sxs-lookup"><span data-stu-id="84106-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="84106-140">執行隱形模式篩選 (不會) 所要求的封包的無訊息放置。</span><span class="sxs-lookup"><span data-stu-id="84106-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="84106-141">控制 TCP 煙囪卸載。</span><span class="sxs-lookup"><span data-stu-id="84106-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="84106-142">與 Teredo 服務互動。</span><span class="sxs-lookup"><span data-stu-id="84106-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="84106-143">篩選引擎可讓協力廠商的標注在其每個核心模式層級進行註冊。</span><span class="sxs-lookup"><span data-stu-id="84106-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="84106-144">應用程式設計介面</span><span class="sxs-lookup"><span data-stu-id="84106-144">Application Programming Interface</span></span>

<span data-ttu-id="84106-145">一組可供開發人員用來建立和管理網路篩選應用程式的資料類型和函式。</span><span class="sxs-lookup"><span data-stu-id="84106-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="84106-146">這些資料類型和函式會分組為多個 [API 集合](api-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="84106-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="84106-147">WFP 功能</span><span class="sxs-lookup"><span data-stu-id="84106-147">WFP Features</span></span>

-   <span data-ttu-id="84106-148">提供封包篩選基礎結構，其中的獨立軟體廠商 (Isv) 可以外掛程式特殊化的篩選模組。</span><span class="sxs-lookup"><span data-stu-id="84106-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="84106-149">適用于 IPv4 和 IPv6。</span><span class="sxs-lookup"><span data-stu-id="84106-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="84106-150">允許資料篩選、修改和重新插入。</span><span class="sxs-lookup"><span data-stu-id="84106-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="84106-151">執行封包和串流處理。</span><span class="sxs-lookup"><span data-stu-id="84106-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="84106-152">除了每個網路介面或每個埠之外，還允許針對每個應用程式、每個使用者和每個連線啟用封包篩選。</span><span class="sxs-lookup"><span data-stu-id="84106-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="84106-153">提供開機時間安全性，直到基礎篩選引擎 (BFE) 可以啟動為止。</span><span class="sxs-lookup"><span data-stu-id="84106-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="84106-154">啟用可設定狀態的連接篩選。</span><span class="sxs-lookup"><span data-stu-id="84106-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="84106-155">處理預先和之後 IPsec 加密的資料。</span><span class="sxs-lookup"><span data-stu-id="84106-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="84106-156">允許整合 IPsec 和防火牆篩選原則。</span><span class="sxs-lookup"><span data-stu-id="84106-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="84106-157">提供原則管理基礎結構，以判斷何時應啟用特定篩選。</span><span class="sxs-lookup"><span data-stu-id="84106-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="84106-158">這包括來自不同廠商所提供的多個篩選準則的調節衝突需求。</span><span class="sxs-lookup"><span data-stu-id="84106-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="84106-159">處理大部分的封包重組和狀態追蹤。</span><span class="sxs-lookup"><span data-stu-id="84106-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="84106-160">包含一般使用者通知系統，可通知訂閱者對篩選系統的變更。</span><span class="sxs-lookup"><span data-stu-id="84106-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="84106-161">執行可報告系統狀態的列舉函數。</span><span class="sxs-lookup"><span data-stu-id="84106-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="84106-162">使用 net 事件來記錄 IPsec 錯誤和封包卸載。</span><span class="sxs-lookup"><span data-stu-id="84106-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="84106-163">支援網路診斷架構 [ (NDF) helper 類別](/windows/desktop/NDF/extensible-helper-classes)。</span><span class="sxs-lookup"><span data-stu-id="84106-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="84106-164">支援 Winsock API 的 [安全通訊端延伸](/windows/desktop/WinSock/winsock-secure-socket-extensions) 模組，可讓網路應用程式藉由設定 WFP 來保護其流量。</span><span class="sxs-lookup"><span data-stu-id="84106-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="84106-165">在應用層強制執行 (ALE) 層級，只會處理連接中的第一個封包，以最少的方式影響網路效能。</span><span class="sxs-lookup"><span data-stu-id="84106-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="84106-166">整合硬體卸載，其中核心模式注標模組可以使用硬體來執行特定的封包檢查。</span><span class="sxs-lookup"><span data-stu-id="84106-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84106-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="84106-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84106-168">WFP 架構</span><span class="sxs-lookup"><span data-stu-id="84106-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="84106-169">WFP 操作</span><span class="sxs-lookup"><span data-stu-id="84106-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="84106-170">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="84106-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="84106-171">IPsec 設定</span><span class="sxs-lookup"><span data-stu-id="84106-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="84106-172">WFP 設定</span><span class="sxs-lookup"><span data-stu-id="84106-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="84106-173">WFP 監視</span><span class="sxs-lookup"><span data-stu-id="84106-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="84106-174">WFP API</span><span class="sxs-lookup"><span data-stu-id="84106-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 

