---
title: SystemMonitor. ShowValueBar 屬性
description: 抓取或設定值，這個值會決定是否要在控制項上顯示值列 (圖形) 下方的統計值集。
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- ShowValueBar 屬性 SysMon
- ShowValueBar 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，ShowValueBar 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685688"
---
# <a name="systemmonitorshowvaluebar-property"></a>SystemMonitor. ShowValueBar 屬性

抓取或設定值，這個值會決定是否要在控制項上顯示值列 (圖形) 下方的統計值集。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>屬性值

True 表示顯示在控制項上的值列;否則為 false。 這個屬性的預設值是 True。

## <a name="remarks"></a>備註

顯示的統計資料包含最後一個值、平均值，以及目前選取的計數器在顯示的時間間隔內的最小值和最大值。 若要選取要顯示的計數器值，使用者必須在控制項的 [圖例] 窗格中選取計數器。

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

 

 





