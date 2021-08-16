---
description: 包含無線局域網路設定檔的名稱。
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: WLANProfile) 專案的名稱 (
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
ms.openlocfilehash: 6a6d19c043f7cc2e42ca8221e98b05e4afe7628b143bd572465f00e1d3652275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984111"
---
# <a name="name-wlanprofile-element"></a>WLANProfile) 專案的名稱 (

名稱 (WLANProfile) 元素包含無線局域網路設定檔的名稱。

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

**Name** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素所定義。

## <a name="remarks"></a>備註

名稱會區分大小寫。

針對 Windows xp service pack 3 (SP3) 以及 Windows XP service pack 2 (SP2) 的無線區域網路 API，當設定檔儲存在設定檔存放區時，會忽略 name 元素。 設定檔的名稱衍生自網路的 SSID。 在基礎結構網路設定檔中，設定檔的名稱是網路的 SSID。 針對臨機操作網路設定檔，設定檔的名稱是臨機操作網路的 SSID，後面接著 `-adhoc` 。 XML escape 字元（例如 &）不會顯示。 請避免使用適用于 Windows XP SP2 的 Windows XP （含 SP3）或無線區域網路 API 上所部署的設定檔的 SSID 名稱中的 XML escape 字元。

對於任何僅適用于 Windows Vista 或 Windows Server 2008 的網路設定檔，其名稱可以是任何字串。

## <a name="examples"></a>範例

若要查看使用 **name** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

 

 




