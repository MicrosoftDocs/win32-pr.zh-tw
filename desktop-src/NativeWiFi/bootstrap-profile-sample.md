---
description: 在電腦加入網域之前，第一次用來驗證無線網路。
ms.assetid: e1a5ce76-9761-4c65-8b26-a44bf2eb1835
title: 啟動程式設定檔範例
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96c7daa6bdc72146400973d08c9e5780092b214a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193296"
---
# <a name="bootstrap-profile-sample"></a><span data-ttu-id="e281c-103">啟動程式設定檔範例</span><span class="sxs-lookup"><span data-stu-id="e281c-103">Bootstrap Profile Sample</span></span>

<span data-ttu-id="e281c-104">在電腦加入網域之前，第一次可以使用啟動程式設定檔範例來驗證無線網路。</span><span class="sxs-lookup"><span data-stu-id="e281c-104">The Bootstrap profile sample can be used to authenticate to a wireless network for the first time before the computer has joined a domain.</span></span>

<span data-ttu-id="e281c-105">此設定檔不會驗證遠端驗證撥入消費者服務 (RADIUS) server 所提供的憑證，而且不應該在電腦加入網域之後使用。</span><span class="sxs-lookup"><span data-stu-id="e281c-105">This profile does not validate the certificates presented by the Remote Authentication Dial-In User Service (RADIUS) server, and should not be used after the machine is joined to a domain.</span></span>

<span data-ttu-id="e281c-106">此範例設定為使用在企業模式下執行的 Wi-Fi Protected Access 2 安全性 (WPA2-Enterprise) 。</span><span class="sxs-lookup"><span data-stu-id="e281c-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="e281c-107">只要驗證方法是 PEAP Eap-mschapv2，就可以使用其他安全性類型。</span><span class="sxs-lookup"><span data-stu-id="e281c-107">Other security types can be used as long as the authentication method is PEAP-MSCHAPv2.</span></span>

<span data-ttu-id="e281c-108">**安裝了無線局域網路服務的 windows 7 和 Windows Server 2008 R2：** 變更會在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。</span><span class="sxs-lookup"><span data-stu-id="e281c-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="e281c-109">當無線局域網路設定檔中未設定此元素時， [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 的預設設定已變更。</span><span class="sxs-lookup"><span data-stu-id="e281c-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="e281c-110">在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上，預設設定會變更為 "false"。</span><span class="sxs-lookup"><span data-stu-id="e281c-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="e281c-111">Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。</span><span class="sxs-lookup"><span data-stu-id="e281c-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="e281c-112">如需詳細資訊，請參閱 [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 架構元素的描述。</span><span class="sxs-lookup"><span data-stu-id="e281c-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="e281c-113">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：**[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素的 [**name**](wlan-profileschema-name-wlanprofile-element.md)子系會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e281c-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="e281c-114">設定檔的名稱（儲存在設定檔存放區中）是衍生自 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素的 [**名稱**](wlan-profileschema-name-ssid-element.md)子系。</span><span class="sxs-lookup"><span data-stu-id="e281c-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="e281c-115">不支援 [**OneX**](onexschema-onex-element.md)元素的 [**cacheUserData**](onexschema-cacheuserdata-onex-element.md)、 [**authMode**](onexschema-authmode-onex-element.md)和 [**singleSignOn**](onexschema-singlesignon-onex-element.md)子系，而且應該在使用之前從設定檔中移除。</span><span class="sxs-lookup"><span data-stu-id="e281c-115">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleBootstrap</name>
    <SSIDConfig>
        <SSID>
            <name>SampleBootstrap</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <authMode>machineOrUser</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
               <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
               </EAPConfig>
           </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="e281c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="e281c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e281c-117">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="e281c-117">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="e281c-118">將 Windows Vista 無線用戶端加入網域</span><span class="sxs-lookup"><span data-stu-id="e281c-118">Joining a Windows Vista Wireless Client to a Domain</span></span>](https://www.microsoft.com/technet/network/wifi/vista_bootstrap_wireless.mspx)
</dt> </dl>

 

 



