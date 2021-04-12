---
title: RepetitionPattern 物件
description: 腳本物件，定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- 觸發程式工作排程器，重複模式物件
- 重複模式工作排程器，物件
- RepetitionPattern 物件工作排程器
- RepetitionPattern 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464813"
---
# <a name="repetitionpattern-object"></a>RepetitionPattern 物件

腳本物件，定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。

## <a name="members"></a>成員

**RepetitionPattern** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**RepetitionPattern** 物件具有這些屬性。



| 屬性                                                                    | 存取類型           | Description                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**持續時間**](repetitionpattern-duration.md)<br/>                   | 讀取/寫入<br/> | 取得或設定重複模式的時間長度。<br/>                                                                                          |
| [**間隔**](repetitionpattern-interval.md)<br/>                   | 讀取/寫入<br/> | 取得或設定每次重新開機工作之間的時間量。<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | 讀取/寫入<br/> | 取得或設定布林值，這個值表示是否在重複模式期間結束時停止正在執行的工作實例。<br/> |



 

## <a name="remarks"></a>備註

如果您指定工作的重複持續時間，您也必須指定重複間隔。

如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動五次。 您可以使用下列模式來定義五次重複。

1.  工作會在第一分鐘的開頭開始。
2.  下一項工作會在第一分鐘結束時啟動。
3.  下一項工作會在第二分鐘結束時啟動。
4.  下一項工作會從第三分鐘的結尾開始。
5.  下一項工作會在第四分鐘結束時啟動。

**Windows Server 2003、WINDOWS XP 和 windows 2000：** 如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動四次。

讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) 專案來指定重複模式。

## <a name="examples"></a>範例

如需此屬性的詳細資訊和範例程式碼，請參閱 [ (腳本) 的每日觸發程式範例 ](daily-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





