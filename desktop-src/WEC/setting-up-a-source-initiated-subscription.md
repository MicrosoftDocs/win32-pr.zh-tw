---
title: 設定來源起始的訂用帳戶
description: 來源起始的訂用帳戶可讓您在事件收集器電腦上定義訂用帳戶，而不需定義事件來源電腦，然後可以設定多個遠端事件來源電腦 (使用群組原則設定) 將事件轉寄至事件收集器電腦。
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/04/2020
ms.locfileid: "104374916"
---
# <a name="setting-up-a-source-initiated-subscription"></a>設定來源起始的訂用帳戶

來源起始的訂用帳戶可讓您在事件收集器電腦上定義訂用帳戶，而不需定義事件來源電腦，然後可以設定多個遠端事件來源電腦 (使用群組原則設定) 將事件轉寄至事件收集器電腦。 這與收集器起始的訂用帳戶不同，因為在收集器起始的訂閱模型中，事件收集器必須定義事件訂用帳戶中的所有事件來源。

設定來源起始的訂用帳戶時，請考慮事件來源電腦是否位於與事件收集器電腦相同的網域中。 下列各節說明當事件來源位於相同網域，或與事件收集器電腦不同的網域中時，所要遵循的步驟。

> [!Note]  
> 網域（本機或遠端）中的任何電腦都可以是事件收集器。 不過，在選擇事件收集器時，請務必選取拓撲接近大部分事件產生位置的機器。 將事件傳送至 WAN 上網路位置的電腦，可降低事件收集的整體效能和效率。

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>設定來源起始的訂用帳戶，其中事件來源位於與事件收集器電腦相同的網域中

事件來源電腦與事件收集器電腦都必須設定為設定來源起始的訂用帳戶。

> [!Note]  
> 這些指示假設您擁有 Windows Server 網域控制站的系統管理員存取權，而該網域服務將設定遠端電腦或電腦來收集事件。

### <a name="configuring-the-event-source-computer"></a>設定事件來源電腦

1. 從 Windows Server 網域控制站上提高許可權的命令提示字元中執行下列命令，以設定 Windows 遠端管理：

    **winrm qc-q**

2. 執行下列命令來啟動群組原則：

    **% SYSTEMROOT% \\ System32 \\ gpedit.msc**

3. 在 [ **電腦** 設定] 節點底下，展開 [ **系統管理範本** ] 節點，然後展開 [ **Windows 元件** ] 節點，然後選取 [ **事件轉送** ] 節點。

4. 以滑鼠右鍵按一下 [ **SubscriptionManager** ] 設定，然後選取 [ **屬性**]。 啟用 [ **SubscriptionManager** ] 設定，然後按一下 [ **顯示** ] 按鈕，將伺服器位址新增至設定。 至少新增一個指定事件收集器電腦的設定。 [ **SubscriptionManager 屬性** ] 視窗包含說明設定語法的 [ **說明** ] 索引標籤。

5. 新增 **SubscriptionManager** 設定之後，請執行下列命令以確保套用原則：

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>設定事件收集器電腦

1. 從 Windows Server 網域控制站上提高許可權的命令提示字元中執行下列命令，以設定 Windows 遠端管理：

    **winrm qc-q**

2. 執行下列命令來設定事件收集器服務：

    **>wecutil qc/q**

3. 建立來源起始的訂用帳戶。 這可以透過程式設計方式來完成，方法是使用事件檢視器，或使用 [**Wecutil.exe**](wecutil.md)。 如需如何以程式設計方式建立訂閱的詳細資訊，請參閱 [建立來源起始訂用](creating-a-source-initiated-subscription.md)帳戶中的程式碼範例。 如果您使用 Wecutil.exe，則必須建立事件訂閱 XML 檔案，並使用下列命令：

    **>wecutil cs** *configurationFile.xml*

    下列 XML 是訂用帳戶設定檔的內容範例，此檔案會建立來源起始的訂用帳戶，以便將遠端電腦的應用程式事件記錄檔中的事件轉送至事件收集器電腦上的 ForwardedEvents 記錄檔。

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > 建立來源起始的訂閱時，如果 AllowedSourceDomainComputers、AllowedSourceNonDomainComputers/IssuerCAList、AllowedSubjectList 和 DeniedSubjectList 都是空的，則 "O:NSG： NSD： (A;;GA;;;DC)  (A;;GA;;;NS) 」將用作 AllowedSourceDomainComputers 的預設安全描述項。 預設描述項會授與網域電腦網域群組的成員，以及本機轉寄站) 的局域網路服務群組 (，這是為此訂用帳戶引發事件的能力。

### <a name="to-validate-that-the-subscription-works-correctly"></a>驗證訂用帳戶是否正確運作

1. 在事件收集器電腦上，完成下列步驟：

    1. 請在 Windows Server 網域控制站上，從提高許可權的命令提示字元執行下列命令，以取得訂用帳戶的執行時間狀態：

        **>wecutil gr** *&lt; subscriptionID &gt;*

    2. 確認事件來源已連接。 在您建立要連接之事件來源的訂用帳戶之後，您可能需要等候直到原則中指定的重新整理間隔結束為止。
    3. 執行下列命令以取得訂用帳戶資訊：

        **>wecutil gs** *&lt; subscriptionID &gt;*

    4. 從訂用帳戶資訊中取得 DeliveryMaxItems 值。

2. 在事件來源電腦上，從事件訂用帳戶引發符合查詢的事件。 必須針對要轉送的事件引發事件的 DeliveryMaxItems 數目。
3. 在事件收集器電腦上，驗證事件已轉送至 ForwardedEvents 記錄檔或訂用帳戶中指定的記錄檔。

## <a name="forwarding-the-security-log"></a>轉送安全性記錄檔

若要能夠轉寄安全性記錄檔，您需要將 NETWORK SERVICE 帳戶新增到 EventLog Readers 群組。

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>設定來源起始的訂用帳戶，其中事件來源不在與事件收集器電腦相同的網域中

> [!Note]  
> 這些指示假設您擁有 Windows Server 網域控制站的系統管理員存取權。 在此情況下，由於遠端事件收集器電腦或電腦 (s) 不在網域控制站所提供的網域中，因此必須使用 Services (services.msc) 將 Windows 遠端管理設定為 [自動]，以啟動個別用戶端。 或者，您可以在每個遠端用戶端上執行 "winrm quickconfig"。

必須符合下列必要條件，才能建立訂用帳戶。

1. 在事件收集器電腦上，從提升許可權的命令提示字元執行下列命令，以設定 Windows 遠端管理和事件收集器服務：

    **winrm qc-q**

    **>wecutil qc/q**

2. 收集器電腦應該在本機電腦憑證存放區中有伺服器驗證憑證 (憑證與伺服器驗證目的) 。
3. 在事件來源電腦上，執行下列命令以設定 Windows 遠端管理：

    **winrm qc-q**

4. 來源電腦的用戶端驗證憑證 (憑證，在本機電腦憑證存放區中) 用戶端驗證目的。
5. 在事件收集器電腦上開啟埠5986。 若要開啟此埠，請執行下列命令：

    **netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**

### <a name="certificates-requirements"></a>憑證需求

- 伺服器驗證憑證必須安裝在本機電腦的個人存放區中的事件收集器電腦上。 此憑證的主體必須符合收集器的 FQDN。
- 用戶端驗證憑證必須安裝在本機電腦的個人存放區中的事件來源電腦上。 此憑證的主體必須符合電腦的 FQDN。
- 如果用戶端憑證是由不同的憑證授權單位單位所簽發，而不是其中一個事件收集器，則這些根和中繼憑證也必須安裝在事件收集器上。
- 如果用戶端憑證是由中繼憑證授權單位單位所發出，而收集器正在執行 Windows 2012 或更新版本，您就必須設定下列登錄機碼：

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- 確認伺服器和用戶端都能夠成功檢查所有憑證的撤銷狀態。 使用 **certutil** 命令可協助針對任何錯誤進行疑難排解。

請在本文中尋找詳細資訊： https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>在事件收集器上設定接聽程式

1. 使用下列命令來設定憑證驗證：

    **winrm set winrm/config/service/auth @ {Certificate = "true"}**

2. 具有伺服器驗證憑證的 WinRM HTTPS 接聽程式應該存在於事件收集器電腦上。 您可以使用下列命令來驗證：

    **winrm e winrm/config/接聽程式**

3. 如果您看不到 HTTPS 接聽程式，或如果 HTTPS 接聽程式的捲動方塊列印與收集器電腦上的伺服器驗證憑證的 thumb 列印不同，您可以刪除該接聽程式，並使用正確的 thumb 列印來建立新的接聽程式。 若要刪除 HTTPs 接聽程式，請使用下列命令：

    **winrm 刪除 winrm/config/接聽程式？位址 = * + 傳輸 = HTTPS**

    若要建立新的接聽程式，請使用下列命令：

    **winrm 建立 winrm/config/接聽程式？Address =&#42;+ Transport = HTTPS @ {Hostname = "** &lt; _收集器的 FQDN_ &gt; **";CertificateThumbprint = "** &lt; _伺服器驗證憑證的 Thumb 列印_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>設定事件收集器的憑證對應

1. 建立新的本機使用者，並將它新增至本機系統管理員群組。
2. 使用存在於電腦「信任的根憑證授權單位」或「中繼憑證授權單位單位」的憑證來建立憑證對應。

    這是發出安裝在事件來源電腦上之憑證的根或中繼 CA 的憑證 *(為了避免混淆，這是憑證鏈中憑證正下方的 ca)*：

    **winrm create winrm/config/service/certmapping？** = &lt; _發行 CA 憑證_ 的簽發者指紋 &gt; **+ Subject =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **";Password = "** &lt; _password_ &gt; **"}-remote： localhost**

3. 從用戶端，使用下列命令來測試接聽程式和憑證對應：

    **winrm g winrm/config-r:HTTPs：//** &lt;_事件收集器 FQDN_ &gt;**： 5986-a:certificate-certificate： "** &lt;_用戶端驗證憑證_ &gt; 的指紋 **"**

    這應該會傳回事件收集器的 WinRM 設定。 如果未顯示設定，**請勿** 移過此步驟。

    **此步驟會發生什麼事？**
    - 用戶端會連線到事件收集器，並傳送指定的憑證
    - 事件收集器會尋找發行 CA，並檢查是否為相符的憑證對應
    - 事件收集器會驗證用戶端憑證鏈和撤銷狀態
    - 如果上述步驟成功，就會完成驗證。

> [!NOTE]
> 您可能會收到「拒絕存取」錯誤抱怨驗證方法，這可能會造成誤導。 若要進行疑難排解，請檢查事件收集器上的 CAPI 記錄檔。

4. 使用下列命令來列出已設定的 certmapping 專案： **winrm enum winrm/config/service/certmapping**

### <a name="event-source-computer-configuration"></a>事件來源電腦設定

1. 使用系統管理員帳戶登入，並開啟本機群組原則編輯器 (gpedit.msc) 
2. 流覽至本機電腦原則設定 [管理 \ 系統管理範本] Components\Event 轉送。
3. 開啟 [設定目標訂用帳戶管理員的伺服器位址、重新整理間隔和簽發者憑證授權單位單位] 原則。
4. 啟用原則，然後按一下 [顯示 ...] SubscriptionManagers按鈕。
5. 在 [SubscriptionManagers] 視窗中，輸入下列字串：

    **伺服器 = HTTPS：//** &lt;_事件收集器伺服器_ &gt; 的 FQDN **： 5986/wsman/SubscriptionManager/WEC，Refresh =** &lt;重新整理 _間隔（秒）_ &gt;**、IssuerCA =** &lt;_發行 CA 憑證的指紋_&gt;

6. 執行下列命令列，以重新整理本機群組原則設定： Gpupdate/force
7. 這些步驟應該會在來源電腦事件檢視器應用程式和服務 Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational 記錄檔中產生事件104，並顯示下列訊息：

    「轉寄站已成功連接到位於位址 FQDN 的訂用帳戶管理員， &lt; &gt; 後面接著事件100，並顯示下列訊息：「 &lt; 已成功建立訂用帳戶 sub_name &gt; 。」

8. 在事件收集器上，訂用帳戶執行時間狀態現在會顯示1個作用中的電腦。
9. 開啟事件收集器上的 ForwardedEvents 記錄，並檢查您是否有從來源電腦轉送的事件。

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>在事件來源上授與用戶端憑證私密金鑰的許可權

1. 在事件來源電腦上，開啟本機電腦的 [憑證管理] 主控台。
2. 以滑鼠右鍵按一下用戶端憑證，然後管理私密金鑰。
3. 授與讀取權限給網路服務使用者。

### <a name="event-subscription-configuration"></a>事件訂用帳戶設定

1. 在事件收集器中開啟事件檢視器，然後流覽至 [訂閱] 節點。
2. 以滑鼠右鍵按一下 [訂閱]，然後選擇 [建立訂用帳戶 ...]
3. 提供新訂用帳戶的名稱和選擇性描述。
4. 選取 [來源電腦起始] 選項，然後按一下 [選取電腦群組 ...]。
5. 在 [電腦群組] 中，按一下 [新增非網域電腦 ...] 並輸入事件來源主機名稱。
6. 按一下 [新增憑證 ...] 並新增發出用戶端憑證之憑證授權單位單位的憑證。 您可以按一下 [查看憑證] 來驗證憑證。
7. 在 [憑證授權單位單位] 中，按一下 [確定] 以新增憑證。
8. 新增電腦完成後，請按一下 [確定]。
9. 返回訂用帳戶屬性，按一下 [選取事件]。
10. 藉由指定事件層級 (s) 、事件記錄 (s) 或事件來源 () 、事件識別碼 () 和任何其他篩選選項來設定事件查詢篩選器。
11. 返回訂用帳戶屬性，按一下 [Advanced] .。。
12. 選擇其中一個優化選項，以將事件從來源事件傳遞至事件收集器，或保留預設為正常： 
    1. **最小化頻寬**：傳遞的事件將會降低儲存頻寬的頻率。
    2. 將 **延遲降至最低**：系統會儘快傳遞事件以減少事件延遲。
13. 將通訊協定變更為 HTTPS，然後按一下 [確定]。
14. 按一下 [確定] 以建立新的訂用帳戶。
15. 以滑鼠右鍵按一下並選擇 [執行時間狀態]，以檢查訂用帳戶的執行時間狀態
