---
title: RegistrationInfo (taskType) 元素
description: 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- 註冊資訊工作排程器、XML 元素
- RegistrationInfo 元素工作排程器
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466020"
---
# <a name="registrationinfo-tasktype-element"></a>RegistrationInfo (taskType) 元素

指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

**RegistrationInfo** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                          | 衍生自                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | 定義工作排程器服務所執行的工作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                                                                  | 類型     | Description                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**編寫 (registrationInfoType)**](taskschedulerschema-author-registrationinfotype-element.md)                         | 字串   | 指定工作的作者。<br/>                                                                              |
| [**日期 (registrationInfoType)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | 指定註冊工作的日期和時間。<br/>                                                       |
| [**描述 (registrationInfoType)**](taskschedulerschema-description-registrationinfotype-element.md)               | 字串   | 指定工作的描述。<br/>                                                                         |
| [**檔 (registrationInfoType)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | 字串   | 指定工作的任何其他檔。<br/>                                                           |
| [**SecurityDescriptor (registrationInfoType)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | 字串   | 指定工作的安全描述項。<br/>                                                                 |
| [**來源 (registrationInfoType)**](taskschedulerschema-source-registrationinfotype-element.md)                         | 字串   | 指定工作源自的位置。 例如，從元件、服務、應用程式或使用者。<br/> |
| [**URI (registrationInfoType)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | 指定工作的 URI。<br/>                                                                                 |
| [**版本 (registrationInfoType)**](taskschedulerschema-version-registrationinfotype-element.md)                       | 字串   | 指定工作的版本號碼。<br/>                                                                      |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**TaskDefinition RegistrationInfo**](taskdefinition-registrationinfo.md) 屬性指定工作的註冊資訊。

針對 c + + 開發，會使用 [**ITaskDefinition 的 RegistrationInfo 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo)來指定工作的註冊資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





