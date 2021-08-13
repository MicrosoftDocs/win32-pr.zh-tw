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
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587401"
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



| 名稱 | 類型   | 描述                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| 路徑 | anyURI | 通道的名稱或包含事件之記錄檔的路徑。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**查詢 (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





