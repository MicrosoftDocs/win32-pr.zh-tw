---
title: LogonTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在使用者登入時啟動工作。
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- 登入觸發程式工作排程器，物件
- LogonTrigger 物件工作排程器
- LogonTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aed10ba9c0c792a5e4f882988ca07770c4ac568cb893b8ffac16a3a24efd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760095"
---
# <a name="logontrigger-object"></a>LogonTrigger 物件

代表觸發程式的腳本物件，此觸發程式會在使用者登入時啟動工作。 當工作排程器服務啟動時，系統會列舉所有登入的使用者，並執行與登入的使用者相符之登入觸發程式所註冊的任何工作。

## <a name="members"></a>成員

**LogonTrigger** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**LogonTrigger** 物件具有這些屬性。



| 屬性                                                            | 存取類型           | 描述                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**延遲**](logontrigger-delay.md)<br/>                      | 讀取/寫入<br/> | 取得或設定值，這個值表示使用者登入和工作啟動時間之間的時間量。<br/>                                                                              |
| [**啟用**](trigger-enabled.md)<br/>                       | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定布林值，這個值會指出是否已啟用觸發程式。<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定停用觸發程式的日期和時間。 觸發程式在停用之後無法啟動工作。<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定允許執行觸發程式之工作的最大時間量。<br/>                                         |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定觸發程式的識別碼。<br/>                                                                                             |
| [**重複**](trigger-repetition.md)<br/>                 | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | 讀取/寫入<br/> | 繼承自 [**觸發**](trigger.md) 程式物件。 取得或設定啟動觸發程式的日期和時間。<br/>                                                                            |
| [**類型**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | 唯讀<br/>  | 繼承自 [**觸發**](trigger.md) 程式物件。 取得觸發程式的類型。<br/>                                                                                                            |
| [**UserId**](logontrigger-userid.md)<br/>                    | 讀取/寫入<br/> | 取得或設定使用者的識別碼。<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>備註

如果您想要在群組的任何成員登入電腦而非特定使用者登入時觸發工作，則不要將值指派給 [**LogonTrigger。 UserId**](logontrigger-userid.md) 屬性。 相反地，請使用 **LogonTrigger 的 UserId** 屬性建立登入觸發程式，並使用 [**principal**](principal-groupid.md) 屬性將值指派給工作的主體。

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) 元素來指定登入觸發程式。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [登入觸發程式範例 (腳本) ](logon-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**觸發程序**](trigger.md)
</dt> </dl>

 

 





