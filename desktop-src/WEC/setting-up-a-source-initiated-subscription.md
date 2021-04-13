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
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="5ef02-103">設定來源起始的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="5ef02-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="5ef02-104">來源起始的訂用帳戶可讓您在事件收集器電腦上定義訂用帳戶，而不需定義事件來源電腦，然後可以設定多個遠端事件來源電腦 (使用群組原則設定) 將事件轉寄至事件收集器電腦。</span><span class="sxs-lookup"><span data-stu-id="5ef02-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="5ef02-105">這與收集器起始的訂用帳戶不同，因為在收集器起始的訂閱模型中，事件收集器必須定義事件訂用帳戶中的所有事件來源。</span><span class="sxs-lookup"><span data-stu-id="5ef02-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="5ef02-106">設定來源起始的訂用帳戶時，請考慮事件來源電腦是否位於與事件收集器電腦相同的網域中。</span><span class="sxs-lookup"><span data-stu-id="5ef02-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="5ef02-107">下列各節說明當事件來源位於相同網域，或與事件收集器電腦不同的網域中時，所要遵循的步驟。</span><span class="sxs-lookup"><span data-stu-id="5ef02-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="5ef02-108">網域（本機或遠端）中的任何電腦都可以是事件收集器。</span><span class="sxs-lookup"><span data-stu-id="5ef02-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="5ef02-109">不過，在選擇事件收集器時，請務必選取拓撲接近大部分事件產生位置的機器。</span><span class="sxs-lookup"><span data-stu-id="5ef02-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="5ef02-110">將事件傳送至 WAN 上網路位置的電腦，可降低事件收集的整體效能和效率。</span><span class="sxs-lookup"><span data-stu-id="5ef02-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="5ef02-111">設定來源起始的訂用帳戶，其中事件來源位於與事件收集器電腦相同的網域中</span><span class="sxs-lookup"><span data-stu-id="5ef02-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="5ef02-112">事件來源電腦與事件收集器電腦都必須設定為設定來源起始的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ef02-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="5ef02-113">這些指示假設您擁有 Windows Server 網域控制站的系統管理員存取權，而該網域服務將設定遠端電腦或電腦來收集事件。</span><span class="sxs-lookup"><span data-stu-id="5ef02-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="5ef02-114">設定事件來源電腦</span><span class="sxs-lookup"><span data-stu-id="5ef02-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="5ef02-115">從 Windows Server 網域控制站上提高許可權的命令提示字元中執行下列命令，以設定 Windows 遠端管理：</span><span class="sxs-lookup"><span data-stu-id="5ef02-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="5ef02-116">**winrm qc-q**</span><span class="sxs-lookup"><span data-stu-id="5ef02-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="5ef02-117">執行下列命令來啟動群組原則：</span><span class="sxs-lookup"><span data-stu-id="5ef02-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="5ef02-118">**% SYSTEMROOT% \\ System32 \\ gpedit.msc**</span><span class="sxs-lookup"><span data-stu-id="5ef02-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="5ef02-119">在 [ **電腦** 設定] 節點底下，展開 [ **系統管理範本** ] 節點，然後展開 [ **Windows 元件** ] 節點，然後選取 [ **事件轉送** ] 節點。</span><span class="sxs-lookup"><span data-stu-id="5ef02-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="5ef02-120">以滑鼠右鍵按一下 [ **SubscriptionManager** ] 設定，然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="5ef02-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="5ef02-121">啟用 [ **SubscriptionManager** ] 設定，然後按一下 [ **顯示** ] 按鈕，將伺服器位址新增至設定。</span><span class="sxs-lookup"><span data-stu-id="5ef02-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="5ef02-122">至少新增一個指定事件收集器電腦的設定。</span><span class="sxs-lookup"><span data-stu-id="5ef02-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="5ef02-123">[ **SubscriptionManager 屬性** ] 視窗包含說明設定語法的 [ **說明** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5ef02-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="5ef02-124">新增 **SubscriptionManager** 設定之後，請執行下列命令以確保套用原則：</span><span class="sxs-lookup"><span data-stu-id="5ef02-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="5ef02-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="5ef02-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="5ef02-126">設定事件收集器電腦</span><span class="sxs-lookup"><span data-stu-id="5ef02-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="5ef02-127">從 Windows Server 網域控制站上提高許可權的命令提示字元中執行下列命令，以設定 Windows 遠端管理：</span><span class="sxs-lookup"><span data-stu-id="5ef02-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="5ef02-128">**winrm qc-q**</span><span class="sxs-lookup"><span data-stu-id="5ef02-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="5ef02-129">執行下列命令來設定事件收集器服務：</span><span class="sxs-lookup"><span data-stu-id="5ef02-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="5ef02-130">**>wecutil qc/q**</span><span class="sxs-lookup"><span data-stu-id="5ef02-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="5ef02-131">建立來源起始的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ef02-131">Create a source initiated subscription.</span></span> <span data-ttu-id="5ef02-132">這可以透過程式設計方式來完成，方法是使用事件檢視器，或使用 [**Wecutil.exe**](wecutil.md)。</span><span class="sxs-lookup"><span data-stu-id="5ef02-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="5ef02-133">如需如何以程式設計方式建立訂閱的詳細資訊，請參閱 [建立來源起始訂用](creating-a-source-initiated-subscription.md)帳戶中的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="5ef02-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="5ef02-134">如果您使用 Wecutil.exe，則必須建立事件訂閱 XML 檔案，並使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="5ef02-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="5ef02-135">**>wecutil cs** *configurationFile.xml*</span><span class="sxs-lookup"><span data-stu-id="5ef02-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="5ef02-136">下列 XML 是訂用帳戶設定檔的內容範例，此檔案會建立來源起始的訂用帳戶，以便將遠端電腦的應用程式事件記錄檔中的事件轉送至事件收集器電腦上的 ForwardedEvents 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5ef02-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

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
    > <span data-ttu-id="5ef02-137">建立來源起始的訂閱時，如果 AllowedSourceDomainComputers、AllowedSourceNonDomainComputers/IssuerCAList、AllowedSubjectList 和 DeniedSubjectList 都是空的，則 "O:NSG： NSD： (A;;GA;;;DC)  (A;;GA;;;NS) 」將用作 AllowedSourceDomainComputers 的預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="5ef02-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="5ef02-138">預設描述項會授與網域電腦網域群組的成員，以及本機轉寄站) 的局域網路服務群組 (，這是為此訂用帳戶引發事件的能力。</span><span class="sxs-lookup"><span data-stu-id="5ef02-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="5ef02-139">驗證訂用帳戶是否正確運作</span><span class="sxs-lookup"><span data-stu-id="5ef02-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="5ef02-140">在事件收集器電腦上，完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5ef02-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="5ef02-141">請在 Windows Server 網域控制站上，從提高許可權的命令提示字元執行下列命令，以取得訂用帳戶的執行時間狀態：</span><span class="sxs-lookup"><span data-stu-id="5ef02-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="5ef02-142">**>wecutil gr** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="5ef02-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="5ef02-143">確認事件來源已連接。</span><span class="sxs-lookup"><span data-stu-id="5ef02-143">Verify that the event source has connected.</span></span> <span data-ttu-id="5ef02-144">在您建立要連接之事件來源的訂用帳戶之後，您可能需要等候直到原則中指定的重新整理間隔結束為止。</span><span class="sxs-lookup"><span data-stu-id="5ef02-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="5ef02-145">執行下列命令以取得訂用帳戶資訊：</span><span class="sxs-lookup"><span data-stu-id="5ef02-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="5ef02-146">**>wecutil gs** *&lt; subscriptionID &gt;*</span><span class="sxs-lookup"><span data-stu-id="5ef02-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="5ef02-147">從訂用帳戶資訊中取得 DeliveryMaxItems 值。</span><span class="sxs-lookup"><span data-stu-id="5ef02-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="5ef02-148">在事件來源電腦上，從事件訂用帳戶引發符合查詢的事件。</span><span class="sxs-lookup"><span data-stu-id="5ef02-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="5ef02-149">必須針對要轉送的事件引發事件的 DeliveryMaxItems 數目。</span><span class="sxs-lookup"><span data-stu-id="5ef02-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="5ef02-150">在事件收集器電腦上，驗證事件已轉送至 ForwardedEvents 記錄檔或訂用帳戶中指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5ef02-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="5ef02-151">轉送安全性記錄檔</span><span class="sxs-lookup"><span data-stu-id="5ef02-151">Forwarding the security log</span></span>

<span data-ttu-id="5ef02-152">若要能夠轉寄安全性記錄檔，您需要將 NETWORK SERVICE 帳戶新增到 EventLog Readers 群組。</span><span class="sxs-lookup"><span data-stu-id="5ef02-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="5ef02-153">設定來源起始的訂用帳戶，其中事件來源不在與事件收集器電腦相同的網域中</span><span class="sxs-lookup"><span data-stu-id="5ef02-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="5ef02-154">這些指示假設您擁有 Windows Server 網域控制站的系統管理員存取權。</span><span class="sxs-lookup"><span data-stu-id="5ef02-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="5ef02-155">在此情況下，由於遠端事件收集器電腦或電腦 (s) 不在網域控制站所提供的網域中，因此必須使用 Services (services.msc) 將 Windows 遠端管理設定為 [自動]，以啟動個別用戶端。</span><span class="sxs-lookup"><span data-stu-id="5ef02-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="5ef02-156">或者，您可以在每個遠端用戶端上執行 "winrm quickconfig"。</span><span class="sxs-lookup"><span data-stu-id="5ef02-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="5ef02-157">必須符合下列必要條件，才能建立訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ef02-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="5ef02-158">在事件收集器電腦上，從提升許可權的命令提示字元執行下列命令，以設定 Windows 遠端管理和事件收集器服務：</span><span class="sxs-lookup"><span data-stu-id="5ef02-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="5ef02-159">**winrm qc-q**</span><span class="sxs-lookup"><span data-stu-id="5ef02-159">**winrm qc -q**</span></span>

    <span data-ttu-id="5ef02-160">**>wecutil qc/q**</span><span class="sxs-lookup"><span data-stu-id="5ef02-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="5ef02-161">收集器電腦應該在本機電腦憑證存放區中有伺服器驗證憑證 (憑證與伺服器驗證目的) 。</span><span class="sxs-lookup"><span data-stu-id="5ef02-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="5ef02-162">在事件來源電腦上，執行下列命令以設定 Windows 遠端管理：</span><span class="sxs-lookup"><span data-stu-id="5ef02-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="5ef02-163">**winrm qc-q**</span><span class="sxs-lookup"><span data-stu-id="5ef02-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="5ef02-164">來源電腦的用戶端驗證憑證 (憑證，在本機電腦憑證存放區中) 用戶端驗證目的。</span><span class="sxs-lookup"><span data-stu-id="5ef02-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="5ef02-165">在事件收集器電腦上開啟埠5986。</span><span class="sxs-lookup"><span data-stu-id="5ef02-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="5ef02-166">若要開啟此埠，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="5ef02-166">To open this port, run the command:</span></span>

    <span data-ttu-id="5ef02-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span><span class="sxs-lookup"><span data-stu-id="5ef02-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="5ef02-168">憑證需求</span><span class="sxs-lookup"><span data-stu-id="5ef02-168">Certificates requirements</span></span>

- <span data-ttu-id="5ef02-169">伺服器驗證憑證必須安裝在本機電腦的個人存放區中的事件收集器電腦上。</span><span class="sxs-lookup"><span data-stu-id="5ef02-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="5ef02-170">此憑證的主體必須符合收集器的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5ef02-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="5ef02-171">用戶端驗證憑證必須安裝在本機電腦的個人存放區中的事件來源電腦上。</span><span class="sxs-lookup"><span data-stu-id="5ef02-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="5ef02-172">此憑證的主體必須符合電腦的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5ef02-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="5ef02-173">如果用戶端憑證是由不同的憑證授權單位單位所簽發，而不是其中一個事件收集器，則這些根和中繼憑證也必須安裝在事件收集器上。</span><span class="sxs-lookup"><span data-stu-id="5ef02-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="5ef02-174">如果用戶端憑證是由中繼憑證授權單位單位所發出，而收集器正在執行 Windows 2012 或更新版本，您就必須設定下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="5ef02-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="5ef02-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="5ef02-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="5ef02-176">確認伺服器和用戶端都能夠成功檢查所有憑證的撤銷狀態。</span><span class="sxs-lookup"><span data-stu-id="5ef02-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="5ef02-177">使用 **certutil** 命令可協助針對任何錯誤進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="5ef02-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="5ef02-178">請在本文中尋找詳細資訊： https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="5ef02-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="5ef02-179">在事件收集器上設定接聽程式</span><span class="sxs-lookup"><span data-stu-id="5ef02-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="5ef02-180">使用下列命令來設定憑證驗證：</span><span class="sxs-lookup"><span data-stu-id="5ef02-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="5ef02-181">**winrm set winrm/config/service/auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="5ef02-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="5ef02-182">具有伺服器驗證憑證的 WinRM HTTPS 接聽程式應該存在於事件收集器電腦上。</span><span class="sxs-lookup"><span data-stu-id="5ef02-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="5ef02-183">您可以使用下列命令來驗證：</span><span class="sxs-lookup"><span data-stu-id="5ef02-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="5ef02-184">**winrm e winrm/config/接聽程式**</span><span class="sxs-lookup"><span data-stu-id="5ef02-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="5ef02-185">如果您看不到 HTTPS 接聽程式，或如果 HTTPS 接聽程式的捲動方塊列印與收集器電腦上的伺服器驗證憑證的 thumb 列印不同，您可以刪除該接聽程式，並使用正確的 thumb 列印來建立新的接聽程式。</span><span class="sxs-lookup"><span data-stu-id="5ef02-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="5ef02-186">若要刪除 HTTPs 接聽程式，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="5ef02-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="5ef02-187">**winrm 刪除 winrm/config/接聽程式？位址 = \* + 傳輸 = HTTPS**</span><span class="sxs-lookup"><span data-stu-id="5ef02-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="5ef02-188">若要建立新的接聽程式，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="5ef02-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="5ef02-189">**winrm 建立 winrm/config/接聽程式？Address =&#42;+ Transport = HTTPS @ {Hostname = "** &lt; _收集器的 FQDN_ &gt; **";CertificateThumbprint = "** &lt; _伺服器驗證憑證的 Thumb 列印_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="5ef02-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="5ef02-190">設定事件收集器的憑證對應</span><span class="sxs-lookup"><span data-stu-id="5ef02-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="5ef02-191">建立新的本機使用者，並將它新增至本機系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="5ef02-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="5ef02-192">使用存在於電腦「信任的根憑證授權單位」或「中繼憑證授權單位單位」的憑證來建立憑證對應。</span><span class="sxs-lookup"><span data-stu-id="5ef02-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="5ef02-193">這是發出安裝在事件來源電腦上之憑證的根或中繼 CA 的憑證 *(為了避免混淆，這是憑證鏈中憑證正下方的 ca)*：</span><span class="sxs-lookup"><span data-stu-id="5ef02-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="5ef02-194">**winrm create winrm/config/service/certmapping？** = &lt; _發行 CA 憑證_ 的簽發者指紋 &gt; **+ Subject =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **";Password = "** &lt; _password_ &gt; **"}-remote： localhost**</span><span class="sxs-lookup"><span data-stu-id="5ef02-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="5ef02-195">從用戶端，使用下列命令來測試接聽程式和憑證對應：</span><span class="sxs-lookup"><span data-stu-id="5ef02-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="5ef02-196">**winrm g winrm/config-r:HTTPs：//** &lt;_事件收集器 FQDN_ &gt;**： 5986-a:certificate-certificate： "** &lt;_用戶端驗證憑證_ &gt; 的指紋 **"**</span><span class="sxs-lookup"><span data-stu-id="5ef02-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="5ef02-197">這應該會傳回事件收集器的 WinRM 設定。</span><span class="sxs-lookup"><span data-stu-id="5ef02-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="5ef02-198">如果未顯示設定，**請勿** 移過此步驟。</span><span class="sxs-lookup"><span data-stu-id="5ef02-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="5ef02-199">**此步驟會發生什麼事？**</span><span class="sxs-lookup"><span data-stu-id="5ef02-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="5ef02-200">用戶端會連線到事件收集器，並傳送指定的憑證</span><span class="sxs-lookup"><span data-stu-id="5ef02-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="5ef02-201">事件收集器會尋找發行 CA，並檢查是否為相符的憑證對應</span><span class="sxs-lookup"><span data-stu-id="5ef02-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="5ef02-202">事件收集器會驗證用戶端憑證鏈和撤銷狀態</span><span class="sxs-lookup"><span data-stu-id="5ef02-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="5ef02-203">如果上述步驟成功，就會完成驗證。</span><span class="sxs-lookup"><span data-stu-id="5ef02-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef02-204">您可能會收到「拒絕存取」錯誤抱怨驗證方法，這可能會造成誤導。</span><span class="sxs-lookup"><span data-stu-id="5ef02-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="5ef02-205">若要進行疑難排解，請檢查事件收集器上的 CAPI 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5ef02-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="5ef02-206">使用下列命令來列出已設定的 certmapping 專案： **winrm enum winrm/config/service/certmapping**</span><span class="sxs-lookup"><span data-stu-id="5ef02-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="5ef02-207">事件來源電腦設定</span><span class="sxs-lookup"><span data-stu-id="5ef02-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="5ef02-208">使用系統管理員帳戶登入，並開啟本機群組原則編輯器 (gpedit.msc) </span><span class="sxs-lookup"><span data-stu-id="5ef02-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="5ef02-209">流覽至本機電腦原則設定 [管理 \ 系統管理範本] Components\Event 轉送。</span><span class="sxs-lookup"><span data-stu-id="5ef02-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="5ef02-210">開啟 [設定目標訂用帳戶管理員的伺服器位址、重新整理間隔和簽發者憑證授權單位單位] 原則。</span><span class="sxs-lookup"><span data-stu-id="5ef02-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="5ef02-211">啟用原則，然後按一下 [顯示 ...] SubscriptionManagers按鈕。</span><span class="sxs-lookup"><span data-stu-id="5ef02-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="5ef02-212">在 [SubscriptionManagers] 視窗中，輸入下列字串：</span><span class="sxs-lookup"><span data-stu-id="5ef02-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="5ef02-213">**伺服器 = HTTPS：//** &lt;_事件收集器伺服器_ &gt; 的 FQDN **： 5986/wsman/SubscriptionManager/WEC，Refresh =** &lt;重新整理 _間隔（秒）_ &gt;**、IssuerCA =** &lt;_發行 CA 憑證的指紋_&gt;</span><span class="sxs-lookup"><span data-stu-id="5ef02-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="5ef02-214">執行下列命令列，以重新整理本機群組原則設定： Gpupdate/force</span><span class="sxs-lookup"><span data-stu-id="5ef02-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="5ef02-215">這些步驟應該會在來源電腦事件檢視器應用程式和服務 Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational 記錄檔中產生事件104，並顯示下列訊息：</span><span class="sxs-lookup"><span data-stu-id="5ef02-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="5ef02-216">「轉寄站已成功連接到位於位址 FQDN 的訂用帳戶管理員， &lt; &gt; 後面接著事件100，並顯示下列訊息：「 &lt; 已成功建立訂用帳戶 sub_name &gt; 。」</span><span class="sxs-lookup"><span data-stu-id="5ef02-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="5ef02-217">在事件收集器上，訂用帳戶執行時間狀態現在會顯示1個作用中的電腦。</span><span class="sxs-lookup"><span data-stu-id="5ef02-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="5ef02-218">開啟事件收集器上的 ForwardedEvents 記錄，並檢查您是否有從來源電腦轉送的事件。</span><span class="sxs-lookup"><span data-stu-id="5ef02-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="5ef02-219">在事件來源上授與用戶端憑證私密金鑰的許可權</span><span class="sxs-lookup"><span data-stu-id="5ef02-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="5ef02-220">在事件來源電腦上，開啟本機電腦的 [憑證管理] 主控台。</span><span class="sxs-lookup"><span data-stu-id="5ef02-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="5ef02-221">以滑鼠右鍵按一下用戶端憑證，然後管理私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="5ef02-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="5ef02-222">授與讀取權限給網路服務使用者。</span><span class="sxs-lookup"><span data-stu-id="5ef02-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="5ef02-223">事件訂用帳戶設定</span><span class="sxs-lookup"><span data-stu-id="5ef02-223">Event subscription configuration</span></span>

1. <span data-ttu-id="5ef02-224">在事件收集器中開啟事件檢視器，然後流覽至 [訂閱] 節點。</span><span class="sxs-lookup"><span data-stu-id="5ef02-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="5ef02-225">以滑鼠右鍵按一下 [訂閱]，然後選擇 [建立訂用帳戶 ...]</span><span class="sxs-lookup"><span data-stu-id="5ef02-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="5ef02-226">提供新訂用帳戶的名稱和選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="5ef02-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="5ef02-227">選取 [來源電腦起始] 選項，然後按一下 [選取電腦群組 ...]。</span><span class="sxs-lookup"><span data-stu-id="5ef02-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="5ef02-228">在 [電腦群組] 中，按一下 [新增非網域電腦 ...]</span><span class="sxs-lookup"><span data-stu-id="5ef02-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="5ef02-229">並輸入事件來源主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5ef02-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="5ef02-230">按一下 [新增憑證 ...]</span><span class="sxs-lookup"><span data-stu-id="5ef02-230">Click “Add Certificates…”</span></span> <span data-ttu-id="5ef02-231">並新增發出用戶端憑證之憑證授權單位單位的憑證。</span><span class="sxs-lookup"><span data-stu-id="5ef02-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="5ef02-232">您可以按一下 [查看憑證] 來驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="5ef02-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="5ef02-233">在 [憑證授權單位單位] 中，按一下 [確定] 以新增憑證。</span><span class="sxs-lookup"><span data-stu-id="5ef02-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="5ef02-234">新增電腦完成後，請按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="5ef02-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="5ef02-235">返回訂用帳戶屬性，按一下 [選取事件]。</span><span class="sxs-lookup"><span data-stu-id="5ef02-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="5ef02-236">藉由指定事件層級 (s) 、事件記錄 (s) 或事件來源 () 、事件識別碼 () 和任何其他篩選選項來設定事件查詢篩選器。</span><span class="sxs-lookup"><span data-stu-id="5ef02-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="5ef02-237">返回訂用帳戶屬性，按一下 [Advanced] .。。</span><span class="sxs-lookup"><span data-stu-id="5ef02-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="5ef02-238">選擇其中一個優化選項，以將事件從來源事件傳遞至事件收集器，或保留預設為正常：</span><span class="sxs-lookup"><span data-stu-id="5ef02-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="5ef02-239">**最小化頻寬**：傳遞的事件將會降低儲存頻寬的頻率。</span><span class="sxs-lookup"><span data-stu-id="5ef02-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="5ef02-240">將 **延遲降至最低**：系統會儘快傳遞事件以減少事件延遲。</span><span class="sxs-lookup"><span data-stu-id="5ef02-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="5ef02-241">將通訊協定變更為 HTTPS，然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="5ef02-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="5ef02-242">按一下 [確定] 以建立新的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ef02-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="5ef02-243">以滑鼠右鍵按一下並選擇 [執行時間狀態]，以檢查訂用帳戶的執行時間狀態</span><span class="sxs-lookup"><span data-stu-id="5ef02-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>
