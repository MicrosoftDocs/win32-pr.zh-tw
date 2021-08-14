---
title: URI (registrationInfoType) 元素
description: 指定工作的 URI。
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- URI 元素工作排程器
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b9a2d9b8faf327f7b64be2cdd4273f2252405767004dc6e0d58b0c95b5f1910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355601"
---
# <a name="uri-registrationinfotype-element"></a>URI (registrationInfoType) 元素

指定工作的 URI。 這個元素是用來指定已註冊的工作放置於工作資料夾階層中的位置。

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

**URI** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，工作的 URI 是使用 [**RegistrationInfo**](registrationinfo-uri.md) 屬性來指定。

若是 c + + 開發，則會使用 [**IRegistrationInfo：： URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) 屬性來指定工作的 URI。

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

 

 





