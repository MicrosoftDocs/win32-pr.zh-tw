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
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934669"
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



| 元素                                                                                           | 類型     | Description                                                                                                        |
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構複雜類型](task-scheduler-schema-complex-types.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





