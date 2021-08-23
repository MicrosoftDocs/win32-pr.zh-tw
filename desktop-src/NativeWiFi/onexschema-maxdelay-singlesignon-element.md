---
description: 指定單一登入連接嘗試失敗之前的延遲上限（以秒為單位）。
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: maxDelay (singleSignOn) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cd4e82e8031f57e9672dd11a066a9a1fb2e8f3540c93dc4e1898afa4f1cf6302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684838"
---
# <a name="maxdelay-singlesignon-element"></a>maxDelay (singleSignOn) 元素

MaxDelay (singleSignOn) 元素會指定單一登入連接嘗試失敗之前的延遲上限（以秒為單位）。

這是選擇性的項目。 當設定檔中未指定 maxDelay 時，會使用10秒的值。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**MaxDelay** 元素是由 [**singleSignOn**](onexschema-singlesignon-onex-element.md)元素定義。

## <a name="remarks"></a>備註

您可以使用 **netsh wlan set profileparameter** 命令，在命令列設定這個參數。 如需詳細資訊，請參閱 [無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
