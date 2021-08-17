---
title: logonType 簡單類型
description: 定義 LogonType 元素的可能值。
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- logonType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f40301957ec323b8abf7c09829bf3b551e2e1665a811409622d342784d86e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758890"
---
# <a name="logontype-simple-type"></a>logonType 簡單類型

定義 [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) 元素的可能值。

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>列舉值

**LogonType** 簡單類型會定義下列值。



| 值                      | 描述                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | 使用者必須使用服務登入使用者 (S4U) 登入。 使用 S4U 登入時，系統不會儲存任何密碼，也無法存取網路或加密的檔案。<br/>                                                                                                                                                          |
| 密碼                   | 使用者必須使用密碼登入。<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | 使用者必須已經登入。 此工作只會在現有的互動式會話中執行。<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | 不再使用;目前與密碼相同。<br/> **Windows 10、1511版、Windows 10、1507版、Windows 8.1、Windows Server 2012 R2、Windows 8、Windows Server 2012、Windows Vista 和 Windows Server 2008：** 工作將在現有的互動式會話中執行，或使用者必須使用密碼登入。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構簡單類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





