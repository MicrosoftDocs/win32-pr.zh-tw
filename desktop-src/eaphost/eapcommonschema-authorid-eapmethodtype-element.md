---
title: 作者 (EapMethodType) 元素
description: 瞭解 (EapMethodType) 元素的作者。 作者 (EapMethodType) 專案是指方法作者。
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- 作者元素 EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f15c5fc981592bb82f9ad52d590f12ac0b1f4b20af3537a511d01dd0a8cc15e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021748"
---
# <a name="authorid-eapmethodtype-element"></a>作者 (EapMethodType) 元素

作者 **(EapMethodType)** 專案是指方法作者。

作者是由網際網路指派的數位授權單位 (IANA) 發出的唯一號碼。

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

**作者** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

針對特定方法， **作者** 和 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) 元素不需要相同的。

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

 

 





