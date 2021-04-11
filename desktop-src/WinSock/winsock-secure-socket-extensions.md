---
description: Winsock 的安全通訊端延伸模組可讓通訊端應用程式透過網路控制其流量的安全性。
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Winsock 安全通訊端擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026208"
---
# <a name="winsock-secure-socket-extensions"></a><span data-ttu-id="6acb3-103">Winsock 安全通訊端擴充功能</span><span class="sxs-lookup"><span data-stu-id="6acb3-103">Winsock Secure Socket Extensions</span></span>

<span data-ttu-id="6acb3-104">Winsock 的安全通訊端延伸模組可讓通訊端應用程式透過網路控制其流量的安全性。</span><span class="sxs-lookup"><span data-stu-id="6acb3-104">The secure socket extensions to Winsock allow a socket application to control the security of their traffic over a network.</span></span> <span data-ttu-id="6acb3-105">這些延伸模組可讓應用程式針對其網路流量提供安全性原則和需求，以及查詢所套用的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6acb3-105">These extensions allow an application to provide security policy and requirements for their network traffic, and query the security settings applied.</span></span> <span data-ttu-id="6acb3-106">例如，應用程式可以使用這些擴充功能來查詢對等安全性權杖，以用來執行應用層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="6acb3-106">For example, an application can use these extensions to query the peer security token that can be used to perform application level access checks.</span></span>

<span data-ttu-id="6acb3-107">安全通訊端擴充功能的目的是要將 IPsec 所提供的服務和其他安全性通訊協定與 Winsock 架構整合。</span><span class="sxs-lookup"><span data-stu-id="6acb3-107">The secure socket extensions are intended to integrate the services provided by IPsec and other security protocols with the Winsock framework.</span></span> <span data-ttu-id="6acb3-108">在 Windows Vista 之前的 windows Server 2003 和 Windows XP 上，系統管理員已透過本機和網域原則設定 IPsec。</span><span class="sxs-lookup"><span data-stu-id="6acb3-108">Prior to Windows Vista, on Windows Server 2003 and Windows XP, IPsec has been configured by an administrator via local and domain policies.</span></span> <span data-ttu-id="6acb3-109">在 Windows Vista 上，安全通訊端延伸模組會改為允許應用程式完全或部分設定和控制其在通訊端層級的網路流量安全性。</span><span class="sxs-lookup"><span data-stu-id="6acb3-109">On Windows Vista, the secure socket extensions instead allow applications to entirely or partially configure and control the security of their network traffic at the socket level.</span></span>

<span data-ttu-id="6acb3-110">應用程式已可使用公用 Api （例如 IPsec 管理、Windows 篩選平台和安全性支援提供者介面 (SSPI) ）來保護網路流量。</span><span class="sxs-lookup"><span data-stu-id="6acb3-110">Applications can already secure network traffic by using public APIs, such as IPsec management, Windows Filtering Platform and Security Support Provider Interface (SSPI).</span></span> <span data-ttu-id="6acb3-111">不過，使用這些 Api 可能會讓應用程式更難開發，而且可能會使設定和部署變得更困難。</span><span class="sxs-lookup"><span data-stu-id="6acb3-111">However, using these APIs may make the application more difficult to develop, and may make it more difficult to configure and deploy.</span></span> <span data-ttu-id="6acb3-112">Winsock 安全通訊端擴充功能的設計目的是為了簡化需要安全網路流量的網路應用程式開發，讓 Winsock 處理大部分的複雜度。</span><span class="sxs-lookup"><span data-stu-id="6acb3-112">The Winsock secure socket extensions have been designed to simplify the development of network applications that require secure network traffic by letting Winsock handle most of the complexity.</span></span>

<span data-ttu-id="6acb3-113">這些安全通訊端擴充功能可在 Windows Vista 和更新版本上使用。</span><span class="sxs-lookup"><span data-stu-id="6acb3-113">These secure socket extensions are available on Windows Vista and later.</span></span>

## <a name="secure-socket-functions"></a><span data-ttu-id="6acb3-114">安全通訊端函式</span><span class="sxs-lookup"><span data-stu-id="6acb3-114">Secure Socket Functions</span></span>

<span data-ttu-id="6acb3-115">安全通訊端擴充功能如下所示：</span><span class="sxs-lookup"><span data-stu-id="6acb3-115">The secure socket extension functions are as follows:</span></span>

-   [<span data-ttu-id="6acb3-116">**WSADeleteSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="6acb3-116">**WSADeleteSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [<span data-ttu-id="6acb3-117">**WSAImpersonateSocketPeer**</span><span class="sxs-lookup"><span data-stu-id="6acb3-117">**WSAImpersonateSocketPeer**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [<span data-ttu-id="6acb3-118">**WSAQuerySocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="6acb3-118">**WSAQuerySocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [<span data-ttu-id="6acb3-119">**WSARevertImpersonation**</span><span class="sxs-lookup"><span data-stu-id="6acb3-119">**WSARevertImpersonation**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [<span data-ttu-id="6acb3-120">**WSASetSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="6acb3-120">**WSASetSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [<span data-ttu-id="6acb3-121">**WSASetSocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="6acb3-121">**WSASetSocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> <span data-ttu-id="6acb3-122">安全通訊端函式目前只支援 IPsec 通訊協定，可在 Windows Vista 和更新版本上使用。</span><span class="sxs-lookup"><span data-stu-id="6acb3-122">The secure socket functions currently support only the IPsec protocol and are available on Windows Vista and later.</span></span>

 

<span data-ttu-id="6acb3-123">安全通訊端函數所使用的結構和列舉如下：</span><span class="sxs-lookup"><span data-stu-id="6acb3-123">The structures and enumerations used by the secure socket functions are as follows:</span></span>

-   [<span data-ttu-id="6acb3-124">**通訊端 \_ 對等 \_ 目標 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="6acb3-124">**SOCKET\_PEER\_TARGET\_NAME**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [<span data-ttu-id="6acb3-125">**通訊端 \_ 安全性 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="6acb3-125">**SOCKET\_SECURITY\_PROTOCOL**</span></span>](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [<span data-ttu-id="6acb3-126">**通訊端 \_ 安全性 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6acb3-126">**SOCKET\_SECURITY\_QUERY\_INFO**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [<span data-ttu-id="6acb3-127">**通訊端 \_ 安全性 \_ 查詢 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="6acb3-127">**SOCKET\_SECURITY\_QUERY\_TEMPLATE**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [<span data-ttu-id="6acb3-128">**通訊端 \_ 安全性 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="6acb3-128">**SOCKET\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [<span data-ttu-id="6acb3-129">**通訊端 \_ 安全性 \_ 設定 \_ IPSEC**</span><span class="sxs-lookup"><span data-stu-id="6acb3-129">**SOCKET\_SECURITY\_SETTINGS\_IPSEC**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

<span data-ttu-id="6acb3-130">安全通訊端函式很容易用於一般的應用程式，而且對於需要高度控制安全性的應用程式來說，具有足夠的彈性。</span><span class="sxs-lookup"><span data-stu-id="6acb3-130">The secure socket functions are simple to use for normal applications and are flexible enough for applications that need a high degree of control over their security.</span></span> <span data-ttu-id="6acb3-131">這些函式可讓您將基礎安全性機制隱藏在應用程式之外。</span><span class="sxs-lookup"><span data-stu-id="6acb3-131">These functions make it possible to keep the underlying security mechanism hidden from the application.</span></span> <span data-ttu-id="6acb3-132">應用程式可以指定一般安全性需求，並讓系統管理員控制用來支援需求的安全性通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6acb3-132">An application can specify generic security requirements and let the administrator control the security protocol that is used to support the requirements.</span></span> <span data-ttu-id="6acb3-133">雖然可以擴充這些函式以新增其他安全性通訊協定，但目前只有 IPsec 會與安全通訊端功能整合。</span><span class="sxs-lookup"><span data-stu-id="6acb3-133">While it is possible to extend these functions to add other security protocols, currently only IPsec integrates with the secure socket functions.</span></span>

<span data-ttu-id="6acb3-134">[**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)函式可讓應用程式在建立連接之前啟用安全性並套用安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6acb3-134">The [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) function allows an application to enable security and apply security settings before a connection is established.</span></span>

<span data-ttu-id="6acb3-135">[**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)函數可讓應用程式指定對應至對等實體的目標名稱。</span><span class="sxs-lookup"><span data-stu-id="6acb3-135">The [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) function allows an application to specify the target name corresponding to a peer entity.</span></span> <span data-ttu-id="6acb3-136">在驗證對等時，所選取的安全性通訊協定會使用這類資訊。</span><span class="sxs-lookup"><span data-stu-id="6acb3-136">The selected security protocol will use this information when authenticating the peer.</span></span> <span data-ttu-id="6acb3-137">這項功能解決了受信任攔截式攻擊的疑慮。</span><span class="sxs-lookup"><span data-stu-id="6acb3-137">This feature addresses concerns about trusted man-in-the-middle attacks.</span></span>

<span data-ttu-id="6acb3-138">[**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)函式是用來刪除先前為通訊端指定的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="6acb3-138">The [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) function is used to delete a previously specified peer name for a socket.</span></span>

<span data-ttu-id="6acb3-139">建立連線之後， [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) 函式可讓應用程式查詢連接的安全性屬性，其中可包含對等存取或電腦存取權杖。</span><span class="sxs-lookup"><span data-stu-id="6acb3-139">After a connection is established, the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function allows an application to query the security properties of the connection, which can include the peer access or computer access token.</span></span>

<span data-ttu-id="6acb3-140">建立連線之後， [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) 函式可讓應用程式模擬對應至通訊端對等的安全性主體，以執行應用層級授權。</span><span class="sxs-lookup"><span data-stu-id="6acb3-140">After a connection is established, the [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) function allows an application to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.</span></span>

<span data-ttu-id="6acb3-141">[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)可讓應用程式終止通訊端對等互連的模擬。</span><span class="sxs-lookup"><span data-stu-id="6acb3-141">The [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) allows an application to terminate the impersonation of a socket peer.</span></span>

## <a name="secure-socket-architecture"></a><span data-ttu-id="6acb3-142">安全通訊端架構</span><span class="sxs-lookup"><span data-stu-id="6acb3-142">Secure Socket Architecture</span></span>

![winsock 安全通訊端擴充功能的基本架構](images/ss-arch.png)

-   <span data-ttu-id="6acb3-144">應用程式會呼叫安全通訊端函數來設定或查詢通訊端的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="6acb3-144">An application calls the secure socket functions to set or query security settings for a socket.</span></span>
-   <span data-ttu-id="6acb3-145">安全通訊端函式是一組型別安全的擴充函式，會使用 Windows Vista 和更新版本上可用之 *dwIoControlCode* 參數的新定義值，將呼叫包裝至 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)函式。</span><span class="sxs-lookup"><span data-stu-id="6acb3-145">The secure socket functions are a set of type-safe extension functions that wrap calls to the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using newly-defined values for the *dwIoControlCode* parameter available on Windows Vista and later.</span></span> <span data-ttu-id="6acb3-146">這些 IOCTLs 由網路堆疊處理。</span><span class="sxs-lookup"><span data-stu-id="6acb3-146">These IOCTLs are handled by the network stack.</span></span>
-   <span data-ttu-id="6acb3-147">網路堆疊會將 [應用層強制執行 (ALE) ](../fwp/application-layer-enforcement--ale-.md) 以及端點控制碼的呼叫導向。</span><span class="sxs-lookup"><span data-stu-id="6acb3-147">The network stack will direct the call to [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md) along with the endpoint handle.</span></span> <span data-ttu-id="6acb3-148">針對 [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)、 [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)和 [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) 函式，ALE 會在本機端點上設定應用程式的設定。</span><span class="sxs-lookup"><span data-stu-id="6acb3-148">For the [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname), and [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) functions, ALE will configure the application's settings on the local endpoint.</span></span> <span data-ttu-id="6acb3-149">針對 [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) 函式，ALE 將會從適用的本機和遠端端點讀取要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="6acb3-149">For the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function, ALE will read the requested information from applicable local and remote endpoints.</span></span>
-   <span data-ttu-id="6acb3-150">根據通訊端事件、應用層強制執行 (ALE) 會使用 Windows 篩選平台來強制執行安全通訊端架構的原則。</span><span class="sxs-lookup"><span data-stu-id="6acb3-150">Based on socket events, Application Layer Enforcement (ALE) enforces policies for the secure socket architecture using the Windows Filtering Platform.</span></span> <span data-ttu-id="6acb3-151">如需詳細資訊，請參閱 [關於 Windows 篩選平台](../fwp/about-windows-filtering-platform.md) 和 [應用層強制執行 (ALE) ](../fwp/application-layer-enforcement--ale-.md)。</span><span class="sxs-lookup"><span data-stu-id="6acb3-151">For more information, see [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6acb3-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="6acb3-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6acb3-153">關於 Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="6acb3-153">About Windows Filtering Platform</span></span>](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[<span data-ttu-id="6acb3-154">使用安全通訊端延伸模組的 Advanced Winsock 範例</span><span class="sxs-lookup"><span data-stu-id="6acb3-154">Advanced Winsock Samples Using Secure Socket Extensions</span></span>](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="6acb3-155">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="6acb3-155">Application Layer Enforcement (ALE)</span></span>](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="6acb3-156">IPsec 設定</span><span class="sxs-lookup"><span data-stu-id="6acb3-156">IPsec Configuration</span></span>](../fwp/ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="6acb3-157">IPsec 功能</span><span class="sxs-lookup"><span data-stu-id="6acb3-157">IPsec Functions</span></span>](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[<span data-ttu-id="6acb3-158">安全 Winsock 程式設計</span><span class="sxs-lookup"><span data-stu-id="6acb3-158">Secure Winsock Programming</span></span>](secure-winsock-programming.md)
</dt> <dt>

[<span data-ttu-id="6acb3-159">安全性支援提供者介面 (SSPI)</span><span class="sxs-lookup"><span data-stu-id="6acb3-159">Security Support Provider Interface (SSPI)</span></span>](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[<span data-ttu-id="6acb3-160">使用安全通訊端擴充功能</span><span class="sxs-lookup"><span data-stu-id="6acb3-160">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="6acb3-161">Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="6acb3-161">Windows Filtering Platform</span></span>](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[<span data-ttu-id="6acb3-162">Windows 篩選平台 API 函式</span><span class="sxs-lookup"><span data-stu-id="6acb3-162">Windows Filtering Platform API Functions</span></span>](../fwp/fwp-functions.md)
</dt> </dl>

 

 
