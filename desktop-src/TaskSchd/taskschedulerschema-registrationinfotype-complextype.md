---
title: registrationInfoType 複雜類型
description: 定義 RegistrationInfo 元素的子項目和排序資訊。
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- registrationInfoType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 704fcb3205f032654ef6a666dd119dec34f88992018f16b1715ba4982847149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131658"
---
# <a name="registrationinfotype-complex-type"></a>registrationInfoType 複雜類型

定義 [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) 元素的子項目和排序資訊。

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>子元素



| 元素                                                                                           | 類型     | 描述                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**作者**](taskschedulerschema-author-registrationinfotype-element.md)                         | 字串   | 指定工作的作者。<br/>                                                                       |
| [**日期**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | 指定註冊工作的日期和時間。<br/>                                                |
| [**描述**](taskschedulerschema-description-registrationinfotype-element.md)               | 字串   | 指定工作的描述。<br/>                                                                  |
| [**文件**](taskschedulerschema-documentation-registrationinfotype-element.md)           | 字串   | 指定工作的任何其他檔。<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | 字串   | 指定工作的安全描述項。<br/>                                                          |
| [**源**](taskschedulerschema-source-registrationinfotype-element.md)                         | 字串   | 指定工作源自的位置。 例如，從元件、服務、應用程式或使用者。<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | 指定工作的 URI。<br/>                                                                          |
| [**版本**](taskschedulerschema-version-registrationinfotype-element.md)                       | 字串   | 指定工作的版本號碼。<br/>                                                               |



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

 

 





