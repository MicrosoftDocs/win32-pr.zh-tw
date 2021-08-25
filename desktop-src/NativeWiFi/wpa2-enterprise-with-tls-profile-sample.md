---
description: 使用可延伸的驗證通訊協定傳輸層級安全性 (eap-tls) 搭配憑證向網路驗證 (WPA2 Enterprise) 。
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: 使用 TLS 設定檔的 WPA2-Enterprise 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f3d96ab4a2e1d7fc12f0d6eac0fc67dc7ff14a03401e321b59e1a9926b829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912488"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a>使用 TLS 設定檔的 WPA2-Enterprise 範例

此範例設定檔會使用可延伸的驗證通訊協定傳輸層級安全性 (EAP-TLS) 搭配憑證來向網路進行驗證。

此範例設定為使用 Wi-Fi 在 Enterprise 模式下執行的 Protected Access 2 安全性 (WPA2 Enterprise) 。 WPA2-Enterprise 的安全性類型會使用 802.1 X 作為與後端的驗證交換。 進階加密標準 (AES) 加密類型。

EAP-TLS 認證是從憑證存放區取得。 如果以憑證存放區中的認證為基礎的驗證失敗，系統會提示使用者提供有效的認證。 如果第一次嘗試失敗，則不會使用替代的伺服器、根憑證授權單位或使用者名稱進行驗證。

此無線設定檔範例中使用的 EAPHost 設定衍生自 [eap-tls 連線屬性](../eaphost/eap-tls-connection-properties.md) 範例。

**安裝了無線局域網路服務 Windows 7 和 Windows Server 2008 R2：** 變更是在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。 當無線局域網路設定檔中未設定此元素時， [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 的預設設定已變更。 預設設定在 Windows 7 和已安裝無線局域網路服務 Windows Server 2008 R2 上變更為 "false"。 Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。 如需詳細資訊，請參閱 [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 架構元素的描述。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援 EAP-TLS。

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterpriseTLS</name>
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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[無線設定檔範例](wireless-profile-samples.md)
</dt> </dl>

 

 
