---
title: Windows 遠端管理的安裝和設定
description: 針對要執行 Windows 遠端管理 (WinRM) 腳本，以及針對 **winrm** 命令列工具執行資料操作，Windows 遠端管理 (winrm) 必須同時安裝及設定。
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: 4ebe4094984f237a3c8949392e3e9a6b47b8afe6
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/04/2021
ms.locfileid: "104509745"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a><span data-ttu-id="5d43d-103">Windows 遠端管理的安裝和設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-103">Installation and configuration for Windows Remote Management</span></span>

<span data-ttu-id="5d43d-104">針對要執行 Windows 遠端管理 (WinRM) 腳本，以及針對 **winrm** 命令列工具執行資料操作，Windows 遠端管理 (winrm) 必須同時安裝及設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-104">For Windows Remote Management (WinRM) scripts to run, and for the **Winrm** command-line tool to perform data operations, Windows Remote Management (WinRM) has to be both installed and configured.</span></span>

<span data-ttu-id="5d43d-105">這些元素也取決於 WinRM 設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-105">These elements also depend on WinRM configuration.</span></span>

- <span data-ttu-id="5d43d-106">[Windows 遠端 Shell](./windows-remote-management-glossary.md#w)命令列工具 (**Winrs**) 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-106">The [Windows Remote Shell](./windows-remote-management-glossary.md#w) command-line tool (**Winrs**).</span></span>
- <span data-ttu-id="5d43d-107">[事件轉送](./windows-remote-management-glossary.md#e)。</span><span class="sxs-lookup"><span data-stu-id="5d43d-107">[Event forwarding](./windows-remote-management-glossary.md#e).</span></span>
- <span data-ttu-id="5d43d-108">Windows PowerShell 2.0 遠端處理。</span><span class="sxs-lookup"><span data-stu-id="5d43d-108">Windows PowerShell 2.0 remoting.</span></span>

## <a name="where-winrm-is-installed"></a><span data-ttu-id="5d43d-109">安裝 WinRM 的位置</span><span class="sxs-lookup"><span data-stu-id="5d43d-109">Where WinRM is installed</span></span>

<span data-ttu-id="5d43d-110">WinRM 會自動與所有目前支援的 Windows 作業系統版本一起安裝。</span><span class="sxs-lookup"><span data-stu-id="5d43d-110">WinRM is automatically installed with all currently-supported versions of the Windows operating system.</span></span>

## <a name="configuration-of-winrm-and-ipmi"></a><span data-ttu-id="5d43d-111">Configuration WinRM 與 IPMI</span><span class="sxs-lookup"><span data-stu-id="5d43d-111">Configuration of WinRM and IPMI</span></span>

<span data-ttu-id="5d43d-112">這些 WinRM 和 [智慧型平臺管理介面 (IPMI) ](./windows-remote-management-glossary.md#i) [WMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 元件與作業系統一起安裝。</span><span class="sxs-lookup"><span data-stu-id="5d43d-112">These WinRM and [Intelligent Platform Management Interface (IPMI)](./windows-remote-management-glossary.md#i) [WMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) components are installed with the operating system.</span></span>

- <span data-ttu-id="5d43d-113">WinRM 服務會在 Windows Server 2008 上自動啟動，而在 Windows Vista 上的 wards (上，您需要以手動方式啟動服務) 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-113">The WinRM service starts automatically on Windows Server 2008 and on wards (on Windows Vista, you need to start the service manually).</span></span>
- <span data-ttu-id="5d43d-114">依預設， [不會設定](./windows-remote-management-glossary.md#l) 任何 WinRM 接聽程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-114">By default, no WinRM [listener](./windows-remote-management-glossary.md#l) is configured.</span></span> <span data-ttu-id="5d43d-115">即使 WinRM 服務正在執行，也無法接收或傳送要求資料 WS-Management 的通訊協定 [訊息](./windows-remote-management-glossary.md#m) 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-115">Even if the WinRM service is running, WS-Management protocol [messages](./windows-remote-management-glossary.md#m) that request data can't be received nor sent.</span></span>
- <span data-ttu-id="5d43d-116">網際網路連線防火牆 (ICF) 封鎖對埠的存取。</span><span class="sxs-lookup"><span data-stu-id="5d43d-116">Internet Connection Firewall (ICF) blocks access to ports.</span></span>

<span data-ttu-id="5d43d-117">請在命令提示字元中輸入下列命令，以使用 **Winrm** 命令來尋找接聽程式和位址。</span><span class="sxs-lookup"><span data-stu-id="5d43d-117">Use the **Winrm** command to locate listeners and the addresses by typing the following command at a command prompt.</span></span>

```console
winrm e winrm/config/listener
```

<span data-ttu-id="5d43d-118">若要檢查設定的狀態，請輸入下列命令。</span><span class="sxs-lookup"><span data-stu-id="5d43d-118">To check the state of configuration settings, type the following command.</span></span>

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a><span data-ttu-id="5d43d-119">快速預設設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-119">Quick default configuration</span></span>

<span data-ttu-id="5d43d-120">您可以在本機電腦上啟用 WS-Management 的通訊協定，並使用命令設定遠端系統管理的預設設定 `winrm quickconfig` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-120">You can enable the WS-Management protocol on the local computer, and set up the default configuration for remote management with the command `winrm quickconfig`.</span></span>

<span data-ttu-id="5d43d-121">`winrm quickconfig`命令 (或縮寫版本 `winrm qc`) 執行這些作業。</span><span class="sxs-lookup"><span data-stu-id="5d43d-121">The `winrm quickconfig` command (or the abbreviated version `winrm qc`) performs these operations.</span></span>

- <span data-ttu-id="5d43d-122">啟動 WinRM 服務，並將服務啟動類型設定為自動啟動。</span><span class="sxs-lookup"><span data-stu-id="5d43d-122">Starts the WinRM service, and sets the service startup type to auto-start.</span></span>
- <span data-ttu-id="5d43d-123">針對在任何 IP 位址上使用 HTTP 或 HTTPS 傳送和接收 WS-Management 通訊協定 [訊息](./windows-remote-management-glossary.md#m) 的埠設定接聽程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-123">Configures a listener for the ports that send and receive WS-Management protocol [messages](./windows-remote-management-glossary.md#m) using either HTTP or HTTPS on any IP address.</span></span>
- <span data-ttu-id="5d43d-124">定義 WinRM 服務的 ICF 例外狀況，並開啟 HTTP 和 HTTPS 的埠。</span><span class="sxs-lookup"><span data-stu-id="5d43d-124">Defines ICF exceptions for the WinRM service, and opens the ports for HTTP and HTTPS.</span></span>

> [!NOTE]
> <span data-ttu-id="5d43d-125">此 `winrm quickconfig` 命令只會針對目前的使用者設定檔建立防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="5d43d-125">The `winrm quickconfig` command creates a firewall exception only for the current user profile.</span></span> <span data-ttu-id="5d43d-126">如果防火牆設定檔因任何原因而變更，您應該執行 `winrm quickconfig` 以啟用新設定檔的防火牆例外，否則可能不會啟用例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5d43d-126">If the firewall profile is changed for any reason, you should run `winrm quickconfig` to enable the firewall exception for the new profile; otherwise, the exception might not be enabled.</span></span>

<span data-ttu-id="5d43d-127">若要取得自訂設定的相關資訊，請 `winrm help config` 在命令提示字元中輸入。</span><span class="sxs-lookup"><span data-stu-id="5d43d-127">To retrieve information about customizing a configuration, type `winrm help config` at a command prompt.</span></span>

### <a name="to-configure-winrm-with-default-settings"></a><span data-ttu-id="5d43d-128">使用預設設定來設定 WinRM</span><span class="sxs-lookup"><span data-stu-id="5d43d-128">To configure WinRM with default settings</span></span>

1. <span data-ttu-id="5d43d-129">`winrm quickconfig`在命令提示字元中輸入。</span><span class="sxs-lookup"><span data-stu-id="5d43d-129">Type `winrm quickconfig` at a command prompt.</span></span>

   <span data-ttu-id="5d43d-130">如果您不是在本機電腦系統管理員帳戶下執行，則必須從 [**開始**] 功能表選取 [**以系統管理員身分執行**]，或在命令提示字元中使用 **Runas** 命令。</span><span class="sxs-lookup"><span data-stu-id="5d43d-130">If you're not running under the local computer Administrator account, then you must either select **Run as Administrator** from the **Start** menu, or use the **Runas** command at a command prompt.</span></span>

2. <span data-ttu-id="5d43d-131">當工具顯示 [ **讓這些變更成為 \[ y/ \] n**] 時，請輸入 **y**。</span><span class="sxs-lookup"><span data-stu-id="5d43d-131">When the tool displays **Make these changes \[y/n\]?**, type **y**.</span></span>

   <span data-ttu-id="5d43d-132">如果設定成功，則會顯示下列輸出。</span><span class="sxs-lookup"><span data-stu-id="5d43d-132">If configuration is successful, then the following output is displayed.</span></span>

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. <span data-ttu-id="5d43d-133">保留 WinRM 用戶端和伺服器元件的預設設定，或進行自訂。</span><span class="sxs-lookup"><span data-stu-id="5d43d-133">Keep the default settings for client and server components of WinRM, or customize them.</span></span> <span data-ttu-id="5d43d-134">例如，您可能需要將特定遠端電腦新增至用戶端設定 TrustedHosts 清單。</span><span class="sxs-lookup"><span data-stu-id="5d43d-134">For example, you might need to add certain remote computers to the client configuration TrustedHosts list.</span></span>

   <span data-ttu-id="5d43d-135">當無法建立相互驗證時，您應該設定信任的主機清單。</span><span class="sxs-lookup"><span data-stu-id="5d43d-135">You should set up a trusted hosts list when mutual authentication can't be established.</span></span> <span data-ttu-id="5d43d-136">Kerberos 允許相互驗證，但不能在工作組 &mdash; 私人網路域中使用。</span><span class="sxs-lookup"><span data-stu-id="5d43d-136">Kerberos allows mutual authentication, but it can't be used in workgroups&mdash;only domains.</span></span> <span data-ttu-id="5d43d-137">為工作組設定受信任的主機時，最佳作法是讓清單盡可能受限制。</span><span class="sxs-lookup"><span data-stu-id="5d43d-137">A best practice when setting up trusted hosts for a workgroup is to make the list as restricted as possible.</span></span>

4. <span data-ttu-id="5d43d-138">輸入命令以建立 HTTPS 接聽程式 `winrm quickconfig -transport:https` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-138">Create an HTTPS listener by typing the command `winrm quickconfig -transport:https`.</span></span> <span data-ttu-id="5d43d-139">請注意，您必須開啟埠5986，HTTPS 傳輸才能運作。</span><span class="sxs-lookup"><span data-stu-id="5d43d-139">Be aware that you must open port 5986 for HTTPS transport to work.</span></span>

## <a name="listener-and-ws-management-protocol-default-settings"></a><span data-ttu-id="5d43d-140">接聽程式和 WS-Management 通訊協定預設設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-140">Listener and WS-Management protocol default settings</span></span>

<span data-ttu-id="5d43d-141">若要取得接聽程式設定，請 `winrm enumerate winrm/config/listener` 在命令提示字元中輸入。</span><span class="sxs-lookup"><span data-stu-id="5d43d-141">To get the listener configuration, type `winrm enumerate winrm/config/listener` at a command prompt.</span></span> <span data-ttu-id="5d43d-142">接聽程式是由傳輸 (HTTP 或 HTTPS) 和 IPv4 或 IPv6 位址所定義。</span><span class="sxs-lookup"><span data-stu-id="5d43d-142">Listeners are defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span>

<span data-ttu-id="5d43d-143">`winrm quickconfig` 為接聽程式建立下列預設設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-143">`winrm quickconfig` creates the following default settings for a listener.</span></span> <span data-ttu-id="5d43d-144">您可以建立一個以上的接聽程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-144">You can create more than one listener.</span></span> <span data-ttu-id="5d43d-145">如需詳細資訊，請 `winrm help config` 在命令提示字元中輸入。</span><span class="sxs-lookup"><span data-stu-id="5d43d-145">For more information, type `winrm help config` at a command prompt.</span></span>

### <a name="address"></a><span data-ttu-id="5d43d-146">位址</span><span class="sxs-lookup"><span data-stu-id="5d43d-146">Address</span></span>

<span data-ttu-id="5d43d-147">指定為其建立此接聽程式的位址。</span><span class="sxs-lookup"><span data-stu-id="5d43d-147">Specifies the address for which this listener was created.</span></span>

### <a name="transport"></a><span data-ttu-id="5d43d-148">傳輸</span><span class="sxs-lookup"><span data-stu-id="5d43d-148">Transport</span></span>

<span data-ttu-id="5d43d-149">指定要用來傳送和接收 WS-Management 通訊協定的要求和回應的傳輸。</span><span class="sxs-lookup"><span data-stu-id="5d43d-149">Specifies the transport to use to send and receive WS-Management protocol requests and responses.</span></span> <span data-ttu-id="5d43d-150">值必須是 *HTTP* 或 *HTTPS*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-150">The value must be either *HTTP* or *HTTPS*.</span></span> <span data-ttu-id="5d43d-151">預設值為 *HTTP*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-151">The default is *HTTP*.</span></span>

### <a name="port"></a><span data-ttu-id="5d43d-152">連接埠</span><span class="sxs-lookup"><span data-stu-id="5d43d-152">Port</span></span>

<span data-ttu-id="5d43d-153">指定為其建立此接聽程式的 TCP 連接埠。</span><span class="sxs-lookup"><span data-stu-id="5d43d-153">Specifies the TCP port for which this listener is created.</span></span>

<span data-ttu-id="5d43d-154">**WinRM 2.0：** 預設 HTTP 埠為5985。</span><span class="sxs-lookup"><span data-stu-id="5d43d-154">**WinRM 2.0:** The default HTTP port is 5985.</span></span>

### <a name="hostname"></a><span data-ttu-id="5d43d-155">Hostname (主機名稱)</span><span class="sxs-lookup"><span data-stu-id="5d43d-155">Hostname</span></span>

<span data-ttu-id="5d43d-156">指定執行 WinRM 服務之電腦的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5d43d-156">Specifies the host name of the computer on which the WinRM service is running.</span></span> <span data-ttu-id="5d43d-157">此值必須是完整功能變數名稱、IPv4 或 IPv6 常值字串，或萬用字元。</span><span class="sxs-lookup"><span data-stu-id="5d43d-157">The value must be a fully-qualified domain name, or an IPv4 or IPv6 literal string, or a wildcard character.</span></span>

### <a name="enabled"></a><span data-ttu-id="5d43d-158">已啟用</span><span class="sxs-lookup"><span data-stu-id="5d43d-158">Enabled</span></span>

<span data-ttu-id="5d43d-159">指定接聽程式已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="5d43d-159">Specifies whether the listener is enabled or disabled.</span></span> <span data-ttu-id="5d43d-160">預設值是 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-160">The default value is *True*.</span></span>

### <a name="urlprefix"></a><span data-ttu-id="5d43d-161">URLPrefix</span><span class="sxs-lookup"><span data-stu-id="5d43d-161">URLPrefix</span></span>

<span data-ttu-id="5d43d-162">指定要接受 HTTP 或 HTTPS 要求的 URL 前置詞。</span><span class="sxs-lookup"><span data-stu-id="5d43d-162">Specifies a URL prefix on which to accept HTTP or HTTPS requests.</span></span> <span data-ttu-id="5d43d-163">這是一個字串，其中只包含字元 a-z、a-z、9-0、底線 (\_) 和斜線 (/) 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-163">This is a string containing only the characters a-z, A-Z, 9-0, underscore (\_), and slash (/).</span></span> <span data-ttu-id="5d43d-164">字串不得以斜線開頭或結尾 (/) 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-164">The string must not start with or end with a slash (/).</span></span> <span data-ttu-id="5d43d-165">例如，如果電腦名稱稱是 SampleMachine，則 WinRM 用戶端會 https://SampleMachine/< 在目的地位址中指定 *URLPrefix*>。</span><span class="sxs-lookup"><span data-stu-id="5d43d-165">For example, if the computer name is SampleMachine, then the WinRM client would specify https://SampleMachine/<*URLPrefix*> in the destination address.</span></span> <span data-ttu-id="5d43d-166">預設的 URL 前置詞為 "wsman"。</span><span class="sxs-lookup"><span data-stu-id="5d43d-166">The default URL prefix is "wsman".</span></span>

### <a name="certificatethumbprint"></a><span data-ttu-id="5d43d-167">CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5d43d-167">CertificateThumbprint</span></span>

<span data-ttu-id="5d43d-168">指定服務憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="5d43d-168">Specifies the thumbprint of the service certificate.</span></span> <span data-ttu-id="5d43d-169">此值代表在憑證的 [憑證指紋] 欄位中找到的兩位數十六進位值的字串。</span><span class="sxs-lookup"><span data-stu-id="5d43d-169">This value represents a string of two-digit hexadecimal values found in the Thumbprint field of the certificate.</span></span> <span data-ttu-id="5d43d-170">此字串包含憑證的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="5d43d-170">This string contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="5d43d-171">憑證將用於用戶端憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-171">Certificates are used in client certificate-based authentication.</span></span> <span data-ttu-id="5d43d-172">憑證只能對應至本機使用者帳戶，而且無法使用網域帳戶。</span><span class="sxs-lookup"><span data-stu-id="5d43d-172">Certificates can be mapped only to local user accounts, and they do not work with domain accounts.</span></span>

### <a name="listeningon"></a><span data-ttu-id="5d43d-173">ListeningOn</span><span class="sxs-lookup"><span data-stu-id="5d43d-173">ListeningOn</span></span>

<span data-ttu-id="5d43d-174">指定接聽程式所使用的 IPv4 和 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="5d43d-174">Specifies the IPv4 and IPv6 addresses that the listener uses.</span></span> <span data-ttu-id="5d43d-175">例如： "111.0.0.1，111.222.333.444，：：1，1000：2000：2c：3： c19：9ec8： a715：5e24，3ffe：8311： ffff： f70f：0：5efe：111.222.333.444，fe80：：5efe： 111.222.333.444% 8，fe80：： c19：9ec8： a715： 5e24% 6"。</span><span class="sxs-lookup"><span data-stu-id="5d43d-175">For example: "111.0.0.1, 111.222.333.444, ::1, 1000:2000:2c:3:c19:9ec8:a715:5e24, 3ffe:8311:ffff:f70f:0:5efe:111.222.333.444, fe80::5efe:111.222.333.444%8, fe80::c19:9ec8:a715:5e24%6".</span></span>

## <a name="protocol-default-settings"></a><span data-ttu-id="5d43d-176">通訊協定預設設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-176">Protocol default settings</span></span>

<span data-ttu-id="5d43d-177">許多設定設定（例如 MaxEnvelopeSizekb 或 SoapTraceEnabled）會決定 WinRM 用戶端和伺服器元件與 WS-Management 通訊協定的互動方式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-177">Many of the configuration settings, such as MaxEnvelopeSizekb or SoapTraceEnabled, determine how the WinRM client and server components interact with the WS-Management protocol.</span></span> <span data-ttu-id="5d43d-178">下列清單描述可用的設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-178">The following list describes the available configuration settings.</span></span>

### <a name="maxenvelopesizekb"></a><span data-ttu-id="5d43d-179">MaxEnvelopeSizekb</span><span class="sxs-lookup"><span data-stu-id="5d43d-179">MaxEnvelopeSizekb</span></span>

<span data-ttu-id="5d43d-180">指定最大的簡單物件存取通訊協定 (SOAP) 資料（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d43d-180">Specifies the maximum Simple Object Access Protocol (SOAP) data in kilobytes.</span></span> <span data-ttu-id="5d43d-181">預設值為 150 kb。</span><span class="sxs-lookup"><span data-stu-id="5d43d-181">The default is 150 kilobytes.</span></span>

> [!NOTE]  
> <span data-ttu-id="5d43d-182">如果 MaxEnvelopeSizekb 設為大於1039440的值，則不支援此行為。</span><span class="sxs-lookup"><span data-stu-id="5d43d-182">The behavior is unsupported if MaxEnvelopeSizekb is set to a value greater than 1039440.</span></span>

### <a name="maxtimeoutms"></a><span data-ttu-id="5d43d-183">MaxTimeoutms</span><span class="sxs-lookup"><span data-stu-id="5d43d-183">MaxTimeoutms</span></span>

<span data-ttu-id="5d43d-184">指定可用於提取要求以外任何要求的最大超時時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d43d-184">Specifies the maximum time-out, in milliseconds, that can be used for any request other than Pull requests.</span></span> <span data-ttu-id="5d43d-185">預設值為60000。</span><span class="sxs-lookup"><span data-stu-id="5d43d-185">The default is 60000.</span></span>

### <a name="maxbatchitems"></a><span data-ttu-id="5d43d-186">MaxBatchItems</span><span class="sxs-lookup"><span data-stu-id="5d43d-186">MaxBatchItems</span></span>

<span data-ttu-id="5d43d-187">指定可在 Pull 回應中使用的元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d43d-187">Specifies the maximum number of elements that can be used in a Pull response.</span></span> <span data-ttu-id="5d43d-188">預設值為32000。</span><span class="sxs-lookup"><span data-stu-id="5d43d-188">The default is 32000.</span></span>

### <a name="maxproviderrequests"></a><span data-ttu-id="5d43d-189">MaxProviderRequests</span><span class="sxs-lookup"><span data-stu-id="5d43d-189">MaxProviderRequests</span></span>

<span data-ttu-id="5d43d-190">指定服務所允許的並行要求數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d43d-190">Specifies the maximum number of concurrent requests that are allowed by the service.</span></span> <span data-ttu-id="5d43d-191">預設值為 25。</span><span class="sxs-lookup"><span data-stu-id="5d43d-191">The default is 25.</span></span>

<span data-ttu-id="5d43d-192">**WinRM 2.0：** 這項設定已被取代，而且設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5d43d-192">**WinRM 2.0:** This setting is deprecated, and is set to read-only.</span></span>

## <a name="winrm-client-default-configuration-settings"></a><span data-ttu-id="5d43d-193">WinRM 用戶端預設設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-193">WinRM client default configuration settings</span></span>

<span data-ttu-id="5d43d-194">WinRM 的用戶端版本具有下列預設設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-194">The client version of WinRM has the following default configuration settings.</span></span>

### <a name="networkdelayms"></a><span data-ttu-id="5d43d-195">NetworkDelayms</span><span class="sxs-lookup"><span data-stu-id="5d43d-195">NetworkDelayms</span></span>

<span data-ttu-id="5d43d-196">指定用戶端電腦將等候以配合網路延遲時間的額外時間 (以毫秒為單位)。</span><span class="sxs-lookup"><span data-stu-id="5d43d-196">Specifies the extra time in milliseconds that the client computer waits to accommodate for network delay time.</span></span> <span data-ttu-id="5d43d-197">預設值為5000毫秒。</span><span class="sxs-lookup"><span data-stu-id="5d43d-197">The default is 5000 milliseconds.</span></span>

### <a name="urlprefix"></a><span data-ttu-id="5d43d-198">URLPrefix</span><span class="sxs-lookup"><span data-stu-id="5d43d-198">URLPrefix</span></span>

<span data-ttu-id="5d43d-199">指定要接受 HTTP 或 HTTPS 要求的 URL 前置詞。</span><span class="sxs-lookup"><span data-stu-id="5d43d-199">Specifies a URL prefix on which to accept HTTP or HTTPS requests.</span></span> <span data-ttu-id="5d43d-200">預設的 URL 前置詞為 "wsman"。</span><span class="sxs-lookup"><span data-stu-id="5d43d-200">The default URL prefix is "wsman".</span></span>

### <a name="allowunencrypted"></a><span data-ttu-id="5d43d-201">AllowUnencrypted</span><span class="sxs-lookup"><span data-stu-id="5d43d-201">AllowUnencrypted</span></span>

<span data-ttu-id="5d43d-202">允許用戶端電腦要求未加密的流量。</span><span class="sxs-lookup"><span data-stu-id="5d43d-202">Allows the client computer to request unencrypted traffic.</span></span> <span data-ttu-id="5d43d-203">根據預設，用戶端電腦需要加密的網路流量，且此設定為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-203">By default, the client computer requires encrypted network traffic and this setting is *False*.</span></span>

### <a name="basic"></a><span data-ttu-id="5d43d-204">基本</span><span class="sxs-lookup"><span data-stu-id="5d43d-204">Basic</span></span>

<span data-ttu-id="5d43d-205">允許用戶端電腦使用基本驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-205">Allows the client computer to use Basic authentication.</span></span> <span data-ttu-id="5d43d-206">基本驗證是使用純文字，將使用者名稱與密碼傳送至伺服器或 Proxy 的配置。</span><span class="sxs-lookup"><span data-stu-id="5d43d-206">Basic authentication is a scheme in which the user name and password are sent in clear text to the server or proxy.</span></span> <span data-ttu-id="5d43d-207">這個方法是最不安全的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="5d43d-207">This method is the least secure method of authentication.</span></span> <span data-ttu-id="5d43d-208">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-208">The default is *True*.</span></span>

### <a name="digest"></a><span data-ttu-id="5d43d-209">Digest</span><span class="sxs-lookup"><span data-stu-id="5d43d-209">Digest</span></span>

<span data-ttu-id="5d43d-210">允許用戶端使用摘要式驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-210">Allows the client to use Digest authentication.</span></span> <span data-ttu-id="5d43d-211">摘要式驗證是一種查問-回應配置，會針對該查問使用伺服器特定的資料字串。</span><span class="sxs-lookup"><span data-stu-id="5d43d-211">Digest authentication is a challenge-response scheme that uses a server-specified data string for the challenge.</span></span> <span data-ttu-id="5d43d-212">只有用戶端電腦可以起始摘要式驗證要求。</span><span class="sxs-lookup"><span data-stu-id="5d43d-212">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="5d43d-213">用戶端電腦會將要求傳送至伺服器以進行驗證，並從伺服器接收權杖字串。</span><span class="sxs-lookup"><span data-stu-id="5d43d-213">The client computer sends a request to the server to authenticate, and receives a token string from the server.</span></span> <span data-ttu-id="5d43d-214">然後，用戶端電腦會傳送資源要求，包括使用者名稱和密碼的密碼編譯雜湊與權杖字串合併。</span><span class="sxs-lookup"><span data-stu-id="5d43d-214">Then the client computer sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="5d43d-215">HTTP 和 HTTPS 都支援摘要式驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-215">Digest authentication is supported for HTTP and for HTTPS.</span></span> <span data-ttu-id="5d43d-216">WinRM Shell 用戶端腳本和應用程式可以指定摘要式驗證，但是 WinRM 服務不接受摘要式驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-216">WinRM Shell client scripts and applications can specify Digest authentication, but the WinRM service does not accept Digest authentication.</span></span> <span data-ttu-id="5d43d-217">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-217">The default is *True*.</span></span>

> [!NOTE]
> <span data-ttu-id="5d43d-218">透過 HTTP 進行的摘要式驗證會被視為不安全的。</span><span class="sxs-lookup"><span data-stu-id="5d43d-218">Digest authentication over HTTP is not considered secure.</span></span>

### <a name="certificate"></a><span data-ttu-id="5d43d-219">憑證</span><span class="sxs-lookup"><span data-stu-id="5d43d-219">Certificate</span></span>

<span data-ttu-id="5d43d-220">允許用戶端使用以用戶端憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-220">Allows the client to use client certificate-based authentication.</span></span> <span data-ttu-id="5d43d-221">以憑證為基礎的驗證是一種配置，其中伺服器會驗證 X509 憑證所識別的用戶端。</span><span class="sxs-lookup"><span data-stu-id="5d43d-221">Certificate-based authentication is a scheme in which the server authenticates a client identified by an X509 certificate.</span></span> <span data-ttu-id="5d43d-222">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-222">The default is *True*.</span></span>

### <a name="kerberos"></a><span data-ttu-id="5d43d-223">Kerberos</span><span class="sxs-lookup"><span data-stu-id="5d43d-223">Kerberos</span></span>

<span data-ttu-id="5d43d-224">允許用戶端使用 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-224">Allows the client to use Kerberos authentication.</span></span> <span data-ttu-id="5d43d-225">Kerberos 驗證是一種配置，讓用戶端與伺服器可利用 Kerberos 憑證進行互相驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-225">Kerberos authentication is a scheme in which the client and server mutually authenticate by using Kerberos certificates.</span></span> <span data-ttu-id="5d43d-226">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-226">The default is *True*.</span></span>

### <a name="negotiate"></a><span data-ttu-id="5d43d-227">交涉</span><span class="sxs-lookup"><span data-stu-id="5d43d-227">Negotiate</span></span>

<span data-ttu-id="5d43d-228">允許用戶端使用交涉驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-228">Allows the client to use Negotiate authentication.</span></span> <span data-ttu-id="5d43d-229">交涉驗證是一種配置，讓用戶端可將要求傳送到伺服器以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-229">Negotiate authentication is a scheme in which the client sends a request to the server to authenticate.</span></span> <span data-ttu-id="5d43d-230">伺服器會判斷要使用 Kerberos 通訊協定或 NTLM。</span><span class="sxs-lookup"><span data-stu-id="5d43d-230">The server determines whether to use the Kerberos protocol or NTLM.</span></span> <span data-ttu-id="5d43d-231">伺服器會選取 Kerberos 通訊協定來驗證網域帳戶，而針對本機電腦帳戶則會選取 NTLM。</span><span class="sxs-lookup"><span data-stu-id="5d43d-231">The Kerberos protocol is selected to authenticate a domain account, and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="5d43d-232">使用者名稱必須以網域使用者的網域 \\ 使用者 \_ 名稱格式來指定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-232">The user name must be specified in domain\\user\_name format for a domain user.</span></span> <span data-ttu-id="5d43d-233">您必須以 \_ \\ \_ 伺服器電腦上本機使用者的「伺服器名稱使用者名稱」格式來指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5d43d-233">The user name must be specified in "server\_name\\user\_name" format for a local user on a server computer.</span></span> <span data-ttu-id="5d43d-234">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-234">The default is *True*.</span></span>

### <a name="credssp"></a><span data-ttu-id="5d43d-235">CredSSP</span><span class="sxs-lookup"><span data-stu-id="5d43d-235">CredSSP</span></span>

<span data-ttu-id="5d43d-236">允許用戶端使用認證安全性支援提供者 (CredSSP) 驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-236">Allows the client to use Credential Security Support Provider (CredSSP) authentication.</span></span> <span data-ttu-id="5d43d-237">CredSSP 可讓應用程式將使用者的認證從用戶端電腦委派至目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="5d43d-237">CredSSP enables an application to delegate the user's credentials from the client computer to the target server.</span></span> <span data-ttu-id="5d43d-238">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-238">The default is *False*.</span></span>

### <a name="defaultports"></a><span data-ttu-id="5d43d-239">DefaultPorts</span><span class="sxs-lookup"><span data-stu-id="5d43d-239">DefaultPorts</span></span>

<span data-ttu-id="5d43d-240">指定用戶端將用於 HTTP 或 HTTPS 的埠。</span><span class="sxs-lookup"><span data-stu-id="5d43d-240">Specifies the ports that the client will use for either HTTP or HTTPS.</span></span>

<span data-ttu-id="5d43d-241">**WinRM 2.0：** 預設的 HTTP 埠是5985，而預設的 HTTPS 埠是5986。</span><span class="sxs-lookup"><span data-stu-id="5d43d-241">**WinRM 2.0:** The default HTTP port is 5985, and the default HTTPS port is 5986.</span></span>

### <a name="trustedhosts"></a><span data-ttu-id="5d43d-242">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="5d43d-242">TrustedHosts</span></span>

<span data-ttu-id="5d43d-243">指定信任的遠端電腦清單。</span><span class="sxs-lookup"><span data-stu-id="5d43d-243">Specifies the list of remote computers that are trusted.</span></span> <span data-ttu-id="5d43d-244">工作組中的其他電腦或不同網域中的電腦應新增到此清單。</span><span class="sxs-lookup"><span data-stu-id="5d43d-244">Other computers in a workgroup or computers in a different domain should be added to this list.</span></span>

> [!Note]
> <span data-ttu-id="5d43d-245">TrustedHosts 清單中的電腦未經過驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-245">The computers in the TrustedHosts list are not authenticated.</span></span> <span data-ttu-id="5d43d-246">用戶端可能會將認證資訊傳送至這些電腦。</span><span class="sxs-lookup"><span data-stu-id="5d43d-246">The client may send credential information to these computers.</span></span>

<span data-ttu-id="5d43d-247">如果為 TrustedHost 指定了 IPv6 位址，則位址必須以方括弧括住，如下列 winrm 公用程式命令所示： `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-247">If an IPv6 address is specified for a TrustedHost, the address must be enclosed in square brackets as demonstrated by the following winrm utility command: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'`.</span></span>

<span data-ttu-id="5d43d-248">如需有關如何將電腦新增到 TrustedHosts 清單的詳細資訊，請輸入 `winrm help config` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-248">For more info about how to add computers to the TrustedHosts list, type `winrm help config`.</span></span>

## <a name="winrm-service-default-configuration-settings"></a><span data-ttu-id="5d43d-249">WinRM 服務預設設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-249">WinRM service default configuration settings</span></span>

<span data-ttu-id="5d43d-250">WinRM 的服務版本具有下列預設設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-250">The service version of WinRM has the following default configuration settings.</span></span>

### <a name="rootsddl"></a><span data-ttu-id="5d43d-251">RootSDDL</span><span class="sxs-lookup"><span data-stu-id="5d43d-251">RootSDDL</span></span>

<span data-ttu-id="5d43d-252">指定控制接聽程式遠端存取的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="5d43d-252">Specifies the security descriptor that controls remote access to the listener.</span></span> <span data-ttu-id="5d43d-253">預設值為 "O:NSG：糟糕： P (A;;GA;;;BA)  (A;;GR;;;ER) S:P (AU; FA;GA;;;WD)  (AU; SA;GWGX;;;WD) 」。</span><span class="sxs-lookup"><span data-stu-id="5d43d-253">The default is "O:NSG:BAD:P(A;;GA;;;BA)(A;;GR;;;ER)S:P(AU;FA;GA;;;WD)(AU;SA;GWGX;;;WD)".</span></span>

### <a name="maxconcurrentoperations"></a><span data-ttu-id="5d43d-254">MaxConcurrentOperations</span><span class="sxs-lookup"><span data-stu-id="5d43d-254">MaxConcurrentOperations</span></span>

<span data-ttu-id="5d43d-255">並行作業的最大數目。</span><span class="sxs-lookup"><span data-stu-id="5d43d-255">The maximum number of concurrent operations.</span></span> <span data-ttu-id="5d43d-256">預設值為 100。</span><span class="sxs-lookup"><span data-stu-id="5d43d-256">The default is 100.</span></span>

<span data-ttu-id="5d43d-257">**WinRM 2.0：** MaxConcurrentOperations 設定已被取代，而且設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5d43d-257">**WinRM 2.0:** The MaxConcurrentOperations setting is deprecated, and is set to read-only.</span></span> <span data-ttu-id="5d43d-258">這項設定已由 MaxConcurrentOperationsPerUser 取代。</span><span class="sxs-lookup"><span data-stu-id="5d43d-258">This setting has been replaced by MaxConcurrentOperationsPerUser.</span></span>

### <a name="maxconcurrentoperationsperuser"></a><span data-ttu-id="5d43d-259">MaxConcurrentOperationsPerUser</span><span class="sxs-lookup"><span data-stu-id="5d43d-259">MaxConcurrentOperationsPerUser</span></span>

<span data-ttu-id="5d43d-260">指定任何使用者可在相同系統上遠端開啟的並行作業數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d43d-260">Specifies the maximum number of concurrent operations that any user can remotely open on the same system.</span></span> <span data-ttu-id="5d43d-261">預設值是 1500。</span><span class="sxs-lookup"><span data-stu-id="5d43d-261">The default is 1500.</span></span>

### <a name="enumerationtimeoutms"></a><span data-ttu-id="5d43d-262">EnumerationTimeoutms</span><span class="sxs-lookup"><span data-stu-id="5d43d-262">EnumerationTimeoutms</span></span>

<span data-ttu-id="5d43d-263">指定提取訊息之間的空閒超時時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d43d-263">Specifies the idle time-out in milliseconds between Pull messages.</span></span> <span data-ttu-id="5d43d-264">預設值為60000。</span><span class="sxs-lookup"><span data-stu-id="5d43d-264">The default is 60000.</span></span>

### <a name="maxconnections"></a><span data-ttu-id="5d43d-265">MaxConnections</span><span class="sxs-lookup"><span data-stu-id="5d43d-265">MaxConnections</span></span>

<span data-ttu-id="5d43d-266">指定服務可以同時處理的使用中要求數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d43d-266">Specifies the maximum number of active requests that the service can process simultaneously.</span></span> <span data-ttu-id="5d43d-267">預設值為300。</span><span class="sxs-lookup"><span data-stu-id="5d43d-267">The default is 300.</span></span>

<span data-ttu-id="5d43d-268">**WinRM 2.0：** 預設值為25。</span><span class="sxs-lookup"><span data-stu-id="5d43d-268">**WinRM 2.0:** The default is 25.</span></span>

### <a name="maxpacketretrievaltimeseconds"></a><span data-ttu-id="5d43d-269">MaxPacketRetrievalTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="5d43d-269">MaxPacketRetrievalTimeSeconds</span></span>

<span data-ttu-id="5d43d-270">指定 WinRM 服務取出封包所需的最大時間長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d43d-270">Specifies the maximum length of time, in seconds, the WinRM service takes to retrieve a packet.</span></span> <span data-ttu-id="5d43d-271">預設值是 120 秒。</span><span class="sxs-lookup"><span data-stu-id="5d43d-271">The default is 120 seconds.</span></span>

### <a name="allowunencrypted"></a><span data-ttu-id="5d43d-272">AllowUnencrypted</span><span class="sxs-lookup"><span data-stu-id="5d43d-272">AllowUnencrypted</span></span>

<span data-ttu-id="5d43d-273">允許用戶端電腦要求未加密的流量。</span><span class="sxs-lookup"><span data-stu-id="5d43d-273">Allows the client computer to request unencrypted traffic.</span></span> <span data-ttu-id="5d43d-274">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-274">The default is *False*.</span></span>

### <a name="basic"></a><span data-ttu-id="5d43d-275">基本</span><span class="sxs-lookup"><span data-stu-id="5d43d-275">Basic</span></span>

<span data-ttu-id="5d43d-276">允許 WinRM 服務使用基本驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-276">Allows the WinRM service to use Basic authentication.</span></span> <span data-ttu-id="5d43d-277">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-277">The default is *False*.</span></span>

### <a name="certificate"></a><span data-ttu-id="5d43d-278">憑證</span><span class="sxs-lookup"><span data-stu-id="5d43d-278">Certificate</span></span>

<span data-ttu-id="5d43d-279">允許 WinRM 服務使用以用戶端憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-279">Allows the WinRM service to use client certificate-based authentication.</span></span> <span data-ttu-id="5d43d-280">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-280">The default is *False*.</span></span>

### <a name="kerberos"></a><span data-ttu-id="5d43d-281">Kerberos</span><span class="sxs-lookup"><span data-stu-id="5d43d-281">Kerberos</span></span>

<span data-ttu-id="5d43d-282">允許 WinRM 服務使用 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-282">Allows the WinRM service to use Kerberos authentication.</span></span> <span data-ttu-id="5d43d-283">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-283">The default is *True*.</span></span>

### <a name="negotiate"></a><span data-ttu-id="5d43d-284">交涉</span><span class="sxs-lookup"><span data-stu-id="5d43d-284">Negotiate</span></span>

<span data-ttu-id="5d43d-285">允許 WinRM 服務使用「協商驗證」。</span><span class="sxs-lookup"><span data-stu-id="5d43d-285">Allows the WinRM service to use Negotiate authentication.</span></span> <span data-ttu-id="5d43d-286">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-286">The default is *True*.</span></span>

### <a name="credssp"></a><span data-ttu-id="5d43d-287">CredSSP</span><span class="sxs-lookup"><span data-stu-id="5d43d-287">CredSSP</span></span>

<span data-ttu-id="5d43d-288">允許 WinRM 服務使用認證安全性支援提供者 (CredSSP) 驗證。</span><span class="sxs-lookup"><span data-stu-id="5d43d-288">Allows the WinRM service to use Credential Security Support Provider (CredSSP) authentication.</span></span> <span data-ttu-id="5d43d-289">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-289">The default is *False*.</span></span>

### <a name="cbthardeninglevel"></a><span data-ttu-id="5d43d-290">CbtHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="5d43d-290">CbtHardeningLevel</span></span>

<span data-ttu-id="5d43d-291">設定驗證要求之通道繫結權杖需求的原則。</span><span class="sxs-lookup"><span data-stu-id="5d43d-291">Sets the policy for channel-binding token requirements in authentication requests.</span></span> <span data-ttu-id="5d43d-292">預設值為 *寬鬆*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-292">The default is *Relaxed*.</span></span>

### <a name="defaultports"></a><span data-ttu-id="5d43d-293">DefaultPorts</span><span class="sxs-lookup"><span data-stu-id="5d43d-293">DefaultPorts</span></span>

<span data-ttu-id="5d43d-294">指定 WinRM 服務將針對 HTTP 或 HTTPS 使用的埠。</span><span class="sxs-lookup"><span data-stu-id="5d43d-294">Specifies the ports that the WinRM service will use for either HTTP or HTTPS.</span></span>

<span data-ttu-id="5d43d-295">**WinRM 2.0：** 預設的 HTTP 埠是5985，而預設的 HTTPS 埠是5986。</span><span class="sxs-lookup"><span data-stu-id="5d43d-295">**WinRM 2.0:** The default HTTP port is 5985, and the default HTTPS port is 5986.</span></span>

### <a name="ipv4filter-and-ipv6filter"></a><span data-ttu-id="5d43d-296">IPv4Filter 和 IPv6Filter</span><span class="sxs-lookup"><span data-stu-id="5d43d-296">IPv4Filter and IPv6Filter</span></span>

<span data-ttu-id="5d43d-297">指定接聽程式可以使用的 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="5d43d-297">Specifies the IPv4 or IPv6 addresses that listeners can use.</span></span> <span data-ttu-id="5d43d-298">預設值為 IPv4Filter = \* 和 IPv6Filter = \* 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-298">The defaults are IPv4Filter = \* and IPv6Filter = \*.</span></span>

<span data-ttu-id="5d43d-299">**IPv4：** IPv4 常值字串是由四個小數點的十進位數所組成，每個數位的範圍介於0到255之間。</span><span class="sxs-lookup"><span data-stu-id="5d43d-299">**IPv4:** An IPv4 literal string consists of four dotted decimal numbers, each in the range 0 through 255.</span></span> <span data-ttu-id="5d43d-300">例如：192.168.0.0。</span><span class="sxs-lookup"><span data-stu-id="5d43d-300">For example: 192.168.0.0.</span></span>

<span data-ttu-id="5d43d-301">**IPv6：** IPv6 常值字串會以括弧括住，且包含以冒號分隔的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="5d43d-301">**IPv6:** An IPv6 literal string is enclosed in brackets and contains hexadecimal numbers that are separated by colons.</span></span> <span data-ttu-id="5d43d-302">例如： \[ ：： 1 \] 或 \[ 3ffe： FFFF：：6ECB： 0101 \] 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-302">For example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

### <a name="enablecompatibilityhttplistener"></a><span data-ttu-id="5d43d-303">EnableCompatibilityHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d43d-303">EnableCompatibilityHttpListener</span></span>

<span data-ttu-id="5d43d-304">指定是否啟用相容性 HTTP 接聽程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-304">Specifies whether the compatibility HTTP listener is enabled.</span></span> <span data-ttu-id="5d43d-305">如果此設定為 *True*，則接聽程式除了埠5985之外，還會接聽埠80。</span><span class="sxs-lookup"><span data-stu-id="5d43d-305">If this setting is *True*, then the listener will listen on port 80 in addition to port 5985.</span></span> <span data-ttu-id="5d43d-306">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-306">The default is *False*.</span></span>

### <a name="enablecompatibilityhttpslistener"></a><span data-ttu-id="5d43d-307">EnableCompatibilityHttpsListener</span><span class="sxs-lookup"><span data-stu-id="5d43d-307">EnableCompatibilityHttpsListener</span></span>

<span data-ttu-id="5d43d-308">指定是否啟用相容性 HTTPS 接聽程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-308">Specifies whether the compatibility HTTPS listener is enabled.</span></span> <span data-ttu-id="5d43d-309">如果此設定為 *True*，則接聽程式除了埠5986之外，還會接聽埠443。</span><span class="sxs-lookup"><span data-stu-id="5d43d-309">If this setting is *True*, then the listener will listen on port 443 in addition to port 5986.</span></span> <span data-ttu-id="5d43d-310">預設值為 *False*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-310">The default is *False*.</span></span>

## <a name="winrs-default-configuration-settings"></a><span data-ttu-id="5d43d-311">Winrs 預設設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-311">Winrs Default Configuration Settings</span></span>

<span data-ttu-id="5d43d-312">`winrm quickconfig` 也會設定 **Winrs** 預設設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-312">`winrm quickconfig` also configures **Winrs** default settings.</span></span>

### <a name="allowremoteshellaccess"></a><span data-ttu-id="5d43d-313">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="5d43d-313">AllowRemoteShellAccess</span></span>

<span data-ttu-id="5d43d-314">啟用遠端殼層的存取。</span><span class="sxs-lookup"><span data-stu-id="5d43d-314">Enables access to remote shells.</span></span> <span data-ttu-id="5d43d-315">如果您將此參數設定為 *False*，則伺服器將會拒絕新的遠端 shell 連接。</span><span class="sxs-lookup"><span data-stu-id="5d43d-315">If you set this parameter to *False*, then new remote shell connections will be rejected by the server.</span></span> <span data-ttu-id="5d43d-316">預設值為 *True*。</span><span class="sxs-lookup"><span data-stu-id="5d43d-316">The default is *True*.</span></span>

### <a name="idletimeout"></a><span data-ttu-id="5d43d-317">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="5d43d-317">IdleTimeout</span></span>

<span data-ttu-id="5d43d-318">指定當遠端殼層中沒有使用者活動時遠端殼層維持開啟的最長時間 (以毫秒為單位)。</span><span class="sxs-lookup"><span data-stu-id="5d43d-318">Specifies the maximum time, in milliseconds, that the remote shell will remain open when there is no user activity in the remote shell.</span></span> <span data-ttu-id="5d43d-319">經過指定的時間之後，系統會自動刪除遠端殼層。</span><span class="sxs-lookup"><span data-stu-id="5d43d-319">The remote shell is automatically deleted after the time that is specified.</span></span>

<span data-ttu-id="5d43d-320">**WinRM 2.0：** 預設值為180000。</span><span class="sxs-lookup"><span data-stu-id="5d43d-320">**WinRM 2.0:** The default is 180000.</span></span> <span data-ttu-id="5d43d-321">最小值是60000。</span><span class="sxs-lookup"><span data-stu-id="5d43d-321">The minimum value is 60000.</span></span> <span data-ttu-id="5d43d-322">將這個值設定為低於60000，將不會影響超時時間。</span><span class="sxs-lookup"><span data-stu-id="5d43d-322">Setting this value lower than 60000 will have no effect on the time-out.</span></span>

### <a name="maxconcurrentusers"></a><span data-ttu-id="5d43d-323">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="5d43d-323">MaxConcurrentUsers</span></span>

<span data-ttu-id="5d43d-324">指定可透過遠端殼層，在相同電腦上同時執行遠端操作的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d43d-324">Specifies the maximum number of users who can concurrently perform remote operations on the same computer through a remote shell.</span></span> <span data-ttu-id="5d43d-325">如果新的遠端 shell 連接超過指定的限制，將會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="5d43d-325">New remote shell connections will be rejected if they exceed the specified limit.</span></span> <span data-ttu-id="5d43d-326">預設值為 5。</span><span class="sxs-lookup"><span data-stu-id="5d43d-326">The default is 5.</span></span>

### <a name="maxshellruntime"></a><span data-ttu-id="5d43d-327">MaxShellRunTime</span><span class="sxs-lookup"><span data-stu-id="5d43d-327">MaxShellRunTime</span></span>

<span data-ttu-id="5d43d-328">指定允許遠端命令或腳本執行的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5d43d-328">Specifies the maximum time, in milliseconds, that the remote command or script is allowed to execute.</span></span> <span data-ttu-id="5d43d-329">預設值為28800000。</span><span class="sxs-lookup"><span data-stu-id="5d43d-329">The default is 28800000.</span></span>

<span data-ttu-id="5d43d-330">**WinRM 2.0：** MaxShellRunTime 設定會設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5d43d-330">**WinRM 2.0:** The MaxShellRunTime setting is set to read-only.</span></span> <span data-ttu-id="5d43d-331">變更 MaxShellRunTime 的值將不會影響遠端 shell。</span><span class="sxs-lookup"><span data-stu-id="5d43d-331">Changing the value for MaxShellRunTime will have no effect on the remote shells.</span></span>

### <a name="maxprocessespershell"></a><span data-ttu-id="5d43d-332">MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="5d43d-332">MaxProcessesPerShell</span></span>

<span data-ttu-id="5d43d-333">指定允許任何殼層操作啟動的處理程序數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d43d-333">Specifies the maximum number of processes that any shell operation is allowed to start.</span></span> <span data-ttu-id="5d43d-334">值為 0 可允許無限數目的處理程序。</span><span class="sxs-lookup"><span data-stu-id="5d43d-334">A value of 0 allows for an unlimited number of processes.</span></span> <span data-ttu-id="5d43d-335">預設值是 15。</span><span class="sxs-lookup"><span data-stu-id="5d43d-335">The default is 15.</span></span>

### <a name="maxmemorypershellmb"></a><span data-ttu-id="5d43d-336">MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="5d43d-336">MaxMemoryPerShellMB</span></span>

<span data-ttu-id="5d43d-337">指定每個 shell 配置的最大記憶體量，包括 shell 的子進程。</span><span class="sxs-lookup"><span data-stu-id="5d43d-337">Specifies the maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="5d43d-338">預設值為 150 MB。</span><span class="sxs-lookup"><span data-stu-id="5d43d-338">The default is 150 MB.</span></span>

### <a name="maxshellsperuser"></a><span data-ttu-id="5d43d-339">MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="5d43d-339">MaxShellsPerUser</span></span>

<span data-ttu-id="5d43d-340">指定任何使用者可以在同一部電腦上遠端開啟的最大並行 Shell 數目。</span><span class="sxs-lookup"><span data-stu-id="5d43d-340">Specifies the maximum number of concurrent shells that any user can remotely open on the same computer.</span></span> <span data-ttu-id="5d43d-341">如果啟用此原則設定，則當計數超過指定的限制時，使用者將無法開啟新的遠端 shell。</span><span class="sxs-lookup"><span data-stu-id="5d43d-341">If this policy setting is enabled, then the user won't be able to open new remote shells if the count exceeds the specified limit.</span></span> <span data-ttu-id="5d43d-342">如果此原則設定已停用或未設定，每個使用者的遠端 Shell 限制將預設為 5 個。</span><span class="sxs-lookup"><span data-stu-id="5d43d-342">If this policy setting is disabled or is not configured, the limit will be set to 5 remote shells per user by default.</span></span>

## <a name="configuring-winrm-with-group-policy"></a><span data-ttu-id="5d43d-343">使用群組原則設定 WinRM</span><span class="sxs-lookup"><span data-stu-id="5d43d-343">Configuring WinRM with Group Policy</span></span>

<span data-ttu-id="5d43d-344">使用群組原則編輯器，為您企業中的電腦設定 Windows 遠端 Shell 和 WinRM。</span><span class="sxs-lookup"><span data-stu-id="5d43d-344">Use the Group Policy editor to configure Windows Remote Shell and WinRM for computers in your enterprise.</span></span>

### <a name="to-configure-with-group-policy"></a><span data-ttu-id="5d43d-345">若要使用群組原則設定</span><span class="sxs-lookup"><span data-stu-id="5d43d-345">To configure with Group Policy</span></span>

1. <span data-ttu-id="5d43d-346">以系統管理員身分開啟 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="5d43d-346">Open a Command Prompt window as an administrator.</span></span>
2. <span data-ttu-id="5d43d-347">在命令提示字元中，輸入 `gpedit.msc` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-347">At the Command Prompt, type `gpedit.msc`.</span></span> <span data-ttu-id="5d43d-348">**群組原則物件編輯器**] 視窗隨即開啟。</span><span class="sxs-lookup"><span data-stu-id="5d43d-348">The **Group Policy Object Editor** window opens.</span></span>
3. <span data-ttu-id="5d43d-349">在 [電腦設定] **\\ 系統管理範本 [ \\ windows 元件**] 下的 [電腦設定] 底下，尋找 **Windows 遠端管理** 和 **WINDOWS 遠端 Shell** 群組原則物件 () GPO</span><span class="sxs-lookup"><span data-stu-id="5d43d-349">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4. <span data-ttu-id="5d43d-350">在 [ **擴充** ] 索引標籤上，選取設定以查看描述。</span><span class="sxs-lookup"><span data-stu-id="5d43d-350">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="5d43d-351">按兩下設定以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="5d43d-351">Double click a setting to edit it.</span></span>

## <a name="windows-firewall-and-winrm-20-ports"></a><span data-ttu-id="5d43d-352">Windows 防火牆和 WinRM 2.0 埠</span><span class="sxs-lookup"><span data-stu-id="5d43d-352">Windows Firewall and WinRM 2.0 ports</span></span>

<span data-ttu-id="5d43d-353">從 WinRM 2.0 開始，所設定的預設接聽程式埠為 `Winrm quickconfig` HTTP 傳輸的埠5985，以及 HTTPS 的埠5986。</span><span class="sxs-lookup"><span data-stu-id="5d43d-353">Starting in WinRM 2.0, the default listener ports configured by `Winrm quickconfig` are port 5985 for HTTP transport, and port 5986 for HTTPS.</span></span> <span data-ttu-id="5d43d-354">WinRM 接聽程式可以在任何任意埠上進行設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-354">WinRM listeners can be configured on any arbitrary port.</span></span>

<span data-ttu-id="5d43d-355">如果電腦已升級至 WinRM 2.0，則會遷移先前設定的接聽程式，並仍會接收流量。</span><span class="sxs-lookup"><span data-stu-id="5d43d-355">If a computer is upgraded to WinRM 2.0, the previously configured listeners are migrated, and still receive traffic.</span></span>

## <a name="winrm-installation-and-configuration-notes"></a><span data-ttu-id="5d43d-356">WinRM 安裝和設定注意事項</span><span class="sxs-lookup"><span data-stu-id="5d43d-356">WinRM installation and configuration notes</span></span>

<span data-ttu-id="5d43d-357">WinRM 不相依于 WinHttp 以外的任何其他服務。</span><span class="sxs-lookup"><span data-stu-id="5d43d-357">WinRM isn't dependent on any other service except WinHttp.</span></span> <span data-ttu-id="5d43d-358">如果 IIS 系統管理員服務安裝在同一部電腦上，您可能會看到指出 WinRM 無法在 Internet Information Services (IIS) 之前載入的訊息。</span><span class="sxs-lookup"><span data-stu-id="5d43d-358">If the IIS Admin Service is installed on the same computer, then you might see messages that indicate that WinRM can't be loaded before Internet Information Services (IIS).</span></span> <span data-ttu-id="5d43d-359">不過，WinRM 實際上不依賴 IIS &mdash; 這些訊息，因為載入順序可確保 iis 服務會在 HTTP 服務之前啟動。</span><span class="sxs-lookup"><span data-stu-id="5d43d-359">However, WinRM doesn't actually depend on IIS&mdash;those messages occur because the load order ensures that the IIS service starts before the HTTP service.</span></span> <span data-ttu-id="5d43d-360">WinRM 確實需要 `WinHTTP.dll` 註冊。</span><span class="sxs-lookup"><span data-stu-id="5d43d-360">WinRM does require that `WinHTTP.dll` be registered.</span></span>

<span data-ttu-id="5d43d-361">如果電腦上已安裝 ISA2004 防火牆用戶端，它可能會導致 Web 服務 (WS-MANAGEMENT) 用戶端停止回應。</span><span class="sxs-lookup"><span data-stu-id="5d43d-361">If the ISA2004 firewall client is installed on the computer, then it can cause a Web Services for Management (WS-Management) client to stop responding.</span></span> <span data-ttu-id="5d43d-362">若要避免此問題，請安裝 ISA2004 Firewall SP1。</span><span class="sxs-lookup"><span data-stu-id="5d43d-362">To avoid this issue, install ISA2004 Firewall SP1.</span></span>

<span data-ttu-id="5d43d-363">如果有兩個具有不同 IP 位址的接聽程式服務設定為使用相同的埠號碼和電腦名稱稱，則 WinRM 只會接聽或接收單一位址的訊息。</span><span class="sxs-lookup"><span data-stu-id="5d43d-363">If two listener services with different IP addresses are configured with the same port number and computer name, then WinRM listens or receives messages on only one address.</span></span> <span data-ttu-id="5d43d-364">這是因為 WS-Management 通訊協定所使用的 URL 前置詞是相同的。</span><span class="sxs-lookup"><span data-stu-id="5d43d-364">This is because the URL prefixes used by the WS-Management protocol are the same.</span></span>

## <a name="ipmi-driver-and-provider-installation-notes"></a><span data-ttu-id="5d43d-365">IPMI 驅動程式和提供者安裝注意事項</span><span class="sxs-lookup"><span data-stu-id="5d43d-365">IPMI driver and provider installation notes</span></span>

<span data-ttu-id="5d43d-366">驅動程式可能無法偵測到非 Microsoft 的 IPMI 驅動程式是否存在。</span><span class="sxs-lookup"><span data-stu-id="5d43d-366">The driver might not detect the existence of IPMI drivers that are not from Microsoft.</span></span> <span data-ttu-id="5d43d-367">如果驅動程式無法啟動，您可能需要停用它。</span><span class="sxs-lookup"><span data-stu-id="5d43d-367">If the driver fails to start, then you might need to disable it.</span></span>

<span data-ttu-id="5d43d-368">如果基礎板 [管理控制器 (BMC) ](./windows-remote-management-glossary.md#b) 資源出現在系統 BIOS 中，則 ACPI (隨插即用) 會偵測 BMC 硬體，並自動安裝 IPMI 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-368">If the [baseboard management controller (BMC)](./windows-remote-management-glossary.md#b) resources appear in the system BIOS, then ACPI (Plug and Play) detects the BMC hardware, and automatically installs the IPMI driver.</span></span> <span data-ttu-id="5d43d-369">隨插即用支援可能不會出現在所有 Bmc 中。</span><span class="sxs-lookup"><span data-stu-id="5d43d-369">Plug and Play support might not be present in all BMCs.</span></span> <span data-ttu-id="5d43d-370">如果隨插即用偵測到 BMC，則在安裝硬體管理元件之前，裝置管理員中會出現不明的裝置。</span><span class="sxs-lookup"><span data-stu-id="5d43d-370">If the BMC is detected by Plug and Play, then an Unknown Device appears in Device Manager before the Hardware Management component is installed.</span></span> <span data-ttu-id="5d43d-371">安裝驅動程式時，裝置管理員中會出現新的元件，即 Microsoft ACPI 一般 IPMI 相容裝置。</span><span class="sxs-lookup"><span data-stu-id="5d43d-371">When the driver is installed, a new component, the Microsoft ACPI Generic IPMI Compliant Device, appears in Device Manager.</span></span>

<span data-ttu-id="5d43d-372">如果您的系統未自動偵測 BMC 並安裝驅動程式，但在安裝過程中偵測到 BMC，則您必須建立 BMC 裝置。</span><span class="sxs-lookup"><span data-stu-id="5d43d-372">If your system doesn't automatically detect the BMC and install the driver, but a BMC was detected during the setup process, then you must create the BMC device.</span></span> <span data-ttu-id="5d43d-373">若要這樣做，請在命令提示字元中輸入下列命令： `Rundll32 ipmisetp.dll, AddTheDevice` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-373">To do this, type the following command at a command prompt: `Rundll32 ipmisetp.dll, AddTheDevice`.</span></span> <span data-ttu-id="5d43d-374">執行此命令之後，會建立 IPMI 裝置，並在裝置管理員中顯示。</span><span class="sxs-lookup"><span data-stu-id="5d43d-374">After this command is executed, the IPMI device is created, and it appears in Device Manager.</span></span> <span data-ttu-id="5d43d-375">如果您卸載硬體管理元件，則會移除裝置。</span><span class="sxs-lookup"><span data-stu-id="5d43d-375">If you uninstall the Hardware Management component, then the device is removed.</span></span>

<span data-ttu-id="5d43d-376">如需詳細資訊，請參閱 [硬體管理簡介](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="5d43d-376">For more information, see [Hardware Management Introduction](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).</span></span>

<span data-ttu-id="5d43d-377">IPMI 提供者會將硬體類別放在 WMI 的 **根 \\ 硬體**[命名空間](/windows/desktop/WmiSdk/gloss-n)中。</span><span class="sxs-lookup"><span data-stu-id="5d43d-377">The IPMI provider places the hardware classes in the **root\\hardware** [namespace](/windows/desktop/WmiSdk/gloss-n) of WMI.</span></span> <span data-ttu-id="5d43d-378">如需硬體類別的詳細資訊，請參閱 [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。</span><span class="sxs-lookup"><span data-stu-id="5d43d-378">For more information about the hardware classes, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="5d43d-379">如需 WMI *命名空間* 的詳細資訊，請參閱 [wmi 架構](/windows/desktop/WmiSdk/wmi-architecture)。</span><span class="sxs-lookup"><span data-stu-id="5d43d-379">For more information about WMI *namespaces*, see [WMI Architecture](/windows/desktop/WmiSdk/wmi-architecture).</span></span>

## <a name="wmi-plug-in-configuration-notes"></a><span data-ttu-id="5d43d-380">WMI 外掛程式設定注意事項</span><span class="sxs-lookup"><span data-stu-id="5d43d-380">WMI plug-in configuration notes</span></span>

<span data-ttu-id="5d43d-381">從 Windows 8 和 Windows Server 2012 開始， [WMI 外掛程式](./windows-remote-management-glossary.md#w) 有自己的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="5d43d-381">Beginning with Windows 8 and Windows Server 2012, [WMI plug-ins](./windows-remote-management-glossary.md#w) have their own security configurations.</span></span> <span data-ttu-id="5d43d-382">若為一般或電源 (非系統管理員) 使用者要能夠使用 *WMI 外掛程式*，您 [必須在設定](./windows-remote-management-glossary.md#l) 接聽程式之後，啟用該使用者的存取權。</span><span class="sxs-lookup"><span data-stu-id="5d43d-382">For a normal or power (non-administrator) user to be able to use the *WMI plug-in*, you need to enable access for that user after the [listener](./windows-remote-management-glossary.md#l) has been configured.</span></span> <span data-ttu-id="5d43d-383">首先，您必須透過下列其中一個步驟，設定使用者以遠端存取 [WMI](./windows-remote-management-glossary.md#w) 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-383">First, you must set up the user for remote access to [WMI](./windows-remote-management-glossary.md#w) through one of these steps.</span></span>

- <span data-ttu-id="5d43d-384">執行 `lusrmgr.msc` 以將使用者新增至 [**本機使用者和群組**] 視窗中的 [ **WinRMRemoteWMIUsers \_ \_** ] 群組，或</span><span class="sxs-lookup"><span data-stu-id="5d43d-384">Run `lusrmgr.msc` to add the user to the **WinRMRemoteWMIUsers\_\_** group in the **Local Users and Groups** window, or</span></span>
- <span data-ttu-id="5d43d-385">使用 **winrm** 命令列工具來設定 [WMI 外掛程式](./windows-remote-management-glossary.md#w)[*命名空間*](./windows-remote-management-glossary.md#n)的安全描述項，如下所示： `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` 。</span><span class="sxs-lookup"><span data-stu-id="5d43d-385">use the **winrm** command-line tool to configure the security descriptor for the [*namespace*](./windows-remote-management-glossary.md#n) of the [WMI plug-in](./windows-remote-management-glossary.md#w), as follows: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace`.</span></span>

<span data-ttu-id="5d43d-386">當使用者介面出現時，請新增使用者。</span><span class="sxs-lookup"><span data-stu-id="5d43d-386">When the user interface appears, add the user.</span></span>

<span data-ttu-id="5d43d-387">設定使用者進行 [wmi](./windows-remote-management-glossary.md#w)的遠端存取之後，您必須設定 *wmi* ，讓使用者能夠存取該外掛程式。</span><span class="sxs-lookup"><span data-stu-id="5d43d-387">After setting up the user for remote access to [WMI](./windows-remote-management-glossary.md#w), you must set up *WMI* to allow the user to access the plug-in.</span></span> <span data-ttu-id="5d43d-388">若要這樣做，請執行 `wmimgmt.msc` 以修改要在 [ **wmi 控制**] 視窗中存取之 [命名空間](./windows-remote-management-glossary.md#n)的 *wmi* 安全性。</span><span class="sxs-lookup"><span data-stu-id="5d43d-388">To do this, run `wmimgmt.msc` to modify the *WMI* security for the [namespace](./windows-remote-management-glossary.md#n) to be accessed in the **WMI Control** window.</span></span>

<span data-ttu-id="5d43d-389">大部分的管理 WMI 類別都是在 **根 \\ cimv2** 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="5d43d-389">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span>