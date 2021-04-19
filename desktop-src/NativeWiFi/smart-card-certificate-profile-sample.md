---
description: 用來連線到使用可延伸驗證通訊協定傳輸層級安全性的網路 (EAP-TLS) 儲存在智慧卡上以進行 802.1 X 驗證的憑證。
ms.assetid: cb6758fc-1cce-4e62-adf7-0976957a49b0
title: 智慧卡憑證設定檔範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13373ea66a7ed93ad527715de9f32d4f72705be5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985129"
---
# <a name="smart-card-certificate-profile-sample"></a>智慧卡憑證設定檔範例

此設定檔範例示範用來連線到網路的有線網路設定檔，該網路使用可延伸的驗證通訊協定傳輸層級安全性 (EAP-TLS) 儲存在智慧卡上以進行 802.1 X 驗證的憑證。 若要查看使用儲存在本機電腦上之 EAP-TLS 憑證的設定檔，請參閱 [電腦憑證設定檔範例](machine-certificate-profile-sample.md)。

此無線設定檔範例中使用的 EAPHost 設定衍生自 [eap-tls 連線屬性](../eaphost/eap-tls-connection-properties.md) 範例。

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
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
                                        <eapTls:SmartCard />
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
</LANProfile>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[有線設定檔範例](wired-profile-samples.md)
</dt> </dl>

 

 
