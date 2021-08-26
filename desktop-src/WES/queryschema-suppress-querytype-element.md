---
title: 隱藏 (QueryType) 元素
description: XPath 查詢，識別要從查詢結果集排除的事件。
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- 隱藏元素 EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032008"
---
# <a name="suppress-querytype-element"></a>隱藏 (QueryType) 元素

XPath 查詢，識別要從查詢結果集排除的事件。

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

**隱藏** 專案是由 [**QueryType**](queryschema-querytype-complextype.md)複雜型別定義。

## <a name="attributes"></a>屬性



| 名稱 | 類型   | 描述                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| 路徑 | anyURI | 通道的名稱或包含事件之記錄檔的路徑。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**查詢 (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





