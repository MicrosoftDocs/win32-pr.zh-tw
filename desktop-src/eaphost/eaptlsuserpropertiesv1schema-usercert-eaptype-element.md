---
title: UserCert (EapType) 元素
description: 指應用於驗證的憑證 SHA-1 雜湊。
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- UserCert 元素 EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef25a43bf13b1cfb1e4b03f78f5772567b3bfb92f1c31bb810da7882a4d3e1c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067228"
---
# <a name="usercert-eaptype-element"></a>UserCert (EapType) 元素

**UserCert (EapType)** 元素指的是應用於驗證的憑證 sha-1 雜湊。

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

**UserCert** 元素是由 [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsuserpropertiesv1 架構](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





