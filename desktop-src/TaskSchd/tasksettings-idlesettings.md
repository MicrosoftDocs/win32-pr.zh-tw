---
title: TaskSettings. IdleSettings 屬性
description: 針對腳本，取得或設定指定當電腦處於閒置狀態時，工作排程器如何執行工作的資訊。
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- IdleSettings 屬性工作排程器
- IdleSettings 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、IdleSettings 屬性
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965505"
---
# <a name="tasksettingsidlesettings-property"></a>TaskSettings. IdleSettings 屬性

針對腳本，取得或設定指定當電腦處於閒置狀態時，工作排程器如何執行工作的資訊。 如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>屬性值

[**IdleSettings**](idlesettings.md)物件，指定當電腦進入閒置狀態時，工作排程器如何處理工作。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) 元素中指定。

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

 

 





