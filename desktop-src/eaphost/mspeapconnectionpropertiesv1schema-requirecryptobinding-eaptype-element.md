---
title: RequireCryptoBinding (EapType) 元素
description: 指出是否要使用支援加密的伺服器進行驗證。
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- RequireCryptoBinding 元素 EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385085"
---
# <a name="requirecryptobinding-eaptype-element"></a>RequireCryptoBinding (EapType) 元素

**RequireCryptoBinding (EapType)** 元素指出是否要使用支援加密的伺服器進行驗證。

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

**RequireCryptoBinding** 元素是由 [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

如果 **RequireCryptoBinding** 元素為 TRUE，則 PEAP 會向不支援加密的伺服器進行驗證;若為 FALSE，則 PEAP 只會驗證支援加密的伺服器。 **RequireCryptoBinding** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





