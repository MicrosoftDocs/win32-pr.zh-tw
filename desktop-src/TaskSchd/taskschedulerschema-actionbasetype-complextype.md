---
title: actionBaseType 複雜類型
description: 定義此型別之所有元素的 Id 屬性。
ms.assetid: adc7117f-881f-4a32-8578-0530f2a0c179
keywords:
- actionBaseType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- actionBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a7620696f21054f67c7e654b50c6ce146e1c596a039e9eb74fc2bc72a994114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857971"
---
# <a name="actionbasetype-complex-type"></a>actionBaseType 複雜類型

定義此型別之所有元素的 Id 屬性。

``` syntax
<xs:complexType name="actionBaseType"
    abstract="true"
>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="attributes"></a>屬性



| 名稱 | 類型 | 描述                                        |
|------|------|----------------------------------------------------|
| id   | 識別碼   | 工作所執行之動作的識別碼。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





