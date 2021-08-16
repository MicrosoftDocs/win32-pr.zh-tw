---
title: InnerEapOptional (EapType) 元素
description: 瞭解 InnerEapOptional (EapType) 元素。 此元素會指出是否要執行來賓存取。
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- InnerEapOptional 元素 EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404588"
---
# <a name="innereapoptional-eaptype-element"></a>InnerEapOptional (EapType) 元素

**InnerEapOptional (EapType)** 元素指出是否要執行來賓存取。

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

**InnerEapOptional** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **InnerEapOptional** 專案是 TRUE，則 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素必須存在，並且描述內部方法和其設定;若為 FALSE，則 PEAP 會執行來賓存取。 **InnerEapOptional** 元素是選擇性的。

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

 

 





