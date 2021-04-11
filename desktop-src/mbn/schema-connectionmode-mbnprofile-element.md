---
description: 指定要用於行動寬頻裝置的自動連線設定。
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: ConnectionMode (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943405"
---
# <a name="connectionmode-mbnprofile-element"></a>ConnectionMode (MBNProfile) 元素

**ConnectionMode (MBNProfile)** 元素會指定要用於行動寬頻裝置的自動連線設定。

這個元素可以具有下列其中一個值。



| 值       | 意義                                                                |
|-------------|------------------------------------------------------------------------|
| 》    | 永遠不會自動連接到網路。                            |
| auto      | 一律自動連接到網路。                           |
| 「自動首頁」 | 會自動連接到網路，但在漫遊網路中的情況除外。 |



 

此元素最多可有一次。

此為必要項目。

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**ConnectionMode** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

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

 

 




