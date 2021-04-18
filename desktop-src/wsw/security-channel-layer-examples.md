---
title: 安全性通道層範例
description: 下列範例說明通道層的安全性。
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- 安全性範例
- 安全性範例，安裝程式
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968437"
---
# <a name="security-channel-layer-examples"></a><span data-ttu-id="23392-107">安全性通道層範例</span><span class="sxs-lookup"><span data-stu-id="23392-107">Security Channel Layer Examples</span></span>

<span data-ttu-id="23392-108">下列範例說明[通道層](channel-layer-overview.md)中的安全性</span><span class="sxs-lookup"><span data-stu-id="23392-108">The following examples illustrate security in the [Channel Layer](channel-layer-overview.md)</span></span>

<span data-ttu-id="23392-109">透過 TCP 的 Windows 傳輸安全性：用戶端： [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-109">Windows transport security over TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="23392-110">具名管道上的 Windows 傳輸安全性：用戶端： [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-110">Windows transport security over named pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="23392-111">SSL 傳輸安全性：用戶端： [HttpClientWithSslExample](httpclientwithsslexample.md)，伺服器： [HttpServerWithSslExample](httpserverwithsslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-111">SSL transport security: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span></span>

<span data-ttu-id="23392-112">透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)，伺服器： [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-112">Username over SSL mixed-mode security: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span></span>

<span data-ttu-id="23392-113">透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md)，伺服器： [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-113">Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span></span>

<span data-ttu-id="23392-114">透過 SSL 混合模式安全性的使用者名稱： [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-114">Username over SSL mixed-mode security: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span></span> <span data-ttu-id="23392-115">透過 SSL 混合模式安全性發出的權杖： [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-115">Issued token over SSL mixed-mode security: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span></span> <span data-ttu-id="23392-116">透過 SSL 混合模式安全性的 X509 憑證： [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="23392-116">X509 certificate over SSL mixed-mode security: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span></span>

## <a name="one-time-setup-for-security-samples"></a><span data-ttu-id="23392-117">安全性範例的 One-Time 設定</span><span class="sxs-lookup"><span data-stu-id="23392-117">One-Time Setup for Security Samples</span></span>

<span data-ttu-id="23392-118">若要執行 WWSAPI 安全性範例，您必須設定 SSL 的用戶端和伺服器憑證，以及用於 HTTP 標頭驗證的本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="23392-118">To run WWSAPI security examples, you need to set up the client and server certificates for SSL, as well as a local user account for HTTP header authentication.</span></span> <span data-ttu-id="23392-119">開始之前，您需要下列工具：</span><span class="sxs-lookup"><span data-stu-id="23392-119">Before you start, you need the following tools:</span></span>

-   <span data-ttu-id="23392-120">MakeCert.exe (適用于 Windows 7 SDK。 ) </span><span class="sxs-lookup"><span data-stu-id="23392-120">MakeCert.exe (Available in the Windows 7 SDK.)</span></span>
-   <span data-ttu-id="23392-121">從 Windows Server 2003 開始，Windows Sdk 中提供 CertUtil.exe 或 CertMgr.exe (CertUtil.exe。</span><span class="sxs-lookup"><span data-stu-id="23392-121">CertUtil.exe or CertMgr.exe (CertUtil.exe is available in the Windows SDKs starting with Windows Server 2003.</span></span> <span data-ttu-id="23392-122">CertMgr.exe 可在 Windows 7 SDK 中取得。</span><span class="sxs-lookup"><span data-stu-id="23392-122">CertMgr.exe is available in the Windows 7 SDK.</span></span> <span data-ttu-id="23392-123">您只需要其中一個工具。 ) </span><span class="sxs-lookup"><span data-stu-id="23392-123">You only need one of these tools.)</span></span>
-   <span data-ttu-id="23392-124">HttpCfg.exe： (只有在使用 Windows 2003 或 Windows XP 時才需要此。</span><span class="sxs-lookup"><span data-stu-id="23392-124">HttpCfg.exe: (You need this only if you are using Windows 2003 or Windows XP.</span></span> <span data-ttu-id="23392-125">這項工具適用于 Windows XP SP2 支援工具，也隨附于 Windows Server 2003 資源套件工具光碟。 ) </span><span class="sxs-lookup"><span data-stu-id="23392-125">This tool is available in Windows XP SP2 Support Tools and also comes with the Windows Server 2003 Resource Kit Tools CD.)</span></span>

<span data-ttu-id="23392-126">如果您藉由安裝 Windows 7 SDK 來取得 WWSAPI 的範例，您可以在% ProgramFiles% \\ Microsoft sdk Windows v2.0 bin 下找到 MakeCert.exe 和 CertMgr.exe \\ \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="23392-126">If you get the WWSAPI examples by installing the Windows 7 SDK, you can find the MakeCert.exe and CertMgr.exe under %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\bin.</span></span>

<span data-ttu-id="23392-127">如果您使用 Windows Vista 和更新版本) ，請從命令提示字元執行下列五步驟安裝 (提高許可權：</span><span class="sxs-lookup"><span data-stu-id="23392-127">Perform the following five-step setup from the command prompt (elevated if you are using Windows Vista and above):</span></span>

1.  <span data-ttu-id="23392-128">產生自我簽署憑證做為憑證授權單位單位 (CA) 或簽發者： **MakeCert.exe-Ss Root-Sr LocalMachine-n "CN = 假-Test-CA"-cy issuer-r-sk "CAKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="23392-128">Generate a self-signed certificate to be the certificate authority (CA) or issuer: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**</span></span>
2.  <span data-ttu-id="23392-129">使用先前的憑證作為簽發者來產生伺服器憑證： **MakeCert.exe-Ss my-Sr LocalMachine-n "CN = localhost"-天空 exchange-** -----ServerKeyContainer</span><span class="sxs-lookup"><span data-stu-id="23392-129">Generate a server certificate using the previous certificate as the issuer: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**</span></span>
3.  <span data-ttu-id="23392-130">藉由執行下列其中一個命令，並搜尋名為 localhost 的憑證（具有簽發者虛設-Test-CA），以找出伺服器憑證的40字元 SHA-1 雜湊)  (的指紋：</span><span class="sxs-lookup"><span data-stu-id="23392-130">Find the thumbprint (a 40-character SHA-1 hash) of the server certificate by running either of the following commands and search for the certificate named localhost with issuer Fake-Test-CA:</span></span>
    -   <span data-ttu-id="23392-131">**CertUtil.exe-儲存我的 localhost**</span><span class="sxs-lookup"><span data-stu-id="23392-131">**CertUtil.exe -store My localhost**</span></span>
    -   <span data-ttu-id="23392-132">**CertMgr.exe-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="23392-132">**CertMgr.exe -s -r LocalMachine My**</span></span>
4.  <span data-ttu-id="23392-133">使用 HTTP.SYS 註冊伺服器憑證的指紋，但不含空格：</span><span class="sxs-lookup"><span data-stu-id="23392-133">Register the server certificate?s thumbprint with no spaces with HTTP.SYS:</span></span>
    -   <span data-ttu-id="23392-134">在 Windows Vista 和更新版本上 ("appid" 選項是任意的 GUID) ： **Netsh.exe HTTP add sslcert ipport = 0.0.0.0： 8443 appid = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint></span><span class="sxs-lookup"><span data-stu-id="23392-134">On Windows Vista and above (the "appid" option is an arbitrary GUID): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint></span></span>
    -   <span data-ttu-id="23392-135">在 Windows XP 或2003上： **HttpCfg.exe 設定 ssl-i 0.0.0.0： 8443-h <40CharacterThumbprint>**</span><span class="sxs-lookup"><span data-stu-id="23392-135">On Windows XP or 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**</span></span>
5.  <span data-ttu-id="23392-136">建立本機使用者： **Net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/add**</span><span class="sxs-lookup"><span data-stu-id="23392-136">Create a local user: **Net user "TestUserForBasicAuth" "TstPWD@\*4Bsic" /add**</span></span>

<span data-ttu-id="23392-137">若要清除憑證、SSL 憑證系結和在先前步驟中建立的使用者帳戶，請執行下列命令。</span><span class="sxs-lookup"><span data-stu-id="23392-137">To clean up the certificates, SSL certificate binding and the user account created in the previous steps, run the following commands.</span></span> <span data-ttu-id="23392-138">請注意，如果有多個相同名稱的憑證，CertMgr.exe 將需要您的輸入，才能將其刪除。</span><span class="sxs-lookup"><span data-stu-id="23392-138">Note if there are multiple certificates of the same name, CertMgr.exe will need your input before deleting them.</span></span>

-   <span data-ttu-id="23392-139">**CertMgr.exe-del-c-n 假-測試-CA-s-r LocalMachine Root**</span><span class="sxs-lookup"><span data-stu-id="23392-139">**CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**</span></span>
-   <span data-ttu-id="23392-140">**CertMgr.exe-del-c-n localhost-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="23392-140">**CertMgr.exe -del -c -n localhost -s -r LocalMachine My**</span></span>
-   <span data-ttu-id="23392-141">**Netsh.exe HTTP delete sslcert ipport = 0.0.0.0： 8443 (或 HttpCfg.exe delete ssl-i 0.0.0.0： 8443)**</span><span class="sxs-lookup"><span data-stu-id="23392-141">**Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (or HttpCfg.exe delete ssl -i 0.0.0.0:8443)**</span></span>
-   <span data-ttu-id="23392-142">**Net user "TestUserForBasicAuth"/delete**</span><span class="sxs-lookup"><span data-stu-id="23392-142">**Net user "TestUserForBasicAuth" /delete**</span></span>

<span data-ttu-id="23392-143">請確定只有一個名為假-Test-CA 的根憑證。</span><span class="sxs-lookup"><span data-stu-id="23392-143">Make sure there is only one root certificate named Fake-Test-CA.</span></span> <span data-ttu-id="23392-144">如果您不確定，您可以使用上述的 [清除] 命令，一律安全地嘗試清除這些憑證 (並且在開始進行五個步驟的設定之前，先忽略錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="23392-144">If you are unsure, it?s always safe to try to clean up these certificates using the cleanup commands above (and ignore errors) before starting the five-step setup.</span></span>

 

 




