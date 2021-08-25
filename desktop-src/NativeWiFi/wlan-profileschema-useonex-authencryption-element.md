---
description: 指出是否使用 802.1 X 驗證。
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: useOneX (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 961f1b6be52da97ada2c230579ac281652a07fcbae67ac32d2399eb2968b1946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912568"
---
# <a name="useonex-authencryption-element"></a>useOneX (authEncryption) 元素

UseOneX (authEncryption) 元素指出是否使用 802.1 X 驗證。

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。

## <a name="examples"></a>範例

若要查看使用 **useOneX** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**authEncryption (安全性)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




