---
description: 包含設定檔建立者的相關資訊。
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: ProfileCreationType (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113453"
---
# <a name="profilecreationtype-mbnprofile-element"></a>ProfileCreationType (MBNProfile) 元素

**ProfileCreationType (MBNProfile)** 元素包含設定檔建立者的相關資訊。

這個元素可以具有下列其中一個值。



| 值                 | 意義                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | 此設定檔是由裝置使用者提供的資訊所建立。                                                     |
| "AdminProvisioned"    | 此設定檔是由 IT 系統管理員所建立，並散發給使用者。                                                     |
| "OperatorProvisioned" | 此設定檔是由網路操作員建立並散發給使用者。                                                    |
| "DeviceProvisioned"   | 此設定檔是由行動寬頻服務使用儲存在裝置布建內容中的資訊所建立。 |



 

這是選擇性項目。

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**ProfileCreationType** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

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

 

 




