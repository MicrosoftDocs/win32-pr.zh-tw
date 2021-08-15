---
title: 密碼 (EapType) 元素
description: 深入瞭解密碼 (EapType) 元素。 這個元素會識別要驗證之使用者或電腦的密碼。
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- 密碼元素 EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbbcb7b0acd372bbe71ee6d22f44a736948b145378f62f40820e3de53d77b875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273197"
---
# <a name="password-eaptype-element"></a>密碼 (EapType) 元素

**密碼 (EapType)** 元素會識別要驗證之使用者或電腦的密碼。

``` syntax
<xs:element name="Password"
    type="string"
 />
```

**Password** 元素是由 [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **密碼 (EapType)** 元素不存在，則會從 winlogon 取得密碼雜湊。 這是選擇性的項目。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mschapv2userpropertiesv1 架構](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





