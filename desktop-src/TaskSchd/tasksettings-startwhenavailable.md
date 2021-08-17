---
title: TaskSettings. StartWhenAvailable 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器可以在經過排程的時間之後隨時啟動工作。
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- StartWhenAvailable 屬性工作排程器
- StartWhenAvailable 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、StartWhenAvailable 屬性
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ed43a04bba63d0e760866684df15c4cae5e80a1b3338d122408756f4cec46e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757921"
---
# <a name="tasksettingsstartwhenavailable-property"></a>TaskSettings. StartWhenAvailable 屬性

針對腳本，取得或設定布林值，指出工作排程器可以在經過排程的時間之後隨時啟動工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則屬性會指出工作排程器可以在經過排程的時間之後隨時啟動工作。 預設值是 False。

## <a name="remarks"></a>備註

這個屬性只適用于以時間為基礎的工作，其結束界限或以時間為基礎的工作設定為無限期地重複。

在排程的時間之後啟動的工作已通過 (，因為 [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) 屬性設定為 True) 會在工作的工作排程器服務佇列中排入佇列，而且會在延遲之後啟動。 預設延遲為10分鐘。

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) 元素中指定。

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

 

 





