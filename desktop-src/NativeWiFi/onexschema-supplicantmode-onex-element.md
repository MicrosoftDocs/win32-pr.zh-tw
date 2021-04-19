---
description: 指定用於 EAPOL-Start 訊息的傳輸方法。
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: supplicantMode (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989390"
---
# <a name="supplicantmode-onex-element"></a>supplicantMode (OneX) 元素

SupplicantMode (OneX) 元素會指定用於 EAPOL-Start 訊息的傳輸方法。 下表說明可能出現的值。



| 值               | 描述                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inhibitTransmission | EAPOL-Start 不會傳送訊息。 僅適用于有線局域網路設定檔。                                                                                             |
| includeLearning     | 用戶端會根據網路功能決定傳送 EAPOL-Start 封包的時機。 EAPOL-Start 訊息只會在必要時傳送。 僅適用于有線局域網路設定檔。 |
| compliant           | EAPOL-Start 的訊息會由 802.1 X 所指定的方式傳輸。 適用于有線和無線局域網路設定檔。                                                             |



 

這是選擇性的項目。 當設定檔中未指定 supplicantMode 時，會將的值 `compliant` 用於有線和無線局域網路設定檔。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**SupplicantMode** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。

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

 

 




