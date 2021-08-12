---
description: 包含無線區域網路的 SSID。
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID (SSIDConfig) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d58ed866e79269e604fe49ad8afe65d557f27a90d0be03904b8d27da5ac5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619055"
---
# <a name="ssid-ssidconfig-element"></a>SSID (SSIDConfig) 元素

SSID (SSIDConfig) 元素包含無線區域網路的 SSID。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 設定檔中最多隻能出現一個 **SSID** 元素。

``` syntax
<xs:element name="SSID"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="name"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
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
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**SSID** 元素是由 [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                              | 類型 | 描述                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | 包含十六進位格式的無線區域網路 SSID。<br/> |
| [**名字**](wlan-profileschema-name-ssid-element.md) |      | 包含無線區域網路的 SSID。<br/>                      |



## <a name="remarks"></a>備註

雖然 [**hex**](wlan-profileschema-hex-ssid-element.md) 和 [**name**](wlan-profileschema-name-ssid-element.md) 元素是選擇性的，但至少一個 **hex** 或 [**name**](wlan-profileschema-name-ssid-element.md) 元素必須顯示為 **SSID** 元素的子系。

當設定檔資訊轉換成 SSID 時，如果有 (，則會將 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素轉換成 ssid 如果) 存在，則會忽略 [**name**](wlan-profileschema-name-ssid-element.md) 元素。 如果 **hex** 元素不存在，則會將 [**name**](wlan-profileschema-name-ssid-element.md) 元素轉換為使用 Unicode 轉換的 SSID。

當 SSID 儲存在設定檔中時，一律會產生 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素。 只有當 SSID 和 XML 設定檔產生的 ASCII 與 Unicode 轉換都成功時，才會產生 [**name**](wlan-profileschema-name-ssid-element.md) 元素。 當原始 SSID 的某些資訊轉換成 [**名稱**](wlan-profileschema-name-ssid-element.md)時，可能會遺失。

## <a name="examples"></a>範例

若要查看使用 **SSID** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




