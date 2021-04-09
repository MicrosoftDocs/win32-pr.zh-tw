---
description: 包含一或多個適用于無線區域網路的 Ssid。
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: SSIDConfig (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849623"
---
# <a name="ssidconfig-wlanprofile-element"></a>SSIDConfig (WLANProfile) 元素

SSIDConfig (WLANProfile) 元素包含一個或多個適用于無線區域網路的 Ssid。

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="nonBroadcast"
                type="boolean"
                minOccurs="0"
             />
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

**SSIDConfig** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。

## <a name="child-elements"></a>子元素



| 元素                                                                    | 類型                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | 包含十六進位格式的無線區域網路 SSID。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**名字**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | 包含無線區域網路的 SSID (區分大小寫) 名稱。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**廣播**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | 指出網路是否會廣播其 SSID。<br/> 如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 ESS，此值可以是 **TRUE** 或 **FALSE**。 如果這個元素不存在，則預設值為 **TRUE** 。<br/> 如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 IBSS，則這個值必須是 **FALSE**。<br/> Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。<br/> |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | 包含無線區域網路的 SSID。<br/> Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 設定檔中最多隻能出現一個 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素。<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>範例

若要查看使用 **SSIDConfig** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
