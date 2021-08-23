---
description: 識別 GSM 裝置的 SIM 識別碼。
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: SimIccID (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: 8a6e4a20d93396337e2af0f0533486618dc707760f1ccd5c4f20f399cbdbf203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777858"
---
# <a name="simiccid-mbnprofile-element"></a>SimIccID (MBNProfile) 元素

**SimIccID (MBNProfile)** 元素會識別適用于 GSM 裝置的 SIM 識別碼。

這個元素是選擇性的，且由行動寬頻服務設定供內部使用。 應用程式在建立或更新設定檔時，不應設定此欄位。

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

**SimIccID** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

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

 

 




