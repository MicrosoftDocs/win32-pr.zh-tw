---
description: 使用受保護的可延伸驗證通訊協定搭配 Microsoft 挑戰交握驗證通訊協定第2版（含 WPA-Enterprise）。
ms.assetid: e344c360-4ab5-4a5f-a1b2-b0fa890b8666
title: WPA-Enterprise 與 PEAP-MSCHAPv2 設定檔範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364cc7a9cc85e4c5e2ef908c0ac2a4726d6c5a96
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395043"
---
# <a name="wpa-enterprise-with-peap-mschapv2-profile-sample"></a><span data-ttu-id="5add0-103">WPA-Enterprise 與 PEAP-MSCHAPv2 設定檔範例</span><span class="sxs-lookup"><span data-stu-id="5add0-103">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>

<span data-ttu-id="5add0-104">此範例設定檔使用受保護的可延伸驗證通訊協定第2版 (PEAP-Eap-mschapv2) 搭配 \* UserName \* **/** _Password_ 來向網路進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5add0-104">This sample profile uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ to authenticate to the network.</span></span> <span data-ttu-id="5add0-105">系統會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="5add0-105">The user is prompted to enter credentials.</span></span>

<span data-ttu-id="5add0-106">此範例設定為使用在企業模式下執行 Wi-Fi 保護的存取安全性 (WPA-Enterprise) 。</span><span class="sxs-lookup"><span data-stu-id="5add0-106">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="5add0-107">WPA-Enterprise 的安全性類型會使用 802.1 X 作為與後端的驗證交換。</span><span class="sxs-lookup"><span data-stu-id="5add0-107">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="5add0-108">時態性金鑰完整性通訊協定 (TKIP) 用於加密。</span><span class="sxs-lookup"><span data-stu-id="5add0-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="5add0-109">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：**[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素的 [**name**](wlan-profileschema-name-wlanprofile-element.md)子系會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5add0-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="5add0-110">設定檔的名稱（儲存在設定檔存放區中）是衍生自 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素的 [**名稱**](wlan-profileschema-name-ssid-element.md)子系。</span><span class="sxs-lookup"><span data-stu-id="5add0-110">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
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
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="5add0-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="5add0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5add0-112">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="5add0-112">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



