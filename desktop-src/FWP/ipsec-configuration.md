---
title: IPsec 設定
description: Windows 篩選平台 (WFP) 是具有 Advanced Security 之 Windows 防火牆的基礎平臺。
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933181"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="f7893-103">IPsec 設定</span><span class="sxs-lookup"><span data-stu-id="f7893-103">IPsec Configuration</span></span>

<span data-ttu-id="f7893-104">Windows 篩選平台 (WFP) 是具有 Advanced Security 之 Windows 防火牆的基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="f7893-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="f7893-105">WFP 可用來設定網路篩選規則，其中包括使用 IPsec 保護網路流量的規則。</span><span class="sxs-lookup"><span data-stu-id="f7893-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="f7893-106">應用程式開發人員可以使用 WFP API 直接設定 IPsec，以利用更細微的網路流量篩選模型，而不是透過適用于具有 Advanced Security 之 Windows 防火牆的 Microsoft Management Console (MMC) 嵌入式管理單元所公開的模型。</span><span class="sxs-lookup"><span data-stu-id="f7893-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="f7893-107">什麼是 IPsec</span><span class="sxs-lookup"><span data-stu-id="f7893-107">What is IPsec</span></span>

<span data-ttu-id="f7893-108">網際網路通訊協定安全性 (IPsec) 是一組安全性通訊協定，可用來跨網際網路傳輸 IP 封包。</span><span class="sxs-lookup"><span data-stu-id="f7893-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="f7893-109">IPsec 對於所有 IPv6 執行都是必要的，而針對 IPv4 則是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f7893-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="f7893-110">安全的 IP 流量有兩個選用的 IPsec 標頭，可識別套用至 IP 封包的密碼編譯保護類型，並包含解碼受保護封包的資訊。</span><span class="sxs-lookup"><span data-stu-id="f7893-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="f7893-111">封裝安全性承載 (ESP) 標頭是用來執行驗證和選擇性加密，以提供隱私權和保護以防止惡意修改。</span><span class="sxs-lookup"><span data-stu-id="f7893-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="f7893-112">它可用於流經 (NAT) 路由器的網路位址轉譯的流量。</span><span class="sxs-lookup"><span data-stu-id="f7893-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="f7893-113">驗證標頭 (AH) 僅用來保護執行驗證的惡意修改。</span><span class="sxs-lookup"><span data-stu-id="f7893-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="f7893-114">它無法用於流經 NAT 路由器的流量。</span><span class="sxs-lookup"><span data-stu-id="f7893-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="f7893-115">如需 IPsec 的詳細資訊，另請參閱：</span><span class="sxs-lookup"><span data-stu-id="f7893-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="f7893-116">[IPsec 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="f7893-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="f7893-117">什麼是 IKE</span><span class="sxs-lookup"><span data-stu-id="f7893-117">What is IKE</span></span>

<span data-ttu-id="f7893-118">網際網路金鑰交換 (IKE) 是 IPsec 通訊協定集一部分的金鑰交換通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f7893-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="f7893-119">IKE 是在設定安全連線時使用，並在不需要使用者介入的情況下完成安全的秘密金鑰和其他保護相關參數的交換。</span><span class="sxs-lookup"><span data-stu-id="f7893-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="f7893-120">如需有關 IKE 的詳細資訊，另請參閱：</span><span class="sxs-lookup"><span data-stu-id="f7893-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="f7893-121">[網際網路金鑰交換](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="f7893-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="f7893-122">什麼是 AuthIP</span><span class="sxs-lookup"><span data-stu-id="f7893-122">What is AuthIP</span></span>

<span data-ttu-id="f7893-123">驗證的網際網路通訊協定 (AuthIP) 是新的金鑰交換通訊協定，可依下列方式展開 IKE。</span><span class="sxs-lookup"><span data-stu-id="f7893-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="f7893-124">雖然 IKE 只支援電腦驗證認證，但 AuthIP 也支援：</span><span class="sxs-lookup"><span data-stu-id="f7893-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="f7893-125">使用者認證： NTLM、Kerberos、憑證。</span><span class="sxs-lookup"><span data-stu-id="f7893-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="f7893-126">網路存取保護 (NAP) 健康情況憑證。</span><span class="sxs-lookup"><span data-stu-id="f7893-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="f7893-127">匿名認證，用於選擇性驗證。</span><span class="sxs-lookup"><span data-stu-id="f7893-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="f7893-128">認證的組合;例如，電腦和使用者 Kerberos 認證的組合。</span><span class="sxs-lookup"><span data-stu-id="f7893-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="f7893-129">AuthIP 具有驗證重試機制，可在連線失敗之前確認所有已設定的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="f7893-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="f7893-130">AuthIP 可以搭配安全通訊端使用，以執行以應用程式為基礎的 IPsec 安全流量。</span><span class="sxs-lookup"><span data-stu-id="f7893-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="f7893-131">它提供：</span><span class="sxs-lookup"><span data-stu-id="f7893-131">It provides:</span></span>

-   <span data-ttu-id="f7893-132">每一通訊端的驗證和加密。</span><span class="sxs-lookup"><span data-stu-id="f7893-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="f7893-133">如需詳細資訊，請參閱 [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) 。</span><span class="sxs-lookup"><span data-stu-id="f7893-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="f7893-134">用戶端模擬。</span><span class="sxs-lookup"><span data-stu-id="f7893-134">Client impersonation.</span></span> <span data-ttu-id="f7893-135"> (IPsec 會模擬建立通訊端所用的安全性內容。 ) </span><span class="sxs-lookup"><span data-stu-id="f7893-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="f7893-136">輸入和輸出對等名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="f7893-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="f7893-137">如需詳細資訊，請參閱 [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) 。</span><span class="sxs-lookup"><span data-stu-id="f7893-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="f7893-138">如需 AuthIP 的詳細資訊，另請參閱：</span><span class="sxs-lookup"><span data-stu-id="f7893-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="f7893-139">Windows Vista 中的 AuthIP</span><span class="sxs-lookup"><span data-stu-id="f7893-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="f7893-140">什麼是 IPsec 原則</span><span class="sxs-lookup"><span data-stu-id="f7893-140">What is an IPsec Policy</span></span>

<span data-ttu-id="f7893-141">IPsec 原則是一組規則，可決定需要使用 IPsec 保護哪些類型的 IP 流量，以及如何保護該流量。</span><span class="sxs-lookup"><span data-stu-id="f7893-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="f7893-142">一次只能在一部電腦上使用一個 IPsec 原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="f7893-143">若要深入瞭解如何執行 IPsec 原則，請開啟 [本機安全性原則] MMC 嵌入式管理單元， (secpol.msc]) 中按 F1 鍵顯示 [說明]，然後選取 [目錄] 中的 [建立和使用 IPsec 原則]。</span><span class="sxs-lookup"><span data-stu-id="f7893-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="f7893-144">如需 IPsec 原則的詳細資訊，另請參閱：</span><span class="sxs-lookup"><span data-stu-id="f7893-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="f7893-145">[IPsec 原則概念總覽](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="f7893-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="f7893-146">[IPsec 原則的描述](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="f7893-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="f7893-147">如何使用 WFP 設定 IPsec 原則</span><span class="sxs-lookup"><span data-stu-id="f7893-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="f7893-148">Microsoft 的 IPsec 執行會使用 Windows 篩選平台來設定 IPsec 原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="f7893-149">IPsec 原則是藉由在不同的 WFP 層級新增篩選準則來執行，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f7893-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="f7893-150">在 FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 層新增篩選器，以指定在主要模式 (MM) 交換期間， (IKE/AuthIP) 的加密模組所使用的協商原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="f7893-151">驗證方法和密碼編譯演算法是在這些層級指定。</span><span class="sxs-lookup"><span data-stu-id="f7893-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="f7893-152">在 FWPM \_ 層 \_ 中，IPSEC \_ V {4 \| 6} 層新增篩選器，以在快速模式 (QM) 和延伸模式 (EM) 交換時，指定加密模組所使用的協商原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="f7893-153">IPsec 標頭 (AH/ESP) 和密碼編譯演算法是在這些層級指定。</span><span class="sxs-lookup"><span data-stu-id="f7893-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="f7893-154">協商原則會指定為與篩選準則相關聯的原則提供者內容。</span><span class="sxs-lookup"><span data-stu-id="f7893-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="f7893-155">加密模組會根據流量特性列舉原則提供者內容，並取得要用於安全性協調的原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="f7893-156">您可以使用 WFP API 來直接指定 (SAs) 的安全性關聯，進而忽略金鑰安全模組的協商原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="f7893-157">在 FWPM \_ 層的 \_ 輸入 \_ 傳輸 \_ v {4 \| 6} 和 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ v {4 \| 6} 層中，會新增可叫用標注並決定應保護哪些流量流程的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="f7893-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="f7893-158">在 FWPM \_ 層的 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 個層級新增篩選準則，以執行身分識別篩選和個別應用程式原則。</span><span class="sxs-lookup"><span data-stu-id="f7893-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="f7893-159">下圖說明各種 WFP 元件的互動，與 IPsec 作業有關。</span><span class="sxs-lookup"><span data-stu-id="f7893-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![使用 windows 篩選平臺進行 ipsec 設定](images/ipsec-configuration.jpg)

<span data-ttu-id="f7893-161">IPsec 一經設定，就會與 WFP 整合，並藉由提供資訊，以在應用層強制執行 (ALE) 授權層級的篩選準則，來擴充 WFP 篩選功能。</span><span class="sxs-lookup"><span data-stu-id="f7893-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="f7893-162">例如，IPsec 提供遠端使用者和遠端電腦身分識別，而 WFP 會在 ALE connect 和接受授權層級公開。</span><span class="sxs-lookup"><span data-stu-id="f7893-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="f7893-163">這項資訊可用於以 WFP 為基礎的防火牆執行，以進行更細緻的遠端身分識別授權。</span><span class="sxs-lookup"><span data-stu-id="f7893-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="f7893-164">以下是可能使用 IPsec 來執行的隔離原則範例：</span><span class="sxs-lookup"><span data-stu-id="f7893-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="f7893-165">FWPM \_ LAYER \_ IKEEXT \_ V {4 \| 6} 層– Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="f7893-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="f7893-166">FWPM \_ 層 \_ IPSEC \_ V {4 \| 6} 層– AH/sha-1。</span><span class="sxs-lookup"><span data-stu-id="f7893-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="f7893-167">FWPM \_ 圖層 \_ 輸入 \_ 傳輸 \_ v {4 \| 6} 和 FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ v {4 \| 6} 層級-所有網路流量的協調探索。</span><span class="sxs-lookup"><span data-stu-id="f7893-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="f7893-168">FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6} 層-所有網路流量都需要 IPsec。</span><span class="sxs-lookup"><span data-stu-id="f7893-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7893-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7893-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f7893-170">**WFP 層**</span><span class="sxs-lookup"><span data-stu-id="f7893-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="f7893-171">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="f7893-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="f7893-172">ALE 層</span><span class="sxs-lookup"><span data-stu-id="f7893-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="f7893-173">**使用 WFP API 執行的 IPsec 原則案例：**</span><span class="sxs-lookup"><span data-stu-id="f7893-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="f7893-174">傳輸模式</span><span class="sxs-lookup"><span data-stu-id="f7893-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="f7893-175">協商探索傳輸模式</span><span class="sxs-lookup"><span data-stu-id="f7893-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="f7893-176">界限模式中的協商探索傳輸模式</span><span class="sxs-lookup"><span data-stu-id="f7893-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="f7893-177">通道模式</span><span class="sxs-lookup"><span data-stu-id="f7893-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="f7893-178">保證加密</span><span class="sxs-lookup"><span data-stu-id="f7893-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="f7893-179">遠端身分識別授權</span><span class="sxs-lookup"><span data-stu-id="f7893-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="f7893-180">手動 IPsec SAs</span><span class="sxs-lookup"><span data-stu-id="f7893-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="f7893-181">IKE/AuthIP 豁免</span><span class="sxs-lookup"><span data-stu-id="f7893-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="f7893-182">**IPsec 解決方案：**</span><span class="sxs-lookup"><span data-stu-id="f7893-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="f7893-183">[伺服器及網域隔離](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="f7893-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 