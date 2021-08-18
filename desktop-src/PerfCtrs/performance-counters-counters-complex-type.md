---
description: 定義檢測資訊清單的區段，以識別提供者以及它們所提供的計數器。
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: 計數器複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14630fa4e0e9461e59d377b4defc3edacee8dca9560d1f7eb42acb317ffd1f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143961"
---
# <a name="counters-complex-type"></a>計數器複雜類型

定義檢測資訊清單的區段，以識別提供者以及它們所提供的計數器。

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素      | 類型                                                               | 描述                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| **供應商** | [**男人：提供者**](performance-counters-provider-complex-type.md) | 識別提供計數器的提供者。<br/> |



## <a name="attributes"></a>屬性



| 名稱          | 類型 | 描述                                                      |
|---------------|------|------------------------------------------------------------------|
| schemaVersion |      | 用來寫入資訊清單的架構版本。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儀錶**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

