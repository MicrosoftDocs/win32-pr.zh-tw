---
title: 日期 (registrationInfoType) 元素
description: 指定註冊工作的日期和時間。
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- 日期元素工作排程器
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f191d6181e450deff8ffdb7bda0bf97cd0b27901fe454c25599d17b8edb30628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866638"
---
# <a name="date-registrationinfotype-element"></a>日期 (registrationInfoType) 元素

指定註冊工作的日期和時間。

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

**Date** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | 描述                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [ [**RegistrationInfo**](registrationinfo-date.md) ] 屬性來指定工作的註冊日期。

針對 c + + 開發，會使用 [**IRegistrationInfo：:D ate**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) 屬性來指定工作的註冊日期。

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

 

 





