---
title: 來源 (registrationInfoType) 元素
description: 指定工作源自的位置。 例如，從元件、服務、應用程式或使用者。
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- 來源元素工作排程器
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384094"
---
# <a name="source-registrationinfotype-element"></a>來源 (registrationInfoType) 元素

指定工作源自的位置。 例如，從元件、服務、應用程式或使用者。

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

**Source** 元素是由 [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                           | 衍生自                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | 指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**RegistrationInfo 的 source**](registrationinfo-source.md) 屬性來指定工作的來源。

若是 c + + 開發，則會使用 [**IRegistrationInfo：： source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) 屬性來指定工作的來源。

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

 

 





