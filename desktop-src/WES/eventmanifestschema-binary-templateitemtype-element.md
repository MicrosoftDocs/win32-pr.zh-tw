---
title: 二元 (TemplateItemType) 元素
description: 包含事件記錄檔 API 所提供的二進位資料。
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- 二元元素 EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966143"
---
# <a name="binary-templateitemtype-element"></a>二元 (TemplateItemType) 元素

包含 [事件記錄](/windows/desktop/EventLog/event-logging) 檔 API 所提供的二進位資料。

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**二元** 元素是由 [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                          |
|------|--------|------------------------------------------------------|
| NAME | 字串 | 與二進位資料相關聯的名稱。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**範本 (TemplateListType)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

