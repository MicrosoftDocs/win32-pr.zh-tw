---
title: SystemMonitor BrowseCounters 方法
description: 顯示 [新增計數器] 對話方塊。
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- BrowseCounters 方法 SysMon
- BrowseCounters 方法 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon，BrowseCounters 方法
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024552"
---
# <a name="systemmonitorbrowsecounters-method"></a>SystemMonitor：： BrowseCounters 方法

顯示 [ **新增計數器** ] 對話方塊。

## <a name="syntax"></a>語法


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此對話方塊可讓使用者從效能物件清單中選取本機或遠端效能計數器。 選取的計數器會新增至 [**計數器**](counters.md) 集合，並顯示于圖形或報表中。

若要在加入計數器時接收通知，請執行 [**OnCounterAdded**](systemmonitor-oncounteradded.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**計數器。新增**](counters-add.md)
</dt> </dl>

 

 





