---
title: TaskSettings 相容性屬性
description: 若為腳本，取得或設定整數值，這個值表示與工作相容的工作排程器版本。
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- 相容性屬性工作排程器
- 相容性屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，相容性屬性
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685736"
---
# <a name="tasksettingscompatibility-property"></a>TaskSettings 相容性屬性

若為腳本，取得或設定整數值，這個值表示與工作相容的工作排程器版本。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>屬性值



| 值                                                                                                                                                                                                                                         | 意義                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**工作 \_相容 \_ 性**</dt> <dt>0</dt> </dl> | 工作與 AT 命令相容。<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**工作 \_相容性 \_ V1**</dt> <dt>1</dt> </dl> | 工作與工作排程器1.0 相容。<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**工作 \_相容性 \_ V2**</dt> <dt>2</dt> </dl> | 工作與工作排程器2.0 相容。<br/> |



 

## <a name="remarks"></a>備註

只有在[](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) \_ \_ 需要從 Windows XP、Windows Server 2003 或 windows 2000 電腦存取或修改工作時，才應該將工作相容性（透過 [相容性] 屬性設定）設定為 [工作相容性 V1]。 否則，建議使用工作排程器2.0 相容性，因為工作將會有更多功能。

與 AT 命令相容的工作只能有一個時間觸發程式。

與工作排程器1.0 相容的工作只能有時間觸發程式、登入觸發程式或開機觸發程式，且工作只能有可執行檔動作。

如需工作相容性的詳細資訊，請參閱工作排程器[和工作](tasks.md)[的新功能](what-s-new-in-task-scheduler.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工作 \_ 相容性**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





