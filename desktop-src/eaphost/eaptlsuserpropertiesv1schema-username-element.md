---
title: " (TLS) 的 Username 元素"
description: 瞭解 Username 元素。 這個元素會捕捉要在 EAP-Identity 回應中傳送的使用者名稱。
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Username 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106991298"
---
# <a name="username-element-tls"></a> (TLS) 的 Username 元素

**Username** 元素會捕捉要在 EAP-Identity 回應中傳送的使用者名稱。

如果 **Username** 專案不存在，則 eap-tls 會使用 [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) 元素中所參考之憑證的名稱。

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>規格需求



| 角色 | 支援的最低 OS 版本 |
|------|-------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1 架構](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





