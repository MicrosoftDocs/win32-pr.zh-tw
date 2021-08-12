---
title: 版本 (registrationInfoType) 元素
description: 指定工作的版本號碼。
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Version 元素工作排程器
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63d69b501b12890939f3bd0b146c959278eeaa0d5eb596851a488cef87f0770a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610423"
---
# <a name="version-registrationinfotype-element"></a>版本 (registrationInfoType) 元素

指定工作的版本號碼。

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

**Version** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | 描述                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**RegistrationInfo**](registrationinfo-version.md) 屬性來指定工作的版本。

針對 c + + 開發，使用 [**IRegistrationInfo：： version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) 屬性指定工作的版本。

## <a name="examples"></a>範例

下列 XML 會定義工作的版本。


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



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

 

 





