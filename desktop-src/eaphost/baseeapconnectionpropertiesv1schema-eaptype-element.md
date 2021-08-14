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
ms.openlocfilehash: 3f2681e5682ad98ab5f4185174996920315d8c3b81dde8ba69d13ca178904ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498784"
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
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[baseeapconnectionpropertiesv1 架構](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





