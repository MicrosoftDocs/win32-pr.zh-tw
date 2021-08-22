---
description: 指定無線區域網路上所使用的802.11 無線區域網路標準。
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: phyType (連接) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f9af94923f9160d18a9787b61036d5cf4104aede6488e2219b18a84325da46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684018"
---
# <a name="phytype-connectivity-element"></a>phyType (連接) 元素

PhyType (connectivity) 元素會指定無線區域網路上所使用的802.11 無線區域網路標準。

您可以指定多個 **phyType**。 如果未指定任何 **phyType** ，則可以使用設定檔來連接至任何 **phyType**。 只有 Windows Vista Service Pack 1 (SP1) 和更新版本的作業系統才支援 "n" 值。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

專案是由 [**connectivity**](wlan-profileschema-connectivity-msm-element.md) 元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**連接**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**(MSM) 的連線能力**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




