---
description: 指出將保留 PMK 快取的時間長度（以分鐘為單位）。
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: PMKCacheTTL (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972020"
---
# <a name="pmkcachettl-security-element"></a>PMKCacheTTL (安全性) 元素

PMKCacheTTL (security) 元素指出 PMK 快取將保留的時間長度（以分鐘為單位）。 只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。

PMK 快取會在 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格中說明。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**安全**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**(MSM) 的安全性**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




