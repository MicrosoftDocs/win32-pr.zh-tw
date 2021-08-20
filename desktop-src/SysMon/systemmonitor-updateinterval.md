---
title: SystemMonitor. UpdateInterval 屬性
description: 抓取或設定 SYSMON 在下一次收集計數器資料並更新圖表或報表之前等候的時間長度。
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- UpdateInterval 屬性 SysMon
- UpdateInterval 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，UpdateInterval 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6c6f9d20a6a9b88d3764e013468747968a71690cf5e4a31603a88acd9e7e33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954523"
---
# <a name="systemmonitorupdateinterval-property"></a>SystemMonitor. UpdateInterval 屬性

抓取或設定 SYSMON 在下一次收集計數器資料並更新圖表或報表之前等候的時間長度。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>屬性值

SYSMON 時間長度（以秒為單位），這是在下一次收集計數器資料並更新圖表或報表之前等候的時間長度。 最小間隔為1秒 (這也是) 的預設值。 最大值為1000000。

## <a name="remarks"></a>備註

只有當 [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) 設定為 False 時，這個屬性才會相關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





