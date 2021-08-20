---
description: 指定應該使用哪一個金鑰索引來加密無線流量。 只有當 keyType 設定為 &\# 0034; networkKey&0034; 時，才會使用此值 \# 。
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: 索引鍵索引 (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 04ac019fe23bcce91c813abcc9a2e88c02b71e90bec6be604cda9375c8e4a996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984148"
---
# <a name="keyindex-security-element"></a>索引鍵索引 (安全性) 元素

索引鍵索引 (security) 元素會指定應該使用哪一個金鑰索引來加密無線流量。 只有當 [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 設定為 "networkKey" 時，才會使用這個。

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista，Windows XP 只提供 SP3 \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



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

 

 




