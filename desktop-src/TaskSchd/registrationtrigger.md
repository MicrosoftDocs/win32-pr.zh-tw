---
title: RegistrationTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在工作註冊或更新時啟動工作。
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- 註冊觸發程式工作排程器，物件
- RegistrationTrigger 物件工作排程器
- RegistrationTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508776"
---
# <a name="registrationtrigger-object"></a>RegistrationTrigger 物件

代表觸發程式的腳本物件，此觸發程式會在工作註冊或更新時啟動工作。

## <a name="members"></a>成員

**RegistrationTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**RegistrationTrigger** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | Description                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](registrationtrigger-delay.md)<br/>               | 讀取/寫入<br/> | 取得或設定工作的註冊時間與工作啟動時間之間的時間量。<br/>                                                                                |
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定允許執行觸發程式之工作的最大時間量。<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                               |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定工作的執行頻率，以及啟動工作之後重複模式重複的時間長度。<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                              |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                              |



 

## <a name="remarks"></a>備註

當您為工作建立自己的 XML 時，會使用工作排程器架構的 [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) 元素來指定註冊觸發程式。

如果註冊了具有延遲註冊觸發程式的工作，且在延遲期間關閉或重新開機工作的電腦，在執行工作之前，工作將不會執行，而且會遺失延遲。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [ (腳本) 的註冊觸發程式範例 ](registration-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection 建立**](triggercollection-create.md)
</dt> </dl>

 

 





