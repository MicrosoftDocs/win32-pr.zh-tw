---
title: EAP MS-CHAPv2 連接屬性
description: 瞭解 EAP MS-CHAPv2 連接屬性。 請參閱 mschapv2connectionpropertiesv1 舊版架構實例的範例。
ms.assetid: d6a057e0-56f6-4a31-9391-fde631ac2898
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e353c4685e131c2e7301db35de26d927b5882c06
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383137"
---
# <a name="eap-ms-chapv2-connection-properties"></a>EAP MS-CHAPv2 連接屬性

這個範例是 [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) 舊版架構的實例。

``` syntax
  <?xml version="1.0" ?> 
  <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
    xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
    xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
    <EapMethod>
      <eapCommon:Type>26</eapCommon:Type> 
      <eapCommon:AuthorId>0</eapCommon:AuthorId> 
    </EapMethod>
    <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
      xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
      xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
      <baseEap:Eap>
        <baseEap:Type>26</baseEap:Type> 
        <msChapV2:EapType>
        <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
        </msChapV2:EapType>
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

 

 




