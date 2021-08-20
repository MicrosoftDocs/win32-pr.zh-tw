---
title: EnableQuarantineChecks (EapType) 元素
description: 瞭解 EnableQuarantineChecks (EapType) 元素。 此元素指出 (NAP) 檢查是否執行網路存取保護。
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- EnableQuarantineChecks 元素 EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 774d2ebe432dde9b16b10257c05b8419d6905a94f4f0a9ddf9fb4315f056071f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904045"
---
# <a name="enablequarantinechecks-eaptype-element"></a>EnableQuarantineChecks (EapType) 元素

**EnableQuarantineChecks (EapType)** 元素指出是否 (NAP) 檢查來執行網路存取保護。

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

**EnableQuarantineChecks** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **EnableQuarantineChecks** 元素為 TRUE，則 PEAP 會執行 NAP 檢查;若為 FALSE，PEAP 將不會執行 NAP 檢查。 **EnableQuarantineChecks** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[mspeapconnectionpropertiesv1 架構元素](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





