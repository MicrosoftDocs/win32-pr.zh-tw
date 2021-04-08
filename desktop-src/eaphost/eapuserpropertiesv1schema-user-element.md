---
title: User 元素
description: 瞭解 User 元素。 透過 EAPHost Api 使用舊版方法時，不會使用這個元素。
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- 使用者元素 EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683123"
---
# <a name="user-element"></a>User 元素

透過 EAPHost Api 使用舊版方法時，不會使用 **使用者** 元素。

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>子元素



| 元素                                                  | 類型 | Description                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) |      | 捕捉方法類型和方法特定的認證資訊。<br/> |



## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eapuserpropertiesv1 架構](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





