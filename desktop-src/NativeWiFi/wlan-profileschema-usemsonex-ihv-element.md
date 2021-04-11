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
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944470"
---
# <a name="usemsonex-ihv-element"></a>useMSOneX (IHV) 元素

**UseMSOneX** (ihv) 元素會指定 IHV 安全性元件所使用的 802.1 x 安全性設定來源。

當 **useMSOneX** 為 true 時，IHV 安全性元件會使用 Microsoft 定義的 802.1 x 設定。 當 **useMSOneX** 為 false 時，IHV 安全性元件會使用廠商提供的 802.1 x 設定。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



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

 

 




