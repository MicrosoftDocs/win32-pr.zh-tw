---
title: 'Username 元素 (CHAP) '
description: 瞭解 Username 元素，這會識別正在驗證的使用者。 請參閱語法範例，並查看其他可用的資源。
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
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
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933613"
---
# <a name="username-element-chap"></a>Username 元素 (CHAP) 

**Username** 元素會識別要驗證的使用者。

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a>備註

如果 **Username** 元素不存在，則會從 winlogon 取得使用者名稱。 這是選擇性的項目。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1 架構](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





