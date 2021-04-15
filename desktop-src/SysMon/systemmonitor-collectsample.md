---
title: SystemMonitor CollectSample 方法
description: 針對計數器物件中的每個計數器取樣一個值。
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- CollectSample 方法 SysMon
- CollectSample 方法 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon，CollectSample 方法
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465561"
---
# <a name="systemmonitorcollectsample-method"></a>SystemMonitor：： CollectSample 方法

針對 [**計數器**](counters.md) 物件中的每個計數器取樣一個值。

## <a name="syntax"></a>語法


```VB
Sub CollectSample()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

只有當 [**ManualUpdate**](systemmonitor-manualupdate.md)為 True，且您要從電腦目前的活動取樣計數器值時，才會呼叫 **CollectSample** ，而不會在從記錄檔取樣時使用這個方法。 圖形或報表會以新的值更新。 請注意，某些圖形類型需要兩個範例，才能繪製資料（例如折線圖）。

若要在收集樣本時接收通知，請執行 [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**計數器**](counters.md)
</dt> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





