---
title: EapMethodType) 元素的 VendorType (
description: 瞭解 (EapMethodType) 元素的 VendorType。 此元素是方法的廠商定義型別。
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- VendorType 元素 EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d83a87e531ff2343cd1c512aa345e84a75c1d8a82d783ea9e5a67a7530b8ecbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904595"
---
# <a name="vendortype-eapmethodtype-element"></a>EapMethodType) 元素的 VendorType (

**VendorType (EapMethodType)** 元素是該方法的廠商定義型別。

**VendorType** 元素是選擇性的。 如果使用，則 **是由** 網際網路指派的號碼授權單位 (IANA) 發出的唯一號碼。

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

**VendorType** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 角色 | 最低支援作業系統版本 |
|------|------------------------------|
| 用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eapcommon 架構](eapcommonschema-schema.md)
</dt> </dl>

 

 





