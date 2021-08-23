---
description: 指定用戶端等候驗證器回應的最大時間長度（以秒為單位）。
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: authPeriod (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ccaef08f65baffa0d7b9a921afd9db78a6ac6c6dd1d0bf4fd8075454fe38be21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684857"
---
# <a name="authperiod-onex-element"></a>authPeriod (OneX) 元素

AuthPeriod (OneX) 元素會指定用戶端等待驗證器回應的最大時間長度（以秒為單位）。 如果在指定的期間內未收到回應，用戶端會假設網路上沒有任何驗證器存在。

這是選擇性的項目。 當設定檔中未指定 authPeriod 時，會使用值18秒。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="authPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**AuthPeriod** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

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

 

 




