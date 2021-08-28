---
title: 'DataType 複雜類型 (Windows 事件記錄) '
description: 定義資料項目。
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- DataType 複雜型別 EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fcbf217b16fb675a7a4eca00c8faa201737c07eea35a809f85617e96e9445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620278"
---
# <a name="datatype-complex-type"></a>DataType 複雜型別

定義資料項目。

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 名稱 | 字串 | 在範本中定義的資料項目名稱 (查看 [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) 複雜類型) 。<br/> |
| 類型 | QName  | 未使用。<br/>                                                                                                                                                     |



## <a name="remarks"></a>備註

資料項目可以是最上層資料項目或結構中的資料項目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 





