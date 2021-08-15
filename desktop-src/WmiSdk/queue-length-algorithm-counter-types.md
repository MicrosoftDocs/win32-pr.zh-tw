---
description: 佇列長度演算法計數器會依適當的 frequency 屬性所指定的每個取樣間隔，遞增佇列中的專案數&\# 8212;Frequency \_ PerfTime 等等。
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: 佇列長度演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9fd3019e9a5e7150402266fd206d3f460f3d0ae3b07f4c6c7d51e82473e9dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316535"
---
# <a name="queue-length-algorithm-counter-types"></a>佇列長度演算法計數器類型

佇列長度的演算法計數器類型會依照適當的 frequency 屬性頻率 PerfTime 所指定的間隔，遞增佇列中的專案數 \_ ，依此類推。 處理後結果會除以樣本數，以產生平均佇列長度。

例如， [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)中使用性能 \_ 計數器 \_ 100ns \_ QUEUELEN \_ type 計數器類型的 >avgdiskqueuelength 屬性。



| CounterType 常數                                                                                                 | Description                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [效能 \_計數器 \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008<br/>            | 一段時間內的資源佇列平均長度。 它會顯示在最新的兩個樣本間隔期間，所觀察佇列長度之間的差異值，再除以間隔的持續時間。                       |
| [效能 \_計數器 \_ 大型 \_ QUEUELEN \_ 類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264<br/>     | 一段時間內的資源佇列平均長度。 這個型別的計數器會顯示在最新的兩個樣本間隔期間，所觀察佇列長度之間的差異值，再除以間隔的持續時間。 |
| [效能 \_計數器 \_ 100ns \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840<br/>     | 一段時間內的資源佇列平均長度，以100毫微秒單位表示。                                                                                                                                        |
| [效能 \_計數器 \_ OBJ \_ TIME \_ QUEUELEN \_ TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416<br/> | 物件在佇列中的時間。                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> </dl>

 

