---
description: 包含1位元組的 hexBinary，用來區別相同 IHV 所建立的 Nic。
ms.assetid: fd6bae3d-27a8-4bff-9340-b444312b8216
title: 輸入 (OUIHeader) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 234b30883df463d7c336ce7d270e574d41a5cabe9924c327a35ff1a31ee65632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797499"
---
# <a name="type-ouiheader-element"></a>輸入 (OUIHeader) 元素

類型 (OUIHeader) 元素包含1個位元組的 hexBinary，可用來區別相同 IHV 所建立的 Nic。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="type">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) 元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




