---
title: principalType 複雜類型
description: 定義主體專案的屬性、子項目和排序資訊。
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- principalType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6b2d7e71642ab0294f6e930eef40c5841aa5832fcc3a8d1c45aef2d7e80bbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611910"
---
# <a name="principaltype-complex-type"></a>principalType 複雜類型

定義 [**主體**](taskschedulerschema-principal-principaltype-element.md) 專案的屬性、子項目和排序資訊。

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                             | 類型                                                                                     | 描述                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md)                        | 字串                                                                                   | 指定工作排程器使用者介面中顯示的主體名稱 (UI) 。<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)                                | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | 指定執行與主體相關聯之工作所需之使用者群組的識別碼。<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | 指定執行與主體相關聯之工作所需的安全性登入方法。<br/>        |
| [**ProcessTokenSidType**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processTokenSidType**](taskschedulerschema-processtokensidtype-simpletype.md)        | 指定工作可使用 (SID) 的進程安全識別碼類型。<br/>                              |
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | 指定執行工作所需的許可權。<br/>                                                               |
| [**RunLevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md)                      | 指定將在其上執行工作的許可權層級。<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)                                  | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | 指定執行與主體相關聯之工作所需的使用者識別碼。<br/>              |



## <a name="attributes"></a>屬性



| 名稱 | 類型 | 描述                                           |
|------|------|-------------------------------------------------------|
| id   | 識別碼   | 指定主體的識別碼。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





