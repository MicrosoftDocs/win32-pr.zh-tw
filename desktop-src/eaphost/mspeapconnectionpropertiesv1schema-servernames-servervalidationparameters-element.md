---
title: 'ServerNames (ServerValidationParameters) 元素 (PEAP) '
description: '瞭解 ServerNames (ServerValidationParameters) 元素。 此元素代表以分號分隔的伺服器名稱清單。 |ServerNames (ServerValidationParameters) 元素 (PEAP) '
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- ServerNames 元素 EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976423"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>ServerNames (ServerValidationParameters) 元素 (PEAP) 

**ServerNames (ServerValidationParameters)** 元素表示以分號分隔的伺服器名稱清單。

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

**ServerNames** 元素是由 [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

每個伺服器名稱會以分號分隔，而且可以使用正則運算式來表示。 **ServerNames** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





