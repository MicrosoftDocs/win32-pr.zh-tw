---
description: 若要使用計數器資料，請參閱使用計數器資料。
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: 使用效能計數器
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 18bb017a34fb23188c20e81bce28c171c50dcb4d43cd52d458e92be99b7d03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033208"
---
# <a name="using-performance-counters"></a>使用效能計數器

效能計數器取用 **者** 是收集和利用效能計數器資料的軟體元件。 Microsoft 提供的範例取用者包括效能監視器 (perfmon.exe) 、資源監視器 (resmon.exe) 、記錄管理員 (logman.exe) 和 typeperf.exe。 協力廠商軟體元件也可以透過效能集合 Api 或 WMI 效能計數器類別收集效能資料。

效能計數器 **提供者** 是發佈效能計數器資料的軟體元件。 效能計數器可以由作業系統元件、設備磁碟機和服務提供。 許多效能計數器都是在 Windows 作業系統中提供。 協力廠商軟體元件可能會透過效能計數器提供者 Api 提供額外的計數器。

- 當您想要從系統收集或查看計數器資料時，請使用 [效能計數器工具](performance-counters-tools.md) 。
- 當您想要撰寫可從本機系統收集計數器資料的程式時，請使用 [效能計數器取用者 api](consuming-counter-data.md) 。
- 當您想要使用 WMI 從本機或遠端系統收集計數器資料時，請使用 [Wmi 效能計數器類別](/windows/desktop/WmiSdk/monitoring-performance-data) 。
- 當您想要從軟體元件發佈效能計數器資料時，請使用 [效能計數器提供者 api](providing-counter-data.md) 。

## <a name="see-also"></a>另請參閱

[關於效能計數器](about-performance-counters.md)

[效能計數器參考](performance-counters-reference.md)
