---
title: EAP MS-CHAPv2 使用者屬性
description: 瞭解 EAP MS-CHAPv2 使用者屬性。 請參閱 mschapv2userpropertiesv1 舊版架構實例的範例。
ms.assetid: f360913d-be5d-4ef0-96c9-652e4d08d9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0082d1672d32b87fe98816fb5baeac791df343d0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383134"
---
# <a name="eap-ms-chapv2-user-properties"></a>EAP MS-CHAPv2 使用者屬性

此範例是 [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md) 舊版架構的實例。

``` syntax
<?xml version="1.0" ?> 
 <EapHostUserCredentials xmlns="https://www.microsoft.com/provisioning/EapHostUserCredentials" 
   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodUserCredentials">
   <EapMethod>
     <eapCommon:Type>26</eapCommon:Type> 
     <eapCommon:AuthorId>0</eapCommon:AuthorId> 
   </EapMethod>
   <Credentials xmlns:eapUser="https://www.microsoft.com/provisioning/EapUserPropertiesV1" 
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapUserPropertiesV1" 
     xmlns:MsPeap="https://www.microsoft.com/provisioning/MsPeapUserPropertiesV1" 
     xmlns:MsChapV2="https://www.microsoft.com/provisioning/MsChapV2UserPropertiesV1">
     <baseEap:Eap>
       <baseEap:Type>26</baseEap:Type> 
       <MsChapV2:EapType>
         <MsChapV2:Username>test</MsChapV2:Username> 
         <MsChapV2:Password>test</MsChapV2:Password> 
         <MsChapV2:LogonDomain>ias-domain</MsChapV2:LogonDomain> 
       </MsChapV2:EapType>
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

 

 




