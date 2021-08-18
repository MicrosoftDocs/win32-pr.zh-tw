---
title: DifferentUsername (EapType) 元素
description: 瞭解 DifferentUsername (EapType) 元素。 此元素決定要使用的使用者名稱。
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- DifferentUsername 元素 EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2980a55e76d238578822cfc8db54a9b6c324e21d4a8f0481ab9bc91e050fb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984088"
---
# <a name="differentusername-eaptype-element"></a>DifferentUsername (EapType) 元素

**DifferentUsername (EapType)** 元素會決定要使用的使用者名稱。

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

**DifferentUsername** 元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **DifferentUserName** 元素為 TRUE，則 eap-tls 應該使用憑證上所顯示的名稱以外的使用者名稱。 如果 **DifferentUserName** 元素為 FALSE，則 eap-tls 會使用憑證上出現的使用者名稱。

**DifferentUserName** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1 架構元素](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





