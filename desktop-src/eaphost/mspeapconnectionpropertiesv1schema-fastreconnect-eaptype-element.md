---
title: FastReconnect (EapType) 元素
description: 瞭解 FastReconnect (EapType) 元素。 此元素指出是否要執行快速重新連接。
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- FastReconnect 元素 EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965453"
---
# <a name="fastreconnect-eaptype-element"></a>FastReconnect (EapType) 元素

**FastReconnect (EapType)** 元素指出是否要執行快速重新連接。

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

**FastReconnect** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **FastReconnect** 元素為 TRUE，則 PEAP 會嘗試執行快速重新連線;如果為 FALSE，則 PEAP 會執行完整驗證。 **FastReconnect** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





