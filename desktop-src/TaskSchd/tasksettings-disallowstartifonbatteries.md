---
title: TaskSettings. DisallowStartIfOnBatteries 屬性
description: 針對腳本，取得或設定布林值，指出如果電腦是以電池執行，將不會啟動工作。
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- DisallowStartIfOnBatteries 屬性工作排程器
- DisallowStartIfOnBatteries 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、DisallowStartIfOnBatteries 屬性
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105347"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>TaskSettings. DisallowStartIfOnBatteries 屬性

針對腳本，取得或設定布林值，指出如果電腦是以電池執行，將不會啟動工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>屬性值

指出當電腦以電池執行時，不會啟動工作的布林值。 若為 True，則在電腦以電池執行時，不會啟動工作。 如果為 False，則工作會在電腦以電池執行時啟動。 預設值為 True。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) 元素中指定。

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

 

 





