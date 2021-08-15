---
title: 描述 (registrationInfoType) 元素
description: 指定工作的描述。
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Description 元素工作排程器
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6fef3012913eacfb8b8aa111793bd77255512d551bea0ab123d45b9caed6501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991388"
---
# <a name="description-registrationinfotype-element"></a>描述 (registrationInfoType) 元素

指定工作的描述。

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

**Description** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**RegistrationInfo 的 description**](registrationinfo-description.md) 屬性指定工作的描述。

針對 c + + 開發，會使用 [**IRegistrationInfo：:D 描述 e)**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) 屬性來指定工作的描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





