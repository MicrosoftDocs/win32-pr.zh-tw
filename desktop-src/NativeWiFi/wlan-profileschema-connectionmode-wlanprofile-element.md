---
description: 指出無線區域網路的連接是否應該自動或由使用者起始。
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: connectionMode (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a6ef18eff8ba27a3169399f1f10e0707c4e0b3c010d54830ad8f8f997c5e1b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684437"
---
# <a name="connectionmode-wlanprofile-element"></a>connectionMode (WLANProfile) 元素

ConnectionMode (WLANProfile) 元素表示無線區域網路的連接是否應該自動或由使用者起始。

如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 ESS，此值可以是 auto 或 manual。 如果這個元素不存在，則預設值為 auto。

如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 IBSS，則這個值必須是手動。

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**ConnectionMode** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。

## <a name="remarks"></a>備註

下表描述列舉值。



| 值  | 描述                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| 自動   | 只要網路在範圍內，就應該自動起始無線網路的連接。 |
| manual | 只有在使用者明確要求時，才會初始化無線網路的連接。               |



 

## <a name="examples"></a>範例

若要查看使用 **connectionMode** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




