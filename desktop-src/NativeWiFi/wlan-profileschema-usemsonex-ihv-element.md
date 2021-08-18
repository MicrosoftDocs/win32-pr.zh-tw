---
description: 指定 IHV 安全性元件所使用之 802.1 X 安全性設定的來源。
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: useMSOneX (IHV) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4a62f2f25ef2a4a52fae82e2ce8ddb097a4b434d7c2f8f35a2783703a617ad8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912638"
---
# <a name="usemsonex-ihv-element"></a>useMSOneX (IHV) 元素

**UseMSOneX** (ihv) 元素會指定 IHV 安全性元件所使用的 802.1 x 安全性設定來源。

當 **useMSOneX** 為 true 時，IHV 安全性元件會使用 Microsoft 定義的 802.1 x 設定。 當 **useMSOneX** 為 false 時，IHV 安全性元件會使用廠商提供的 802.1 x 設定。

**Windows xp 搭配 SP3 和適用于 Windows XP SP2 的無線區域網路 API：** 不支援這個元素。

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) 元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




