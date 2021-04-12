---
title: 選取 (QueryType) 元素
description: XPath 查詢，識別要包含在查詢結果集中的事件。
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Select 元素 EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385146"
---
# <a name="select-querytype-element"></a>選取 (QueryType) 元素

XPath 查詢，識別要包含在查詢結果集中的事件。

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

**Select** 元素是由 [**QueryType**](queryschema-querytype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱 | 類型   | Description                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| 路徑 | anyURI | 通道的名稱或包含事件之記錄檔的路徑。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**查詢 (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





