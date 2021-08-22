---
title: PEAP-TLS 連接屬性
description: 瞭解 PEAP-TLS 連接屬性。 請參閱 eaptlsconnectionpropertiesv1 舊版架構實例的範例。
ms.assetid: 1128b3f7-eba7-484e-a3d8-070d37e9c57f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be661834c6a1053d34ba5c6a8cee7f7d491537ce0153011772c1b29cf78ef89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784806"
---
# <a name="peap-tls-connection-properties"></a>PEAP-TLS 連接屬性

這個範例是 [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md) 舊版架構的實例。

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig"
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon"
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>25</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1"
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1"
      xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>25</baseEap:Type> 
        <msPeap:EapType>
          <msPeap:ServerValidation>
            <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
            <msPeap:ServerNames /> 
            <msPeap:TrustedRootCA /> 
          </msPeap:ServerValidation>
          <msPeap:FastReconnect>true</msPeap:FastReconnect> 
          <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
          <baseEap:Eap>
            <baseEap:Type>13</baseEap:Type> 
            <eapTls:EapType>
              <eapTls:CredentialsSource>
                <eapTls:CertificateStore /> 
              </eapTls:CredentialsSource>
              <eapTls:ServerValidation>
                <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                <eapTls:ServerNames /> 
                <eapTls:TrustedRootCA /> 
              </eapTls:ServerValidation>
              <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
            </eapTls:EapType>
          </baseEap:Eap>
          <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
          <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
        </msPeap:EapType>
      </baseEap:Eap>
    </Config>
  </EapHostConfig>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接屬性](connection-profiles.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> </dl>

 

 




