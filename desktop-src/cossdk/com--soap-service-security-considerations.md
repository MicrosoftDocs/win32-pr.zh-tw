---
description: COM + SOAP 服務安全性考慮
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: COM + SOAP 服務安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a238860e154e9928672a64ef44f9db37e9c8ad2c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847549"
---
# <a name="com-soap-service-security-considerations"></a><span data-ttu-id="ce152-103">COM + SOAP 服務安全性考慮</span><span class="sxs-lookup"><span data-stu-id="ce152-103">COM+ SOAP Service Security Considerations</span></span>

<span data-ttu-id="ce152-104">COM + SOAP 服務取決於 IIS web 伺服器的安全性。</span><span class="sxs-lookup"><span data-stu-id="ce152-104">The COM+ SOAP service depends on the IIS web server for security.</span></span> <span data-ttu-id="ce152-105">即使在 [用戶端啟動的物件模式](accessing-xml-web-services-in-cao-mode.md)中，COM + RPC 也不會傳輸用戶端身分識別，因此無法使用以角色為基礎的安全性或 DCOM 所提供的任何其他安全性功能。</span><span class="sxs-lookup"><span data-stu-id="ce152-105">Even in [client-activated object mode](accessing-xml-web-services-in-cao-mode.md), a COM+ RPC does not transmit the client identity and therefore cannot make use of role-based security or any other security feature provided by DCOM.</span></span> <span data-ttu-id="ce152-106">如果您想要協助保護您的 XML web 服務所傳送之資料的隱私權，或協助保護您的 XML web service 免于未經授權的存取，您可以將 IIS 設定為根據用戶端 IP 位址限制 XML web service 的存取，或要求用戶端出示數位憑證來驗證其身分識別。</span><span class="sxs-lookup"><span data-stu-id="ce152-106">If you want to help protect the privacy of data transmitted to and from your XML web service, or to help protect your XML web service from unauthorized access, you can configure IIS to limit access to an XML web service based on a clients IP address or to require a client to present a digital certificate to verify its identity.</span></span> <span data-ttu-id="ce152-107">如果您未限制存取，任何可以與 web 伺服器通訊的用戶端都可以存取您的 XML web service。</span><span class="sxs-lookup"><span data-stu-id="ce152-107">If you do not limit access, any client that can communicate with your web server can access your XML web service.</span></span>

<span data-ttu-id="ce152-108">您可以設定 IIS 使用公開金鑰加密 SSL 或 TLS 通訊協定，將 XML web service 與用戶端的通訊加密。</span><span class="sxs-lookup"><span data-stu-id="ce152-108">You can configure IIS to encrypt your XML web service communications with clients by using public key encryption SSL or TLS protocols.</span></span> <span data-ttu-id="ce152-109">如果您不加密 SOAP 通訊，在用戶端與伺服器之間交換的資料可能會由協力廠商觀察到任何透過其傳送 SOAP 通訊之網路的存取;視網路拓撲而定，這可能是小型 LAN 或可能是網際網路。</span><span class="sxs-lookup"><span data-stu-id="ce152-109">If you do not encrypt SOAP communications, data exchanged between a client and server could be observed by a third party with access to any network over which the SOAP communication travels; depending on network topology, this might be a small LAN or it might be the Internet.</span></span>

<span data-ttu-id="ce152-110">根據預設，會在 HTTP 埠 (80) 接收未加密的 SOAP 通訊，並在 HTTPS 埠 (443) 接收加密的 SOAP 通訊。</span><span class="sxs-lookup"><span data-stu-id="ce152-110">By default, unencrypted SOAP communications are received at the HTTP port (80) and encrypted SOAP communications are received at the HTTPS port (443).</span></span> <span data-ttu-id="ce152-111">若要讓用戶端成功存取 XML web service，用戶端與伺服器之間的所有防火牆都必須設定為允許 TCP SYN 封包到達適當的伺服器埠。</span><span class="sxs-lookup"><span data-stu-id="ce152-111">For a client to successfully access an XML web service, any firewalls between the client and the server must be configured to allow TCP SYN packets to reach the appropriate server port.</span></span> <span data-ttu-id="ce152-112">相反地，若要限制存取 XML web service，防火牆系統管理員可以選擇關閉這些埠。</span><span class="sxs-lookup"><span data-stu-id="ce152-112">Conversely, to limit access to XML web services, a firewall administrator may choose to close these ports.</span></span>

<span data-ttu-id="ce152-113">公開為 XML web service 之 COM 元件的預設安全性設定，會根據安裝的 Microsoft .NET Framework 版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ce152-113">The default security settings for a COM component exposed as an XML web service differ depending on which version of the Microsoft .NET Framework is installed.</span></span> <span data-ttu-id="ce152-114">如果已安裝1.0 版，則根據預設，XML web service 不是安全的;接受所有呼叫，且不使用加密。</span><span class="sxs-lookup"><span data-stu-id="ce152-114">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="ce152-115">如果已安裝1.1 版或更新版本，則根據預設，XML web service 是安全的;呼叫端必須經過驗證，而且需要加密。</span><span class="sxs-lookup"><span data-stu-id="ce152-115">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

<span data-ttu-id="ce152-116">受保護的 XML web service 不支援透過 WSDL 的 WKO 存取。</span><span class="sxs-lookup"><span data-stu-id="ce152-116">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="ce152-117">相反地，安裝 .NET Framework 1.1 版的用戶端可以使用 CAO 模式來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ce152-117">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="ce152-118">如果協力廠商用戶端需要透過 WSDL 存取您的 XML web service，您必須允許匿名存取。</span><span class="sxs-lookup"><span data-stu-id="ce152-118">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

<span data-ttu-id="ce152-119">公開為 XML web service 的 COM 元件預設會以匿名使用者的許可權來執行， (不會使用其呼叫端) 的許可權。</span><span class="sxs-lookup"><span data-stu-id="ce152-119">A COM component exposed as an XML web service runs by default with the permissions of the anonymous user (not with the permissions of its caller).</span></span> <span data-ttu-id="ce152-120">您可以將 IIS 設定為以不同的使用者的形式執行 XML web service;有時可能是必要的，因為您的元件使用的是匿名使用者沒有存取權的檔案或其他資源。</span><span class="sxs-lookup"><span data-stu-id="ce152-120">You can configure IIS to run the XML web service as a different user; this may sometimes be necessary because your component uses files or other resources to which the anonymous user does not have access.</span></span> <span data-ttu-id="ce152-121">不過，您應該一律嘗試以最少的許可權來執行您的元件，以限制惡意呼叫端可能造成的損害。</span><span class="sxs-lookup"><span data-stu-id="ce152-121">Nevertheless, you should always try to run your component with the fewest privileges possible, to limit the damage a malicious caller might cause.</span></span>

> [!Note]  
> <span data-ttu-id="ce152-122">因為您透過 XML web service 公開的方法可能會向惡意呼叫端公開，所以您應該一律務必驗證它所相依的任何輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ce152-122">Because a method you exposed via an XML web service could potentially be exposed to malicious callers, you should always be sure to validate any input parameters on which it depends.</span></span>

 

<span data-ttu-id="ce152-123">如需有關如何設定特定 XML web service 安全性設定的詳細指示，請參閱 [保護 XML Web 服務](securing-xml-web-services.md)。</span><span class="sxs-lookup"><span data-stu-id="ce152-123">For detailed instructions on how to configure specific XML web service security settings, see [Securing XML Web Services](securing-xml-web-services.md).</span></span>

<span data-ttu-id="ce152-124">**將安全的 SOAP 應用程式轉換成不安全的 SOAP 應用程式**</span><span class="sxs-lookup"><span data-stu-id="ce152-124">**To convert a secure SOAP application to an unsecure SOAP application**</span></span>

1.  <span data-ttu-id="ce152-125">開啟 Internet Information Services (IIS) 系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="ce152-125">Open the Internet Information Services (IIS) administration tool.</span></span>
2.  <span data-ttu-id="ce152-126">找出應用程式的虛擬目錄，然後開啟 [ **屬性** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ce152-126">Locate the virtual directory for the application and open the **Properties** dialog box.</span></span>
3.  <span data-ttu-id="ce152-127">勾選 [**檔**] 索引標籤上的 [**啟用預設內容] 頁面**。</span><span class="sxs-lookup"><span data-stu-id="ce152-127">Check **Enable default content page** on the **Documents** tab.</span></span>
4.  <span data-ttu-id="ce152-128">在 [**目錄安全性**] 索引標籤中，按一下 [**匿名存取及驗證控制**] 底下的 [**編輯**</span><span class="sxs-lookup"><span data-stu-id="ce152-128">From the **Directory Security** tab click **Edit** under **Anonymous access and authentication control**.</span></span>
5.  <span data-ttu-id="ce152-129">核取 [ **匿名存取** ] 以啟用匿名存取，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="ce152-129">Check **Anonymous access** to enable anonymous access and click **OK**.</span></span>
6.  <span data-ttu-id="ce152-130">按一下 [**安全通訊**] 下的 [**編輯**]。</span><span class="sxs-lookup"><span data-stu-id="ce152-130">Click **Edit** under **Secure communications**.</span></span>
7.  <span data-ttu-id="ce152-131">取消核取 [ **需要安全通道 (SSL)** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="ce152-131">Uncheck the **Require secure channel (SSL)** checkbox.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce152-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce152-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce152-133">COM + SOAP 服務總覽</span><span class="sxs-lookup"><span data-stu-id="ce152-133">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> </dl>

 

 



