---
description: 包含十六進位格式的無線區域網路 SSID。
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: hex (SSID) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 666562f7a476505dbb0ff23d5354e0f073505d9dd5195bcae17543294cc5f176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799888"
---
# <a name="hex-ssid-element"></a>hex (SSID) 元素

Hex (SSID) 元素包含十六進位格式的無線區域網路 SSID。

``` syntax
<xs:element name="hex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

元素是由 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素所定義。

## <a name="remarks"></a>備註

雖然 **hex** 和 [**name**](wlan-profileschema-name-ssid-element.md) 元素是選擇性的，但至少一個 **hex** 或 [**name**](wlan-profileschema-name-ssid-element.md) 元素必須顯示為 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素的子系。

當設定檔資訊轉換成 SSID 時，如果有 (，則會將 **hex** 元素轉換成 ssid 如果) 存在，則會忽略 [**name**](wlan-profileschema-name-ssid-element.md) 元素。 如果 **hex** 元素不存在，則會將 [**name**](wlan-profileschema-name-ssid-element.md) 元素轉換為使用 Unicode 轉換的 SSID。

當 SSID 儲存在設定檔中時，一律會產生 **hex** 元素。 只有當 SSID 和 XML 設定檔產生的 ASCII 與 Unicode 轉換都成功時，才會產生 [**name**](wlan-profileschema-name-ssid-element.md) 元素。 當原始 SSID 的某些資訊轉換成 [**名稱**](wlan-profileschema-name-ssid-element.md)時，可能會遺失。

## <a name="examples"></a>範例

若要查看使用 **hex** 元素的範例設定檔，請參閱 [FIPS 設定檔範例](fips-profile-sample.md)。

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

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




