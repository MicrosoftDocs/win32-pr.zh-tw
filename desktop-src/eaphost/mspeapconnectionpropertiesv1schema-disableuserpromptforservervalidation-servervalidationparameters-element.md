---
title: 'DisableUserPromptForServerValidation 元素 (PEAP) '
description: '瞭解 DisableUserPromptForServerValidation (ServerValidationParameters) 元素。 指出是否應要求使用者進行伺服器驗證。 |DisableUserPromptForServerValidation 元素 (PEAP) '
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
keywords:
- DisableUserPromptForServerValidation 元素 EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c032c4c0dcb67f60f64fe2b447fd1af7061df51ed19586f4ee15b43d6a6f870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561758"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>DisableUserPromptForServerValidation (ServerValidationParameters) 元素 (PEAP) 

**DisableUserPromptForServerValidation (ServerValidationParameters)** 元素指出是否應要求使用者進行伺服器驗證。

如果 **DisableUserPromptForServerValidation** 為 TRUE，則 eap-tls 會執行伺服器驗證，而不需要使用者輸入;如果驗證失敗，則 EAP-TLS 會驗證失敗。 如果 **DisableUserPromptForServerValidation** 為 FALSE，則會提示使用者輸入已驗證的伺服器憑證或名稱，或 (CA) 的根憑證授權單位。

**DisableUserPromptForServerValidation** 元素是選擇性的。

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

**DisableUserPromptForServerValidation** 元素是由 [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**架構實例中可能的直接父元素**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構元素](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





