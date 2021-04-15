---
title: TaskSettings. AllowDemandStart 屬性
description: 針對腳本，取得或設定布林值，這個值表示可以使用 [執行] 命令或內容功能表來啟動工作。
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- AllowDemandStart 屬性工作排程器
- AllowDemandStart 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、AllowDemandStart 屬性
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384090"
---
# <a name="tasksettingsallowdemandstart-property"></a>TaskSettings. AllowDemandStart 屬性

針對腳本，取得或設定布林值，這個值表示可以使用 [執行] 命令或內容功能表來啟動工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則可以使用 [執行] 命令或內容功能表來執行工作。 如果為 False，則無法使用 [執行] 命令或內容功能表來執行工作。 預設值為 True。

## <a name="remarks"></a>備註

當這個屬性設定為 True 時，可以在任何觸發程式啟動工作時獨立啟動工作。

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) 元素中指定。

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

 

 





