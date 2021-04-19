---
title: SystemMonitor. EnableToolTips 屬性
description: 取得或設定值，這個值會決定當滑鼠停留在其中一個圖形視圖中的計數器上方時是否顯示工具提示 (不支援報表檢視) 。
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- EnableToolTips 屬性 SysMon
- EnableToolTips 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，EnableToolTips 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967738"
---
# <a name="systemmonitorenabletooltips-property"></a>SystemMonitor. EnableToolTips 屬性

取得或設定值，這個值會決定當滑鼠停留在其中一個圖形視圖中的計數器上方時是否顯示工具提示 (不支援報表檢視) 。

## <a name="syntax"></a>Syntax


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a>屬性值

True 會顯示工具提示，其中包含其中的計數器資訊;否則為 False。

## <a name="remarks"></a>備註

針對折線圖，工具提示會錨定到最接近滑鼠的資料點。 針對橫條圖和長條圖，工具提示表示橫條圖的總數據值，而不是橫條圖內的點。

工具提示包含以資料來源為基礎的不同資訊。 針對記錄檔，工具提示包含計數器路徑、計數器值、時間戳記、資料點中包含的資料樣本數目，以及最小和最大資料值。

針對即時活動，工具提示包含計數器路徑、計數器值和時間戳記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





