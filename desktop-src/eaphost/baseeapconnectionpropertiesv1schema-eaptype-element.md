---
title: 'EapType 元素 (v1 架構連接屬性) '
description: '瞭解 EapType 元素。 這個元素會在 Eap 專案內捕獲特定方法的設定。 |EapType 元素 (v1 架構連接屬性) '
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696390"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>EapType 元素 (v1 架構連接屬性) 

**EapType** 元素會在 Eap 專案內捕獲特定方法的設定。

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>備註

**EapType** 元素是抽象的;每個方法都必須定義和使用實例檔中的衍生元素。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 架構](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





