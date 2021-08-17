---
title: 檔 (registrationInfoType) 元素
description: 指定工作的任何其他檔。
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- 檔元素工作排程器
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6cb8c2a78450fffa467ea659b55015f064310783ae21b067093de9473612fcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356866"
---
# <a name="documentation-registrationinfotype-element"></a>檔 (registrationInfoType) 元素

指定工作的任何其他檔。

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

**檔** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

若為腳本應用程式，則會使用 [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) 屬性來指定額外的工作檔。

若是 c + + 應用程式，則使用 [**IRegistrationInfo：:D 檔**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) 屬性來指定其他工作檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





