---
title: Trigger。重複屬性
description: 針對腳本，取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- 重複屬性工作排程器
- 重複屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，重複屬性
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969767"
---
# <a name="triggerrepetition-property"></a>Trigger。重複屬性

針對腳本，取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。

## <a name="syntax"></a>Syntax


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a>屬性值

[**RepetitionPattern**](repetitionpattern.md)物件，定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會在工作排程器架構的 [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) 元素中指定觸發程式的重複模式。

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
</dt> <dt>

[**RepetitionPattern**](repetitionpattern.md)
</dt> </dl>

 

 





