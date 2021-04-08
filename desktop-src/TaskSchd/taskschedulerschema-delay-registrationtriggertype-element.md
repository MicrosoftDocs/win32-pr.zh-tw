---
title: 延遲 (registrationTriggerType) 元素
description: 指定在註冊工作與啟動工作之間的時間長度。
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
keywords:
- Delay 元素工作排程器
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686567"
---
# <a name="delay-registrationtriggertype-element"></a>延遲 (registrationTriggerType) 元素

指定在註冊工作與啟動工作之間的時間長度。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 如需持續時間類型的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=106886> 。

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

**Delay** 元素是由 [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                     | 衍生自                                                                               | Description                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | 指定在註冊工作時啟動工作的觸發程式。<br/> |



## <a name="remarks"></a>備註

針對開發腳本，會使用 [**RegistrationTrigger 的 delay**](registrationtrigger-delay.md) 屬性指定註冊觸發程式延遲。

針對 c + + 開發，會使用 [**IRegistrationTrigger：:D elay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) 屬性指定註冊觸發程式延遲。

## <a name="examples"></a>範例

下列 XML 定義的註冊觸發程式延遲，可在工作註冊的時間與工作啟動的時間之間有5分鐘的延遲。


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



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

 

 





