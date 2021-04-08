---
title: RepetitionPattern. StopAtDurationEnd 屬性
description: 針對腳本，取得或設定布林值，這個值會指出是否在重複模式期間結束時停止正在執行的工作實例。
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- StopAtDurationEnd 屬性工作排程器
- StopAtDurationEnd 屬性工作排程器，RepetitionPattern 物件
- RepetitionPattern 物件工作排程器、StopAtDurationEnd 屬性
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686142"
---
# <a name="repetitionpatternstopatdurationend-property"></a>RepetitionPattern. StopAtDurationEnd 屬性

針對腳本，取得或設定布林值，這個值會指出是否在重複模式期間結束時停止正在執行的工作實例。

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a>屬性值

布林值，指出是否在重複模式期間結束時停止正在執行的工作實例。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，這項資訊是在工作排程器架構的 [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





