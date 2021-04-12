---
title: SecurityDescriptor (registrationInfoType) 元素
description: 指定工作的安全描述項。
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- SecurityDescriptor 元素工作排程器
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024768"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>SecurityDescriptor (registrationInfoType) 元素

指定工作的安全描述項。

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

**SecurityDescriptor** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**RegistrationInfo SecurityDescriptor**](registrationinfo-securitydescriptor.md) 屬性來指定工作的安全描述項。

若是 c + + 開發，則會使用 [**IRegistrationInfo：： SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) 屬性來指定工作的安全描述項。

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

 

 





