---
title: NAP 伺服器端架構
description: NAP 伺服器端架構
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092559"
---
# <a name="nap-server-side-architecture"></a><span data-ttu-id="d9261-103">NAP 伺服器端架構</span><span class="sxs-lookup"><span data-stu-id="d9261-103">NAP Server-side Architecture</span></span>

> [!Note]  
> <span data-ttu-id="d9261-104">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="d9261-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d9261-105">NAP 伺服器端平臺架構會使用執行 Windows Server 2008 的電腦。</span><span class="sxs-lookup"><span data-stu-id="d9261-105">The NAP server-side platform architecture uses computers running Windows Server 2008.</span></span> <span data-ttu-id="d9261-106">下圖顯示 NAP 平臺的伺服器端支援架構，包括 Windows 型 NAP 強制端點和 NAP 健康原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-106">The following figure shows the architecture of the server-side support for the NAP platform, consisting of Windows-based NAP enforcement points and a NAP health policy server.</span></span>

![nap 平臺的伺服器端支援架構](images/nap-server-side-arch.png)

<span data-ttu-id="d9261-108">以 Windows 為基礎的 NAP 強制端點有一層 NAP 強制伺服器 (ES) 元件。</span><span class="sxs-lookup"><span data-stu-id="d9261-108">A Windows-based NAP enforcement point has a layer of NAP Enforcement Server (ES) components.</span></span> <span data-ttu-id="d9261-109">每個 NAP ES 都是針對不同類型的網路存取或通訊而定義。</span><span class="sxs-lookup"><span data-stu-id="d9261-109">Each NAP ES is defined for a different type of network access or communication.</span></span> <span data-ttu-id="d9261-110">例如，遠端存取 VPN 連線的 NAP ES，以及 DHCP 設定的 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="d9261-110">For example, there is a NAP ES for remote access VPN connections and a NAP ES for DHCP configuration.</span></span> <span data-ttu-id="d9261-111">NAP ES 通常符合特定類型的支援 NAP 用戶端。</span><span class="sxs-lookup"><span data-stu-id="d9261-111">The NAP ES is typically matched to a specific type of NAP-capable client.</span></span> <span data-ttu-id="d9261-112">例如，DHCP NAP ES 是設計來搭配使用 DHCP 型 NAP 強制用戶端 (EC) 。</span><span class="sxs-lookup"><span data-stu-id="d9261-112">For example, the DHCP NAP ES is designed to work with a DHCP-based NAP Enforcement Client (EC).</span></span> <span data-ttu-id="d9261-113">協力廠商軟體廠商或 Microsoft 可以為 NAP 平臺提供額外的 NAP ESs。</span><span class="sxs-lookup"><span data-stu-id="d9261-113">Third-party software vendors or Microsoft can provide additional NAP ESs for the NAP platform.</span></span> <span data-ttu-id="d9261-114">NAP ES 從其對應的 NAP EC 取得健全狀況 (SSoH) 的系統聲明，並將其傳送至 NAP 健康原則伺服器，作為遠端驗證撥入使用者服務 (RADIUS) 廠商專屬的屬性 (VSA) 的 Access-Request [訊息](https://www.ietf.org/rfc/rfc2865.txt?number=2865)</span><span class="sxs-lookup"><span data-stu-id="d9261-114">A NAP ES obtains the System Statement of Health (SSoH) from its corresponding NAP EC and sends it to an NAP health policy server as a Remote Authentication Dial-in User Service (RADIUS) vendor-specific attribute (VSA) of [RADIUS Access-Request message](https://www.ietf.org/rfc/rfc2865.txt?number=2865)</span></span>

<span data-ttu-id="d9261-115">如伺服器端架構圖所示，NAP 健全狀況原則伺服器具有下列元件：</span><span class="sxs-lookup"><span data-stu-id="d9261-115">As shown in server-side architecture figure, the NAP health policy server has the following components:</span></span>

-   <span data-ttu-id="d9261-116">網路原則伺服器 (NPS) 服務</span><span class="sxs-lookup"><span data-stu-id="d9261-116">Network Policy Server (NPS) Service</span></span>

    <span data-ttu-id="d9261-117">接收 RADIUS Access-Request 訊息、解壓縮 SSoH，然後將它傳遞給 NAP 管理伺服器元件。</span><span class="sxs-lookup"><span data-stu-id="d9261-117">Receives the RADIUS Access-Request message, extracts the SSoH, and passes it to the NAP Administration Server component.</span></span> <span data-ttu-id="d9261-118">NPS 服務隨附于 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="d9261-118">The NPS service is provided with Windows Server 2008.</span></span>

-   <span data-ttu-id="d9261-119">NAP 管理伺服器</span><span class="sxs-lookup"><span data-stu-id="d9261-119">NAP Administration Server</span></span>

    <span data-ttu-id="d9261-120">促進 NPS 服務與系統健康狀態驗證 (Shv) 之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="d9261-120">Facilitates communication between the NPS service and the System Health Validators (SHVs).</span></span> <span data-ttu-id="d9261-121">Nap 管理伺服器元件隨附于 NAP 平臺。</span><span class="sxs-lookup"><span data-stu-id="d9261-121">The NAP Administration Server component is provided with the NAP platform.</span></span>

-   <span data-ttu-id="d9261-122">SHV 元件的層級</span><span class="sxs-lookup"><span data-stu-id="d9261-122">A layer of SHV components</span></span>

    <span data-ttu-id="d9261-123">每個 SHV 都是針對一或多個系統健康狀態資訊類型所定義，而且可以與 SHA 相符。</span><span class="sxs-lookup"><span data-stu-id="d9261-123">Each SHV is defined for one or multiple types of system health information and can be matched to an SHA.</span></span> <span data-ttu-id="d9261-124">例如，可能有一個適用于防毒程式的 SHV。</span><span class="sxs-lookup"><span data-stu-id="d9261-124">For example, there could be an SHV for an antivirus program.</span></span> <span data-ttu-id="d9261-125">SHV 可能與一或多個健康需求伺服器相符。</span><span class="sxs-lookup"><span data-stu-id="d9261-125">An SHV could be matched to one or multiple health requirement servers.</span></span> <span data-ttu-id="d9261-126">例如，用於檢查防毒軟體簽章的 SHV 會與包含最新簽章檔案的伺服器相符。</span><span class="sxs-lookup"><span data-stu-id="d9261-126">For example, an SHV for checking antivirus signatures is matched to the server that contains the latest signature file.</span></span> <span data-ttu-id="d9261-127">Shv 不需要有對應的健康需求伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-127">SHVs do not have to have a corresponding health requirement server.</span></span> <span data-ttu-id="d9261-128">SHV 可以指示支援 NAP 的用戶端檢查本機系統設定，以確定已啟用以主機為基礎的防火牆。</span><span class="sxs-lookup"><span data-stu-id="d9261-128">An SHV can just instruct NAP-capable clients to check local system settings to ensure that a host-based firewall is enabled.</span></span> <span data-ttu-id="d9261-129">Windows Server 2008 包含 Windows 安全性健全狀況驗證程式 (WSHV) 。</span><span class="sxs-lookup"><span data-stu-id="d9261-129">Windows Server 2008 includes the Windows Security Health Validator (WSHV).</span></span> <span data-ttu-id="d9261-130">其他 Shv 由協力廠商軟體廠商或 Microsoft 做為 NAP 平臺的附加元件提供。</span><span class="sxs-lookup"><span data-stu-id="d9261-130">Additional SHVs are provided by third-party software vendors or by Microsoft as add-ons to the NAP platform.</span></span>

-   <span data-ttu-id="d9261-131">SHV API</span><span class="sxs-lookup"><span data-stu-id="d9261-131">SHV API</span></span>

    <span data-ttu-id="d9261-132">提供一組函數呼叫，可讓 Shv 向 NAP 管理伺服器元件註冊、接收健康狀態聲明 (Soh) 自 NAP 管理伺服器元件，以及傳送健全狀況回應的聲明 (Sohr) 至 NAP 管理伺服器元件。</span><span class="sxs-lookup"><span data-stu-id="d9261-132">Provides a set of function calls that allow SHVs to register with the NAP Administration Server component, receive Statements of Health (SoHs) from the NAP Administration Server component, and send Statement of Health Responses (SoHRs) to the NAP Administration Server component.</span></span> <span data-ttu-id="d9261-133">SHV API 隨附于 NAP 平臺。</span><span class="sxs-lookup"><span data-stu-id="d9261-133">The SHV API is provided with the NAP platform.</span></span> <span data-ttu-id="d9261-134">請參閱下列 NAP 介面： [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) 和 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)。</span><span class="sxs-lookup"><span data-stu-id="d9261-134">See the following NAP interfaces: [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) and [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span>

<span data-ttu-id="d9261-135">如先前所述，NAP 伺服器端基礎結構的較常見設定是由 NAP 強制端點所組成，以提供特定類型的網路存取或通訊，以及個別的 NPS 健康原則伺服器，提供系統健康情況驗證和修復。</span><span class="sxs-lookup"><span data-stu-id="d9261-135">As previously described, the more common configuration for NAP server-side infrastructure consists of NAP enforcement points providing network access or communication of a specific type and separate NPS health policy servers providing system health validation and remediation.</span></span> <span data-ttu-id="d9261-136">您可以在個別的 Windows NAP 強制端點上，將 NPS 服務安裝為 NAP 健康原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-136">It is possible to install the NPS service as a NAP health policy server on individual Windows-based NAP enforcement points.</span></span> <span data-ttu-id="d9261-137">不過，在此設定中，每個 NAP 強制端點接著必須個別設定網路存取和健康原則。</span><span class="sxs-lookup"><span data-stu-id="d9261-137">However, in this configuration, each NAP enforcement point must then be separately configured with network access and health policies.</span></span> <span data-ttu-id="d9261-138">建議的設定是使用不同的 NAP 健康原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-138">The recommended configuration is to use separate NAP health policy servers.</span></span>

<span data-ttu-id="d9261-139">整體 NAP 架構包含下列元件集：</span><span class="sxs-lookup"><span data-stu-id="d9261-139">The overall NAP architecture consists of the following sets of components:</span></span>

-   <span data-ttu-id="d9261-140">三個 NAP 用戶端元件 (SHA 層、NAP 代理程式和 NAP EC 層) 。</span><span class="sxs-lookup"><span data-stu-id="d9261-140">The three NAP client components (an SHA layer, the NAP Agent, and a NAP EC layer).</span></span>
-   <span data-ttu-id="d9261-141">四個 NAP 伺服器端元件 (SHV 層、NAP 管理伺服器、NPS 服務，以及 Windows 型 NAP 強制端點) 的 NAP ES 層。</span><span class="sxs-lookup"><span data-stu-id="d9261-141">The four NAP server-side components (an SHV layer, the NAP Administration Server, the NPS service, and a NAP ES layer on Windows-based NAP enforcement points).</span></span>
-   <span data-ttu-id="d9261-142">健康需求伺服器，也就是可提供 NAP 健康原則伺服器目前系統健康情況需求的電腦。</span><span class="sxs-lookup"><span data-stu-id="d9261-142">Health requirement severs, which are computers that can provide current system health requirements for NAP health policy servers.</span></span>
-   <span data-ttu-id="d9261-143">補救伺服器，這是包含 NAP 用戶端可以存取以補救其不符合規範狀態的健康狀態更新資源的電腦。</span><span class="sxs-lookup"><span data-stu-id="d9261-143">Remediation servers, which are computers that contain health update resources that NAP clients can access to remediate their noncompliant state.</span></span>

<span data-ttu-id="d9261-144">下圖顯示 NAP 平臺元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="d9261-144">The following figure shows the relationships between the components of the NAP platform.</span></span>

![nap 平臺元件之間的關聯性](images/nap-components.png)

<span data-ttu-id="d9261-146">請注意下列元件集的相符：</span><span class="sxs-lookup"><span data-stu-id="d9261-146">Notice the matching of the following sets of components:</span></span>

-   <span data-ttu-id="d9261-147">NAP ECs 和 NAP ESs 通常相符。</span><span class="sxs-lookup"><span data-stu-id="d9261-147">NAP ECs and NAP ESs are typically matched.</span></span>

    <span data-ttu-id="d9261-148">例如，NAP 用戶端上的 DHCP NAP EC 與 DHCP 伺服器上的 DHCP NAP ES 相符。</span><span class="sxs-lookup"><span data-stu-id="d9261-148">For example, the DHCP NAP EC on the NAP client is matched to the DHCP NAP ES on the DHCP server.</span></span>

-   <span data-ttu-id="d9261-149">可以比對 SHA 和補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-149">SHA and remediation servers can be matched.</span></span>

    <span data-ttu-id="d9261-150">例如，用戶端上的防毒軟體 SHA 符合防毒軟體的補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-150">For example, an antivirus SHA on the client is matched to an antivirus signature remediation server.</span></span>

-   <span data-ttu-id="d9261-151">Shv 和健康需求伺服器可以進行比對。</span><span class="sxs-lookup"><span data-stu-id="d9261-151">SHVs and health requirement servers can be matched.</span></span>

    <span data-ttu-id="d9261-152">例如，NAP 健康原則伺服器上的防毒軟體 SHV 可以與防毒軟體健康需求伺服器進行比對。</span><span class="sxs-lookup"><span data-stu-id="d9261-152">For example, an antivirus SHV on the NAP health policy server can be matched to an antivirus health requirement server.</span></span>

<span data-ttu-id="d9261-153">協力廠商軟體廠商可透過下列方式擴充 NAP 平臺：</span><span class="sxs-lookup"><span data-stu-id="d9261-153">Third-party software vendors can extend the NAP platform in the following ways:</span></span>

-   <span data-ttu-id="d9261-154">建立新方法，以評估 NAP 用戶端的健全狀況。</span><span class="sxs-lookup"><span data-stu-id="d9261-154">Create a new method by which the health of a NAP client is evaluated.</span></span>

    <span data-ttu-id="d9261-155">協力廠商軟體廠商必須建立適用于 NAP 用戶端的 SHA、NAP 健康原則伺服器的 SHV，以及（如有需要）健康需求和補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-155">Third-party software vendors must create an SHA for the NAP client, an SHV for the NAP health policy server, and, if needed, health requirement and remediation servers.</span></span> <span data-ttu-id="d9261-156">如果健康需求或補救伺服器已存在，例如防毒軟體簽章散發伺服器，則只需要建立對應的 SHA 和 SHV 元件。</span><span class="sxs-lookup"><span data-stu-id="d9261-156">If the health requirement or remediation servers already exist, such as an antivirus signature distribution server, then only the corresponding SHA and SHV components need to be created.</span></span> <span data-ttu-id="d9261-157">在某些情況下，不需要健康需求或補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-157">In some cases, health requirement or remediation servers are not needed.</span></span>

-   <span data-ttu-id="d9261-158">建立新的方法，以強制執行網路存取或通訊的健康需求。</span><span class="sxs-lookup"><span data-stu-id="d9261-158">Create a new method for enforcing health requirements for network access or communication.</span></span>

    <span data-ttu-id="d9261-159">協力廠商軟體廠商必須在 NAP 用戶端上建立 NAP EC。</span><span class="sxs-lookup"><span data-stu-id="d9261-159">Third-party software vendors must create a NAP EC on the NAP client.</span></span> <span data-ttu-id="d9261-160">如果強制方法使用 Windows 服務，則協力廠商軟體廠商必須建立對應的 NAP ES，以使用 RADIUS 通訊協定或在 NAP 強制端點上安裝的 NPS 服務作為 RADIUS proxy 來與 NAP 健康原則伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="d9261-160">If the enforcement method uses a Windows-based service, third-party software vendors must create a corresponding NAP ES that communicates with a NAP health policy server using the RADIUS protocol or by using the NPS service installed on the NAP enforcement point as a RADIUS proxy.</span></span>

<span data-ttu-id="d9261-161">下列各節將進一步詳細說明 NAP 伺服器端架構的元件。</span><span class="sxs-lookup"><span data-stu-id="d9261-161">The following sections describe the components of the NAP server-side architecture in further detail.</span></span>

## <a name="nap-enforcement-server"></a><span data-ttu-id="d9261-162">NAP 強制伺服器</span><span class="sxs-lookup"><span data-stu-id="d9261-162">NAP Enforcement Server</span></span>

<span data-ttu-id="d9261-163">NAP 強制伺服器 (ES) 允許某些層級的網路存取或通訊，可將 NAP 用戶端的健康狀態傳遞給網路健康原則伺服器進行評估，並根據回應來強制執行有限的網路存取。</span><span class="sxs-lookup"><span data-stu-id="d9261-163">A NAP Enforcement Server (ES) allows some level of network access or communication, can pass a NAP client's health status to the network health policy server for evaluation, and, based on the response, can provide the enforcement of limited network access.</span></span>

<span data-ttu-id="d9261-164">Windows Server 2008 隨附的 NAP ESs 如下所示：</span><span class="sxs-lookup"><span data-stu-id="d9261-164">The NAP ESs included with Windows Server 2008 are the following:</span></span>

-   <span data-ttu-id="d9261-165">Ipsec 受 IPsec 保護的通訊 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="d9261-165">An IPsec NAP ES for IPsec-protected communications.</span></span>

    <span data-ttu-id="d9261-166">針對受 IPsec 保護的通訊， (HRA) 的健康情況登錄授權單位、執行 Windows Server 2008 的電腦，以及從憑證授權單位單位取得健康情況憑證的 Internet Information Services (IIS) ，將 NAP 用戶端的健康狀態資訊傳遞給 NAP 健康原則伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-166">For IPsec-protected communication, the Health Registration Authority (HRA), a computer running Windows Server 2008 and Internet Information Services (IIS) that obtains health certificates from a certification authority (CA) for compliant computers, passes the NAP client's health status information to the NAP health policy server.</span></span>

-   <span data-ttu-id="d9261-167">Dhcp NAP ES，用於以 DHCP 為基礎的 IP 位址設定。</span><span class="sxs-lookup"><span data-stu-id="d9261-167">A DHCP NAP ES for DHCP-based IP address configuration.</span></span>

    <span data-ttu-id="d9261-168">DHCP NAP ES 是 DHCP 伺服器服務中的功能，使用業界標準 DHCP 訊息與 NAP 用戶端上的 DHCP NAP EC 通訊。</span><span class="sxs-lookup"><span data-stu-id="d9261-168">The DHCP NAP ES is functionality in the DHCP Server service that uses industry standard DHCP messages to communicate with the DHCP NAP EC on a NAP client.</span></span> <span data-ttu-id="d9261-169">有限網路存取的 DHCP 強制是透過 DHCP 選項完成的。</span><span class="sxs-lookup"><span data-stu-id="d9261-169">DHCP enforcement for limited network access is done through DHCP options.</span></span>

-   <span data-ttu-id="d9261-170">終端機服務 (TS 閘道伺服器連接的 TS) 閘道 NAP ES。</span><span class="sxs-lookup"><span data-stu-id="d9261-170">A Terminal Services (TS) Gateway NAP ES for TS Gateway server-based connections.</span></span>

<span data-ttu-id="d9261-171">針對遠端存取 VPN 和 802.1 X 驗證連線，NPS 服務中的功能會使用 NAP 用戶端與 NAP 健康原則伺服器之間的 PEAP TLV 訊息。</span><span class="sxs-lookup"><span data-stu-id="d9261-171">For remote access VPN and 802.1X-authenticated connections, functionality in the NPS service uses PEAP-TLV messages between NAP clients and the NAP health policy server.</span></span> <span data-ttu-id="d9261-172">VPN 強制會透過套用至 VPN 連線的 IP 封包篩選器來執行。</span><span class="sxs-lookup"><span data-stu-id="d9261-172">VPN enforcement is done through IP packet filters that are applied to the VPN connection.</span></span> <span data-ttu-id="d9261-173">802.1 x 強制執行于 802.1 X 網路存取裝置上，方法是將 IP 封包篩選套用至連線，或指派與受限制網路對應的 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9261-173">802.1X enforcement is done at the 802.1X network access device by applying IP packet filters to the connection or by assigning the connection a VLAN ID corresponding to the restricted network.</span></span>

## <a name="nap-administration-server"></a><span data-ttu-id="d9261-174">NAP 管理伺服器</span><span class="sxs-lookup"><span data-stu-id="d9261-174">NAP Administration Server</span></span>

<span data-ttu-id="d9261-175">NAP 管理伺服器元件提供下列服務：</span><span class="sxs-lookup"><span data-stu-id="d9261-175">The NAP Administration Server component provides the following services:</span></span>

-   <span data-ttu-id="d9261-176">透過 NPS 服務取得 NAP ES 的 SSoHs。</span><span class="sxs-lookup"><span data-stu-id="d9261-176">Obtains the SSoHs from the NAP ES through the NPS service.</span></span>
-   <span data-ttu-id="d9261-177">將 SSoHs 中的 Soh 散發給 (SHV) 的適當系統健康情況驗證程式。</span><span class="sxs-lookup"><span data-stu-id="d9261-177">Distributes the SoHs in the SSoHs to the appropriate System Health Validators (SHV).</span></span>
-   <span data-ttu-id="d9261-178">從 Shv 收集 Sohr，並將其傳遞給 NPS 服務進行評估。</span><span class="sxs-lookup"><span data-stu-id="d9261-178">Collects SoHRs from the SHVs and passes them to NPS service for evaluation.</span></span>

## <a name="nps-service"></a><span data-ttu-id="d9261-179">NPS 服務</span><span class="sxs-lookup"><span data-stu-id="d9261-179">NPS Service</span></span>

<span data-ttu-id="d9261-180">RADIUS 是一種廣泛部署的通訊協定，可啟用集中式驗證、授權及帳戶處理 (Rfc) 2865 和2866的要求中所述的網路存取。</span><span class="sxs-lookup"><span data-stu-id="d9261-180">RADIUS is a widely deployed protocol enabling centralized authentication, authorization, and accounting for network access that is described in Requests for Comments (RFCs) 2865 and 2866.</span></span> <span data-ttu-id="d9261-181">RADIUS 最初是針對撥號遠端存取而開發，現在受到無線存取點、驗證乙太網路交換器、VPN 伺服器、數位用戶線路 (DSL) 存取伺服器，以及其他網路存取伺服器的支援。</span><span class="sxs-lookup"><span data-stu-id="d9261-181">Originally developed for dial-up remote access, RADIUS is now supported by wireless access points, authenticating Ethernet switches, VPN servers, Digital Subscriber Line (DSL) access servers, and other network access servers.</span></span>

<span data-ttu-id="d9261-182">NPS 是在 Windows Server 2008 中執行 RADIUS 伺服器和 proxy。</span><span class="sxs-lookup"><span data-stu-id="d9261-182">NPS is the implementation of a RADIUS server and proxy in Windows Server 2008.</span></span> <span data-ttu-id="d9261-183">NPS 會取代 Windows Server 2003 中 (IAS) 的網際網路驗證服務。</span><span class="sxs-lookup"><span data-stu-id="d9261-183">NPS replaces the Internet Authentication Service (IAS) in Windows Server 2003.</span></span> <span data-ttu-id="d9261-184">針對 NAP 平臺，NPS 服務包含 NAP 系統管理員伺服器元件、支援 SHV API 和可安裝的 Shv，以及設定健康原則的選項。</span><span class="sxs-lookup"><span data-stu-id="d9261-184">For the NAP platform, the NPS service includes the NAP Administrator Server component, support for the SHV API and installable SHVs, and options for configuring health policies.</span></span>

<span data-ttu-id="d9261-185">NPS 服務會根據來自 Shv 的 Sohr 和設定的健康情況原則，建立系統健康狀態回應的系統聲明 (SSoHR) ，指出 NAP 用戶端是否符合規範，以及是否包含來自 Shv 的 Sohr 集。</span><span class="sxs-lookup"><span data-stu-id="d9261-185">Based on the SoHRs from the SHVs and the configured health policies, the NPS service creates a System Statement of Health Response (SSoHR), which indicates whether the NAP client is compliant or noncompliant and includes the set of SoHRs from the SHVs.</span></span>

## <a name="system-health-validator-shv"></a><span data-ttu-id="d9261-186">系統健康狀態驗證 (SHV)</span><span class="sxs-lookup"><span data-stu-id="d9261-186">System Health Validator (SHV)</span></span>

<span data-ttu-id="d9261-187">SHV 會從 NAP 管理伺服器接收 SoH，並將系統健全狀況狀態資訊與所需的系統健全狀況狀態進行比較。</span><span class="sxs-lookup"><span data-stu-id="d9261-187">An SHV receives a SoH from the NAP Administration Server and compares the system health status information with the required system health state.</span></span> <span data-ttu-id="d9261-188">例如，如果 SoH 來自防毒軟體 SHA，並且包含最後一個病毒碼檔案的版本號碼，則對應的防毒軟體 SHV 可以檢查防毒軟體健康需求伺服器是否有最新的版本號碼，以驗證 NAP 用戶端的 SoH。</span><span class="sxs-lookup"><span data-stu-id="d9261-188">For example, if the SoH is from an antivirus SHA and contains the version number of the last virus signature file, the corresponding antivirus SHV can check with the antivirus health requirement server for the latest version number to validate the NAP client's SoH.</span></span>

<span data-ttu-id="d9261-189">SHV 會將 SoHR 傳回給 NAP 管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9261-189">The SHV returns an SoHR to the NAP Administration Server.</span></span> <span data-ttu-id="d9261-190">SoHR 可以包含有關 NAP 用戶端上對應 SHA 如何符合目前系統健康需求的資訊。</span><span class="sxs-lookup"><span data-stu-id="d9261-190">The SoHR can contain information about how the corresponding SHA on the NAP client can meet current system health requirements.</span></span> <span data-ttu-id="d9261-191">例如，防毒軟體 SHV 傳送的 SoHR 可指示 NAP 用戶端上的防毒軟體 SHA，根據名稱或 IP 位址，向特定的防毒軟體簽章伺服器要求最新版本的防毒軟體簽章檔案。</span><span class="sxs-lookup"><span data-stu-id="d9261-191">For example, the SoHR sent by the antivirus SHV could instruct the antivirus SHA on the NAP client to request the latest version of the antivirus signature file from a specific antivirus signature server by name or IP address.</span></span>

 

 




