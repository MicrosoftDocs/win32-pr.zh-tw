---
description: 指定在驗證嘗試失敗之後，用戶端不會重新嘗試驗證的時間長度（以秒為單位）。
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: heldPeriod (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981560"
---
# <a name="heldperiod-onex-element"></a>heldPeriod (OneX) 元素

HeldPeriod (OneX) 元素會指定用戶端在驗證嘗試失敗之後不會重新嘗試驗證的時間長度（以秒為單位）。

這是選擇性的項目。 當設定檔中未指定 heldPeriod 時，會使用1秒的值。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="heldPeriod">
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

**HeldPeriod** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 




