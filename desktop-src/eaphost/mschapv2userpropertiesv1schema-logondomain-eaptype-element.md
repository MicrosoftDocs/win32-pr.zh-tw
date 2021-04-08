---
title: LogonDomain (EapType) 元素
description: 瞭解 LogonDomain (EapType) 元素。 這個元素會識別要驗證之使用者或電腦的網域。
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- LogonDomain 元素 EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024080"
---
# <a name="logondomain-eaptype-element"></a>LogonDomain (EapType) 元素

**LogonDomain (EapType)** 元素會識別要驗證之使用者或電腦的網域。

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

**LogonDomain** 元素是由 [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **LogonDomain (EapType)** 元素不存在，則會使用 winlogon 的網域。 這是選擇性的項目。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





