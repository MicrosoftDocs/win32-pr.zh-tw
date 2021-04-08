---
description: 使用可延伸的驗證通訊協定傳輸層級安全性 (EAP-TLS) 搭配憑證來向網路進行驗證。
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: 使用 TLS 設定檔的 WPA-Enterprise 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5300f8886d55ac713b0206b45f20857f22b2772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945050"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="03cba-103">使用 TLS 設定檔的 WPA-Enterprise 範例</span><span class="sxs-lookup"><span data-stu-id="03cba-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="03cba-104">此範例設定檔會使用可延伸的驗證通訊協定傳輸層級安全性 (EAP-TLS) 搭配憑證來向網路進行驗證。</span><span class="sxs-lookup"><span data-stu-id="03cba-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="03cba-105">此範例設定為使用在企業模式下執行 Wi-Fi 保護的存取安全性 (WPA-Enterprise) 。</span><span class="sxs-lookup"><span data-stu-id="03cba-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="03cba-106">WPA-Enterprise 的安全性類型會使用 802.1 X 作為與後端的驗證交換。</span><span class="sxs-lookup"><span data-stu-id="03cba-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="03cba-107">時態性金鑰完整性通訊協定 (TKIP) 用於加密。</span><span class="sxs-lookup"><span data-stu-id="03cba-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="03cba-108">EAP-TLS 認證是從憑證存放區取得。</span><span class="sxs-lookup"><span data-stu-id="03cba-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="03cba-109">如果以憑證存放區中的認證為基礎的驗證失敗，系統會提示使用者提供有效的認證。</span><span class="sxs-lookup"><span data-stu-id="03cba-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="03cba-110">如果第一次嘗試失敗，則不會使用替代的伺服器、根憑證授權單位或使用者名稱進行驗證。</span><span class="sxs-lookup"><span data-stu-id="03cba-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="03cba-111">此無線設定檔範例中使用的 EAPHost 設定衍生自 [eap-tls 連線屬性](../eaphost/eap-tls-connection-properties.md) 範例。</span><span class="sxs-lookup"><span data-stu-id="03cba-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="03cba-112">**安裝了無線局域網路服務的 windows 7 和 Windows Server 2008 R2：** 變更會在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。</span><span class="sxs-lookup"><span data-stu-id="03cba-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="03cba-113">當無線局域網路設定檔中未設定此元素時， [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 的預設設定已變更。</span><span class="sxs-lookup"><span data-stu-id="03cba-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="03cba-114">在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上，預設設定會變更為 "false"。</span><span class="sxs-lookup"><span data-stu-id="03cba-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="03cba-115">Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。</span><span class="sxs-lookup"><span data-stu-id="03cba-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="03cba-116">如需詳細資訊，請參閱 [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 架構元素的描述。</span><span class="sxs-lookup"><span data-stu-id="03cba-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="03cba-117">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援 EAP-TLS。</span><span class="sxs-lookup"><span data-stu-id="03cba-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="03cba-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="03cba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03cba-119">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="03cba-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
