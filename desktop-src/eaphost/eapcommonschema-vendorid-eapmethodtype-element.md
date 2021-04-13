---
title: " (EapMethodType) 元素的 VendorId"
description: 如果類型 (EapMethodType) 元素為 254 (擴充的 EAP 方法) ，則會參考定義方法的廠商。
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- VendorId 元素 EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508651"
---
# <a name="vendorid-eapmethodtype-element"></a> (EapMethodType) 元素的 VendorId

如果 [**類型 (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md)元素是 254 (擴充的 EAP 方法) ，則 **(EapMethodType)** 元素會參考定義方法的廠商。

**VendorId** 是選擇性的。 如果使用，則 **是由** 網際網路指派的號碼授權單位所發出的唯一號碼 (IANA) 。

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

**VendorId** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。

## <a name="remarks"></a>備註

針對特定方法， [**作者**](eapcommonschema-authorid-eapmethodtype-element.md) 和 **VendorId** 元素不需要相同的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 





