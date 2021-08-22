---
title: 觸發程式物件
description: 提供所有觸發程式物件所繼承之通用屬性的腳本物件。
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- 觸發程式工作排程器，觸發程式物件
- 觸發程式物件工作排程器
- 觸發物件工作排程器，說明
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b27427bf77465be119fc678cb4babf85254fa437b350c54d4409c0cd5b28024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002006"
---
# <a name="trigger-object"></a>觸發程式物件

提供所有觸發程式物件所繼承之通用屬性的腳本物件。

## <a name="members"></a>成員

**觸發** 程式物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**觸發** 程式物件具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | 讀取/寫入<br/> | 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 取得或設定允許執行觸發程式之工作的最大時間量。<br/>                                         |
| [**Id**](trigger-id.md)<br/>                                 | 讀取/寫入<br/> | 取得或設定觸發程式的識別碼。<br/>                                                                                             |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 取得或設定啟動觸發程式的日期和時間。 觸發程式可以在啟動觸發程式之後啟動工作。<br/>             |
| [**類型**](trigger-type.md)<br/>                             |                       | 取得觸發程式的類型。<br/>                                                                                                            |



 

## <a name="remarks"></a>備註

工作排程器針對工作可使用的不同觸發程式提供下列個別物件：

-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)

讀取或寫入 XML 時，工作的觸發程式會在工作排程器架構的 [**trigger**](taskschedulerschema-triggers-tasktype-element.md) 元素中指定。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> </dl>

 

 





