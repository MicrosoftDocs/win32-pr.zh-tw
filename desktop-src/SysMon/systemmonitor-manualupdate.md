---
title: SystemMonitor. ManualUpdate 屬性
description: 抓取或設定值，指出系統監視器的內容將會以手動方式更新，還是在指定的間隔自動更新。
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- ManualUpdate 屬性 SysMon
- ManualUpdate 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，ManualUpdate 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968964"
---
# <a name="systemmonitormanualupdate-property"></a>SystemMonitor. ManualUpdate 屬性

抓取或設定值，指出系統監視器的內容將會以手動方式更新，還是在指定的間隔自動更新。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a>屬性值

True 表示圖形會以手動方式更新。 False 表示會根據 [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md)中指定的更新間隔自動更新圖形。

## <a name="remarks"></a>備註

依預設，圖表會自動更新。

若要手動更新圖形，請呼叫 [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) 方法。

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

[**SystemMonitor.CollectSample**](systemmonitor-collectsample.md)
</dt> <dt>

[**SystemMonitor.UpdateGraph**](systemmonitor-updategraph.md)
</dt> </dl>

 

 





