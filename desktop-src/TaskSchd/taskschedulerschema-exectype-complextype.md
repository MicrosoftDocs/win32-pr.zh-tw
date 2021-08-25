---
title: execType 複雜類型
description: 定義 Exec (actionGroup) 元素的子項目和排序資訊。
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- execType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e0726930f902ec0458f42fff9cdce39026cf63ddab92982bc30da33ca671712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796628"
---
# <a name="exectype-complex-type"></a>execType 複雜類型

定義 [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                           | 類型                                                        | 描述                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**引數**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | 指定與命令列操作相關聯的引數。 <br/>                              |
| [**命令**](taskschedulerschema-command-exectype-element.md)                   | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | 指定要執行的可執行檔或檔。<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | 指定可執行檔或可執行檔所使用的檔案所在的目錄。<br/> |



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

 

 





