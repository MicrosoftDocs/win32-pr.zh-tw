---
title: 'EapType 元素 (基底使用者屬性) '
description: '瞭解 EapType 元素。 這個元素會在 Eap 專案內捕獲特定方法的設定。 |EapType 元素 (基底使用者屬性) '
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974811"
---
# <a name="eaptype-element-base-user-properties"></a>EapType 元素 (基底使用者屬性) 

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
|-------------------------------------|------------------------------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[baseeapuserpropertiesv1 架構](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





