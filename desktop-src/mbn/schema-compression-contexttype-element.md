---
description: 指定壓縮是否會用於標頭和資料傳輸的資料連結。
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: 壓縮 (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848113"
---
# <a name="compression-contexttype-element"></a>壓縮 (coNtextType) 元素

**壓縮 (coNtextType)** 元素會指定壓縮是否會用於標頭和資料傳輸的資料連結。

這個元素可以是下列其中一個值。

| 值     | 意義                       |
|-----------|-------------------------------|
| 禁用  | 將會使用壓縮。     |
| 停用 | 將不會使用壓縮。 |



 

這是選擇性的項目。 如果未指定此元素，行動寬頻系統將不會使用壓縮。

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**壓縮** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**coNtextType**](schema-contexttype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile) 內容 (**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




