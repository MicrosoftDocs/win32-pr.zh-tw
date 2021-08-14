---
title: TaskSettings. RunOnlyIfNetworkAvailable 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器只有在有可用的網路時才會執行工作。
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- RunOnlyIfNetworkAvailable 屬性工作排程器
- RunOnlyIfNetworkAvailable 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RunOnlyIfNetworkAvailable 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193d235276ffc37513c95b5ae0a4cef5a6e84cd0bc7d8bea7fab67a262110080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354845"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>TaskSettings. RunOnlyIfNetworkAvailable 屬性

針對腳本，取得或設定布林值，指出工作排程器只有在有可用的網路時才會執行工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則屬性會指出工作排程器只有在有可用的網路時才會執行工作。 預設值是 False。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





