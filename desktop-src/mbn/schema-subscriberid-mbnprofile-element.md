---
description: 識別設定檔的唯一識別碼。
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: SubscriberID (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511740"
---
# <a name="subscriberid-mbnprofile-element"></a>SubscriberID (MBNProfile) 元素

**SubscriberID (MBNProfile)** 元素會識別設定檔的唯一識別碼。

若為 GSM 網路，這應該包含 SIM 的 IMSI (國際行動使用者身分識別) ，而針對 CDMA 裝置，則應該包含裝置的最小 (行動電話識別碼) 。

元素是最大長度為15位數的數值字串。

需要元素。

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

**SubscriberID** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




