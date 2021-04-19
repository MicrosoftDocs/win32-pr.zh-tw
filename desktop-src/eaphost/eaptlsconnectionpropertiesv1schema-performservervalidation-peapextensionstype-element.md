---
title: 'PerformServerValidation (EapType) '
description: '瞭解 PerformServerValidation 元素。 這個元素會指出是否執行伺服器驗證。 |PerformServerValidation (EapType) '
ms.assetid: f6233bff-18e4-45b4-b598-839fa198f676
keywords:
- 元素 EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655379676bd117b89a6fe41a8d6895260e71a2bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976436"
---
# <a name="performservervalidation-eaptype"></a>PerformServerValidation (EapType) 

**PerformServerValidation (EapType)** 元素指出是否執行伺服器驗證。

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS:PerformServerValidation "
 />
```

元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) 元素所定義。

## <a name="remarks"></a>備註

**PerformServerValidation** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



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
</dt> <dt>

[**PerformServerValidation (EapType)**](eaptlsconnectionpropertiesv2shema-tlsextensions-tlsextensionstype-element.md)
</dt> </dl>

 

 





