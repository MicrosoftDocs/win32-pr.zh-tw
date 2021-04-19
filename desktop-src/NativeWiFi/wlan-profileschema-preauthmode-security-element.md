---
description: 指出用戶端是否會使用預先驗證。
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: preAuthMode (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973628"
---
# <a name="preauthmode-security-element"></a>preAuthMode (安全性) 元素

PreAuthMode (security) 元素會指出用戶端是否會使用預先驗證。 WPA2 安全快速漫遊需要預先驗證。 只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。 如果 **PMKCacheMode** 已啟用，且此元素不存在，則預設值為「已停用」。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="preAuthMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
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

 

 




