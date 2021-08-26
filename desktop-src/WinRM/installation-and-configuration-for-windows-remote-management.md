---
title: Windows 遠端管理的安裝和設定
description: 針對要執行 Windows 遠端管理 (winrm) 腳本，以及針對 **winrm** 命令列工具執行資料操作，Windows 遠端管理 (winrm) 必須同時安裝及設定。
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: c031ad9b9d9c888385527c227b102c64bb4dfb65eaea340e52eac3fb9595e591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997618"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Windows 遠端管理的安裝和設定

針對要執行 Windows 遠端管理 (winrm) 腳本，以及針對 **winrm** 命令列工具執行資料操作，Windows 遠端管理 (winrm) 必須同時安裝及設定。

這些元素也取決於 WinRM 設定。

- [Windows 遠端 Shell](./windows-remote-management-glossary.md#w)命令列工具 (**Winrs**) 。
- [事件轉送](./windows-remote-management-glossary.md#e)。
- Windows PowerShell 2.0 遠端處理。

## <a name="where-winrm-is-installed"></a>安裝 WinRM 的位置

WinRM 會自動與所有目前支援的 Windows 作業系統版本一起安裝。

## <a name="configuration-of-winrm-and-ipmi"></a>Configuration WinRM 與 IPMI

這些 WinRM 和 [智慧型平臺管理介面 (IPMI) ](./windows-remote-management-glossary.md#i) [WMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) 元件與作業系統一起安裝。

- WinRM 服務會自動在 Windows Server 2008 和 Windows Vista 上的 wards (上啟動，您必須) 手動啟動服務。
- 依預設， [不會設定](./windows-remote-management-glossary.md#l) 任何 WinRM 接聽程式。 即使 WinRM 服務正在執行，也無法接收或傳送要求資料 WS-Management 的通訊協定 [訊息](./windows-remote-management-glossary.md#m) 。
- 網際網路連線防火牆 (ICF) 封鎖對埠的存取。

請在命令提示字元中輸入下列命令，以使用 **Winrm** 命令來尋找接聽程式和位址。

```console
winrm e winrm/config/listener
```

若要檢查設定的狀態，請輸入下列命令。

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>快速預設設定

您可以在本機電腦上啟用 WS-Management 的通訊協定，並使用命令設定遠端系統管理的預設設定 `winrm quickconfig` 。

`winrm quickconfig`命令 (或縮寫版本 `winrm qc`) 執行這些作業。

- 啟動 WinRM 服務，並將服務啟動類型設定為自動啟動。
- 針對在任何 IP 位址上使用 HTTP 或 HTTPS 傳送和接收 WS-Management 通訊協定 [訊息](./windows-remote-management-glossary.md#m) 的埠設定接聽程式。
- 定義 WinRM 服務的 ICF 例外狀況，並開啟 HTTP 和 HTTPS 的埠。

> [!NOTE]
> 此 `winrm quickconfig` 命令只會針對目前的使用者設定檔建立防火牆例外。 如果防火牆設定檔因任何原因而變更，您應該執行 `winrm quickconfig` 以啟用新設定檔的防火牆例外，否則可能不會啟用例外狀況。

若要取得自訂設定的相關資訊，請 `winrm help config` 在命令提示字元中輸入。

### <a name="to-configure-winrm-with-default-settings"></a>使用預設設定來設定 WinRM

1. `winrm quickconfig`在命令提示字元中輸入。

   如果您不是在本機電腦系統管理員帳戶下執行，則必須從 [**開始**] 功能表選取 [**以系統管理員身分執行**]，或在命令提示字元中使用 **Runas** 命令。

2. 當工具顯示 [ **讓這些變更成為 \[ y/ \] n**] 時，請輸入 **y**。

   如果設定成功，則會顯示下列輸出。

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. 保留 WinRM 用戶端和伺服器元件的預設設定，或進行自訂。 例如，您可能需要將特定遠端電腦新增至用戶端設定 TrustedHosts 清單。

   當無法建立相互驗證時，您應該設定信任的主機清單。 Kerberos 允許相互驗證，但不能在工作組 &mdash; 私人網路域中使用。 為工作組設定受信任的主機時，最佳作法是讓清單盡可能受限制。

4. 輸入命令以建立 HTTPS 接聽程式 `winrm quickconfig -transport:https` 。 請注意，您必須開啟埠5986，HTTPS 傳輸才能運作。

## <a name="listener-and-ws-management-protocol-default-settings"></a>接聽程式和 WS-Management 通訊協定預設設定

若要取得接聽程式設定，請 `winrm enumerate winrm/config/listener` 在命令提示字元中輸入。 接聽程式是由傳輸 (HTTP 或 HTTPS) 和 IPv4 或 IPv6 位址所定義。

`winrm quickconfig` 為接聽程式建立下列預設設定。 您可以建立一個以上的接聽程式。 如需詳細資訊，請 `winrm help config` 在命令提示字元中輸入。

### <a name="address"></a>位址

指定為其建立此接聽程式的位址。

### <a name="transport"></a>傳輸

指定要用來傳送和接收 WS-Management 通訊協定的要求和回應的傳輸。 值必須是 *HTTP* 或 *HTTPS*。 預設值為 *HTTP*。

### <a name="port"></a>連接埠

指定為其建立此接聽程式的 TCP 連接埠。

**WinRM 2.0：** 預設 HTTP 埠為5985。

### <a name="hostname"></a>Hostname (主機名稱)

指定執行 WinRM 服務之電腦的主機名稱。 此值必須是完整功能變數名稱、IPv4 或 IPv6 常值字串，或萬用字元。

### <a name="enabled"></a>啟用

指定接聽程式已啟用或停用。 預設值是 *True*。

### <a name="urlprefix"></a>URLPrefix

指定要接受 HTTP 或 HTTPS 要求的 URL 前置詞。 這是一個字串，其中只包含字元 a-z、a-z、9-0、底線 (\_) 和斜線 (/) 。 字串不得以斜線開頭或結尾 (/) 。 例如，如果電腦名稱稱是 SampleMachine，則 WinRM 用戶端會 https://SampleMachine/< 在目的地位址中指定 *URLPrefix*>。 預設的 URL 前置詞為 "wsman"。

### <a name="certificatethumbprint"></a>CertificateThumbprint

指定服務憑證的指紋。 此值代表在憑證的 [憑證指紋] 欄位中找到的兩位數十六進位值的字串。 此字串包含憑證的 SHA-1 雜湊。 憑證將用於用戶端憑證式驗證。 憑證只能對應至本機使用者帳戶，而且無法使用網域帳戶。

### <a name="listeningon"></a>ListeningOn

指定接聽程式所使用的 IPv4 和 IPv6 位址。 例如： "111.0.0.1，111.222.333.444，：：1，1000：2000：2c：3： c19：9ec8： a715：5e24，3ffe：8311： ffff： f70f：0：5efe：111.222.333.444，fe80：：5efe： 111.222.333.444% 8，fe80：： c19：9ec8： a715： 5e24% 6"。

## <a name="protocol-default-settings"></a>通訊協定預設設定

許多設定設定（例如 MaxEnvelopeSizekb 或 SoapTraceEnabled）會決定 WinRM 用戶端和伺服器元件與 WS-Management 通訊協定的互動方式。 下列清單描述可用的設定。

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

指定最大的簡單物件存取通訊協定 (SOAP) 資料（以 kb 為單位）。 預設值為 150 kb。

> [!NOTE]  
> 如果 MaxEnvelopeSizekb 設為大於1039440的值，則不支援此行為。

### <a name="maxtimeoutms"></a>MaxTimeoutms

指定可用於提取要求以外任何要求的最大超時時間（以毫秒為單位）。 預設值為60000。

### <a name="maxbatchitems"></a>MaxBatchItems

指定可在 Pull 回應中使用的元素數目上限。 預設值為32000。

### <a name="maxproviderrequests"></a>MaxProviderRequests

指定服務所允許的並行要求數目上限。 預設值為 25。

**WinRM 2.0：** 這項設定已被取代，而且設定為唯讀。

## <a name="winrm-client-default-configuration-settings"></a>WinRM 用戶端預設設定

WinRM 的用戶端版本具有下列預設設定。

### <a name="networkdelayms"></a>NetworkDelayms

指定用戶端電腦將等候以配合網路延遲時間的額外時間 (以毫秒為單位)。 預設值為5000毫秒。

### <a name="urlprefix"></a>URLPrefix

指定要接受 HTTP 或 HTTPS 要求的 URL 前置詞。 預設的 URL 前置詞為 "wsman"。

### <a name="allowunencrypted"></a>AllowUnencrypted

允許用戶端電腦要求未加密的流量。 根據預設，用戶端電腦需要加密的網路流量，且此設定為 *False*。

### <a name="basic"></a>Basic

允許用戶端電腦使用基本驗證。 基本驗證是使用純文字，將使用者名稱與密碼傳送至伺服器或 Proxy 的配置。 這個方法是最不安全的驗證方法。 預設值為 *True*。

### <a name="digest"></a>Digest

允許用戶端使用摘要式驗證。 摘要式驗證是一種查問-回應配置，會針對該查問使用伺服器特定的資料字串。 只有用戶端電腦可以起始摘要式驗證要求。 用戶端電腦會將要求傳送至伺服器以進行驗證，並從伺服器接收權杖字串。 然後，用戶端電腦會傳送資源要求，包括使用者名稱和密碼的密碼編譯雜湊與權杖字串合併。 HTTP 和 HTTPS 都支援摘要式驗證。 WinRM Shell 用戶端腳本和應用程式可以指定摘要式驗證，但是 WinRM 服務不接受摘要式驗證。 預設值為 *True*。

> [!NOTE]
> 透過 HTTP 進行的摘要式驗證會被視為不安全的。

### <a name="certificate"></a>憑證

允許用戶端使用以用戶端憑證為基礎的驗證。 以憑證為基礎的驗證是一種配置，其中伺服器會驗證 X509 憑證所識別的用戶端。 預設值為 *True*。

### <a name="kerberos"></a>Kerberos

允許用戶端使用 Kerberos 驗證。 Kerberos 驗證是一種配置，讓用戶端與伺服器可利用 Kerberos 憑證進行互相驗證。 預設值為 *True*。

### <a name="negotiate"></a>交涉

允許用戶端使用交涉驗證。 交涉驗證是一種配置，讓用戶端可將要求傳送到伺服器以進行驗證。 伺服器會判斷要使用 Kerberos 通訊協定或 NTLM。 伺服器會選取 Kerberos 通訊協定來驗證網域帳戶，而針對本機電腦帳戶則會選取 NTLM。 使用者名稱必須以網域使用者的網域 \\ 使用者 \_ 名稱格式來指定。 您必須以 \_ \\ \_ 伺服器電腦上本機使用者的「伺服器名稱使用者名稱」格式來指定使用者名稱。 預設值為 *True*。

### <a name="credssp"></a>CredSSP

允許用戶端使用認證安全性支援提供者 (CredSSP) 驗證。 CredSSP 可讓應用程式將使用者的認證從用戶端電腦委派至目標伺服器。 預設值為 *False*。

### <a name="defaultports"></a>DefaultPorts

指定用戶端將用於 HTTP 或 HTTPS 的埠。

**WinRM 2.0：** 預設的 HTTP 埠是5985，而預設的 HTTPS 埠是5986。

### <a name="trustedhosts"></a>TrustedHosts

指定信任的遠端電腦清單。 工作組中的其他電腦或不同網域中的電腦應新增到此清單。

> [!Note]
> TrustedHosts 清單中的電腦未經過驗證。 用戶端可能會將認證資訊傳送至這些電腦。

如果為 TrustedHost 指定了 IPv6 位址，則位址必須以方括弧括住，如下列 winrm 公用程式命令所示： `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` 。

如需有關如何將電腦新增到 TrustedHosts 清單的詳細資訊，請輸入 `winrm help config` 。

## <a name="winrm-service-default-configuration-settings"></a>WinRM 服務預設設定

WinRM 的服務版本具有下列預設設定。

### <a name="rootsddl"></a>RootSDDL

指定控制接聽程式遠端存取的安全描述項。 預設值為 "O:NSG：糟糕： P (A;;GA;;;BA)  (A;;GR;;;ER) S:P (AU; FA;GA;;;WD)  (AU; SA;GWGX;;;WD) 」。

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

並行作業的最大數目。 預設值為 100。

**WinRM 2.0：** MaxConcurrentOperations 設定已被取代，而且設定為唯讀。 這項設定已由 MaxConcurrentOperationsPerUser 取代。

### <a name="maxconcurrentoperationsperuser"></a>MaxConcurrentOperationsPerUser

指定任何使用者可在相同系統上遠端開啟的並行作業數目上限。 預設值是 1500。

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

指定提取訊息之間的空閒超時時間（以毫秒為單位）。 預設值為60000。

### <a name="maxconnections"></a>MaxConnections

指定服務可以同時處理的使用中要求數目上限。 預設值為300。

**WinRM 2.0：** 預設值為25。

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

指定 WinRM 服務取出封包所需的最大時間長度（以秒為單位）。 預設值是 120 秒。

### <a name="allowunencrypted"></a>AllowUnencrypted

允許用戶端電腦要求未加密的流量。 預設值為 *False*。

### <a name="basic"></a>Basic

允許 WinRM 服務使用基本驗證。 預設值為 *False*。

### <a name="certificate"></a>憑證

允許 WinRM 服務使用以用戶端憑證為基礎的驗證。 預設值為 *False*。

### <a name="kerberos"></a>Kerberos

允許 WinRM 服務使用 Kerberos 驗證。 預設值為 *True*。

### <a name="negotiate"></a>交涉

允許 WinRM 服務使用「協商驗證」。 預設值為 *True*。

### <a name="credssp"></a>CredSSP

允許 WinRM 服務使用認證安全性支援提供者 (CredSSP) 驗證。 預設值為 *False*。

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

設定驗證要求之通道繫結權杖需求的原則。 預設值為 *寬鬆*。

### <a name="defaultports"></a>DefaultPorts

指定 WinRM 服務將針對 HTTP 或 HTTPS 使用的埠。

**WinRM 2.0：** 預設的 HTTP 埠是5985，而預設的 HTTPS 埠是5986。

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter 和 IPv6Filter

指定接聽程式可以使用的 IPv4 或 IPv6 位址。 預設值為 IPv4Filter = \* 和 IPv6Filter = \* 。

**IPv4：** IPv4 常值字串是由四個小數點的十進位數所組成，每個數位的範圍介於0到255之間。 例如：192.168.0.0。

**IPv6：** IPv6 常值字串會以括弧括住，且包含以冒號分隔的十六進位數位。 例如： \[ ：： 1 \] 或 \[ 3ffe： FFFF：：6ECB： 0101 \] 。

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

指定是否啟用相容性 HTTP 接聽程式。 如果此設定為 *True*，則接聽程式除了埠5985之外，還會接聽埠80。 預設值為 *False*。

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

指定是否啟用相容性 HTTPS 接聽程式。 如果此設定為 *True*，則接聽程式除了埠5986之外，還會接聽埠443。 預設值為 *False*。

## <a name="winrs-default-configuration-settings"></a>Winrs 預設設定設定

`winrm quickconfig` 也會設定 **Winrs** 預設設定。

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

啟用遠端殼層的存取。 如果您將此參數設定為 *False*，則伺服器將會拒絕新的遠端 shell 連接。 預設值為 *True*。

### <a name="idletimeout"></a>IdleTimeout

指定當遠端殼層中沒有使用者活動時遠端殼層維持開啟的最長時間 (以毫秒為單位)。 經過指定的時間之後，系統會自動刪除遠端殼層。

**WinRM 2.0：** 預設值為180000。 最小值是60000。 將這個值設定為低於60000，將不會影響超時時間。

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

指定可透過遠端殼層，在相同電腦上同時執行遠端操作的使用者數目上限。 如果新的遠端 shell 連接超過指定的限制，將會遭到拒絕。 預設值為 5。

### <a name="maxshellruntime"></a>MaxShellRunTime

指定允許遠端命令或腳本執行的最長時間（以毫秒為單位）。 預設值為28800000。

**WinRM 2.0：** MaxShellRunTime 設定會設定為唯讀。 變更 MaxShellRunTime 的值將不會影響遠端 shell。

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

指定允許任何殼層操作啟動的處理程序數目上限。 值為 0 可允許無限數目的處理程序。 預設值是 15。

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

指定每個 shell 配置的最大記憶體量，包括 shell 的子進程。 預設值為 150 MB。

### <a name="maxshellsperuser"></a>MaxShellsPerUser

指定任何使用者可以在同一部電腦上遠端開啟的最大並行 Shell 數目。 如果啟用此原則設定，則當計數超過指定的限制時，使用者將無法開啟新的遠端 shell。 如果此原則設定已停用或未設定，每個使用者的遠端 Shell 限制將預設為 5 個。

## <a name="configuring-winrm-with-group-policy"></a>使用群組原則設定 WinRM

使用群組原則編輯器，為您企業中的電腦設定 Windows 的遠端 Shell 和 WinRM。

### <a name="to-configure-with-group-policy"></a>若要使用群組原則設定

1. 以系統管理員身分開啟 [命令提示字元] 視窗。
2. 在命令提示字元中，輸入 `gpedit.msc`。 **群組原則物件編輯器**] 視窗隨即開啟。
3. 在 [電腦設定] **\\) \\ 系統管理範本元件** 下，尋找 **Windows 遠端管理**，並 **Windows 遠端 Shell** 群組原則物件 (GPO Windows。
4. 在 [ **擴充** ] 索引標籤上，選取設定以查看描述。 按兩下設定以進行編輯。

## <a name="windows-firewall-and-winrm-20-ports"></a>Windows防火牆和 WinRM 2.0 埠

從 WinRM 2.0 開始，所設定的預設接聽程式埠為 `Winrm quickconfig` HTTP 傳輸的埠5985，以及 HTTPS 的埠5986。 WinRM 接聽程式可以在任何任意埠上進行設定。

如果電腦已升級至 WinRM 2.0，則會遷移先前設定的接聽程式，並仍會接收流量。

## <a name="winrm-installation-and-configuration-notes"></a>WinRM 安裝和設定注意事項

WinRM 不相依于 WinHttp 以外的任何其他服務。 如果 iis 系統管理員服務安裝在同一部電腦上，您可能會看到指出 WinRM 無法在 Internet Information Services (IIS) 之前載入的訊息。 不過，WinRM 實際上不依賴 IIS &mdash; 這些訊息，因為載入順序可確保 iis 服務會在 HTTP 服務之前啟動。 WinRM 確實需要 `WinHTTP.dll` 註冊。

如果電腦上已安裝 ISA2004 防火牆用戶端，它可能會導致 Web 服務 (WS-MANAGEMENT) 用戶端停止回應。 若要避免此問題，請安裝 ISA2004 Firewall SP1。

如果有兩個具有不同 IP 位址的接聽程式服務設定為使用相同的埠號碼和電腦名稱稱，則 WinRM 只會接聽或接收單一位址的訊息。 這是因為 WS-Management 通訊協定所使用的 URL 前置詞是相同的。

## <a name="ipmi-driver-and-provider-installation-notes"></a>IPMI 驅動程式和提供者安裝注意事項

驅動程式可能無法偵測到非 Microsoft 的 IPMI 驅動程式是否存在。 如果驅動程式無法啟動，您可能需要停用它。

如果基礎板 [管理控制器 (BMC) ](./windows-remote-management-glossary.md#b) 資源出現在系統 BIOS 中，則 ACPI (隨插即用) 會偵測 BMC 硬體，並自動安裝 IPMI 驅動程式。 隨插即用支援可能不會出現在所有 Bmc 中。 如果隨插即用偵測到 BMC，則在安裝硬體管理元件之前，裝置管理員中會出現不明的裝置。 安裝驅動程式時，裝置管理員中會出現新的元件，即 Microsoft ACPI 一般 IPMI 相容裝置。

如果您的系統未自動偵測 BMC 並安裝驅動程式，但在安裝過程中偵測到 BMC，則您必須建立 BMC 裝置。 若要這樣做，請在命令提示字元中輸入下列命令： `Rundll32 ipmisetp.dll, AddTheDevice` 。 執行此命令之後，會建立 IPMI 裝置，並在裝置管理員中顯示。 如果您卸載硬體管理元件，則會移除裝置。

如需詳細資訊，請參閱 [硬體管理簡介](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))。

IPMI 提供者會將硬體類別放在 WMI 的 **根 \\ 硬體**[命名空間](/windows/desktop/WmiSdk/gloss-n)中。 如需硬體類別的詳細資訊，請參閱 [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。 如需 WMI *命名空間* 的詳細資訊，請參閱 [wmi 架構](/windows/desktop/WmiSdk/wmi-architecture)。

## <a name="wmi-plug-in-configuration-notes"></a>WMI 外掛程式設定注意事項

從 Windows 8 和 Windows Server 2012 開始， [WMI 外掛程式](./windows-remote-management-glossary.md#w)有自己的安全性設定。 若為一般或電源 (非系統管理員) 使用者要能夠使用 *WMI 外掛程式*，您 [必須在設定](./windows-remote-management-glossary.md#l) 接聽程式之後，啟用該使用者的存取權。 首先，您必須透過下列其中一個步驟，設定使用者以遠端存取 [WMI](./windows-remote-management-glossary.md#w) 。

- 執行 `lusrmgr.msc` 以將使用者新增至 [**本機使用者和群組**] 視窗中的 [ **WinRMRemoteWMIUsers \_ \_** ] 群組，或
- 使用 **winrm** 命令列工具來設定 [WMI 外掛程式](./windows-remote-management-glossary.md#w)[*命名空間*](./windows-remote-management-glossary.md#n)的安全描述項，如下所示： `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` 。

當使用者介面出現時，請新增使用者。

設定使用者進行 [wmi](./windows-remote-management-glossary.md#w)的遠端存取之後，您必須設定 *wmi* ，讓使用者能夠存取該外掛程式。 若要這樣做，請執行 `wmimgmt.msc` 以修改要在 [ **wmi 控制**] 視窗中存取之 [命名空間](./windows-remote-management-glossary.md#n)的 *wmi* 安全性。

大部分的管理 WMI 類別都是在 **根 \\ cimv2** 命名空間中。