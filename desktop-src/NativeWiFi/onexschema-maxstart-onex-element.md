---
description: 指定傳送 EAPOL-Start 訊息的數目上限。
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: maxStart (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7c50945b8de53b6d058556e3b5c995d3ec17bfdc8f8d55ec3dc2e6e56089b2a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800758"
---
# <a name="maxstart-onex-element"></a>maxStart (OneX) 元素

MaxStart (OneX) 元素會指定傳送的 EAPOL-Start 訊息數目上限。 在傳送 EAPOL-Start 訊息的數目上限之後，用戶端會假設網路上沒有任何驗證器存在。

這是選擇性的項目。 當設定檔中未指定 maxStart 時，會使用3個訊息的值。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**MaxStart** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 




