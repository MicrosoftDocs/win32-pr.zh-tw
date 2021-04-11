---
title: 相互關聯 (SystemPropertiesType) 元素
description: 取用者可用來將相關事件群組在一起的活動識別碼。
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- 相互關聯元素 EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934825"
---
# <a name="correlation-systempropertiestype-element"></a>相互關聯 (SystemPropertiesType) 元素

取用者可用來將相關事件群組在一起的活動識別碼。

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

相互 **關聯** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) 複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱              | 類型                                                | Description                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | 識別目前活動的全域唯一識別碼。 以此識別碼發佈的事件是相同活動的一部分。<br/>                              |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | 全域唯一識別碼，用來識別要將控制項傳送至其中的活動。 相關事件接著會有此識別碼作為其 ActivityID 識別碼。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**系統 (的系統事件)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





