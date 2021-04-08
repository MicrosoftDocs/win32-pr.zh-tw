---
description: 包含無線區域網路的 SSID。
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: " (SSID 的名稱) 元素"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851163"
---
# <a name="name-ssid-element"></a> (SSID 的名稱) 元素

 (SSID 的名稱) 元素包含無線區域網路的 SSID。

``` syntax
<xs:element name="name">
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
```

元素是由 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素所定義。

## <a name="remarks"></a>備註

名稱會區分大小寫。

雖然 [**hex**](wlan-profileschema-hex-ssid-element.md) 和 **name** 元素是選擇性的，但至少一個 **hex** 或 **name** 元素必須顯示為 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) 元素的子系。

當設定檔資訊轉換成 SSID 時，如果有 (，則會將 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素轉換成 ssid 如果) 存在，則會忽略 **name** 元素。 如果 **hex** 元素不存在，則會將 **name** 元素轉換為使用 Unicode 轉換的 SSID。

當 SSID 儲存在設定檔中時，一律會產生 [**hex**](wlan-profileschema-hex-ssid-element.md) 元素。 只有當 SSID 和 XML 設定檔產生的 ASCII 與 Unicode 轉換都成功時，才會產生 **name** 元素。 當原始 SSID 的某些資訊轉換成 **名稱** 時，可能會遺失。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** XML escape 字元（例如 &）不會顯示。 針對 windows XP 加裝 SP3 和適用于 Windows XP SP2 的無線區域網路 API 所部署的設定檔，請避免在 SSID 名稱中使用 XML escape 字元。

## <a name="examples"></a>範例

若要查看使用 **name** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

[**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




