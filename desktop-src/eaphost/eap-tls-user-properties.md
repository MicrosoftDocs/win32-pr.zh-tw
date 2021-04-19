---
title: EAP-TLS 使用者屬性
description: 瞭解 EAP-TLS 使用者屬性。 請參閱 eaptlsuserpropertiesv1 舊版架構實例的範例。
ms.assetid: d5a265a9-4c09-4a60-a188-dff471ee72c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d104d8eb5eaca67985be5574504dfbe57b5a6f9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106965260"
---
# <a name="eap-tls-user-properties"></a>EAP-TLS 使用者屬性

此範例是 [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md) 舊版架構的實例。

``` syntax
 <?xml version="1.0" ?> 
 <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials"> 
   <EapMethod>
     <eapCommon:Type>13</eapCommon:Type> 
     <eapCommon:AuthorId>0</eapCommon:AuthorId> 
   </EapMethod>
   <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1" 
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1" 
     xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsUserPropertiesV1">
     <baseEap:Eap>
       <baseEap:Type>13</baseEap:Type> 
       <eapTls:EapType>
         <eapTls:Username>ias-domain\test</eapTls:Username> 
         <eapTls:UserCert /> 
       </eapTls:EapType>
     </baseEap:Eap>
   </Credentials>
 </EapHostUserCredentials>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用者屬性](user-profiles.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> </dl>

 

 




