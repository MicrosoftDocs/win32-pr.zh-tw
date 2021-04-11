---
description: 效能計數器類型會指定取得計算的效能計數器所需的公式。 這些是 Windows 效能監視所使用的相同計數器類型。
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: WMI 效能計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115032"
---
# <a name="wmi-performance-counter-types"></a>WMI 效能計數器類型

性能 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) 會指定取得計算的效能計數器所需的公式。 這些是 Windows [效能監視](/windows/desktop/PerfCtrs/performance-counters-portal)所使用的相同計數器類型。 在 WMI 效能類別中，計數器類型公式的原始資料來自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別，而且計算結果是在對應 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 類別的相同名稱屬性中找到。

計數器類型會顯示為 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中屬性的 **CounterType** 限定詞，以及 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別中屬性的 **CookingType** 限定詞。

例如， [**win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)類別中的 **AvgDiskBytesPerRead** 屬性是 class [**Win32 \_ AvgDiskBytesPerRead \_ PerfFormattedData \_ PerfDisk**](./retrieving-raw-and-formatted-performance-data.md)中 **LogicalDisk** 屬性的原始資料來源，其中包含與系統監視器中所顯示相同的資料。

下列清單依功能類型組織計數器類型描述：

-   [基底計數器類型](base-counter-types.md)
-   [基本演算法計數器類型](basic-algorithm-counter-types.md)
-   [計數器演算法計數器類型](counter-algorithm-counter-types.md)
-   [Noncomputational 計數器類型](noncomputational-counter-types.md)
-   [精確度計時器演算法計數器類型](precision-timer-algorithm-counter-types.md)
-   [佇列長度演算法計數器類型](queue-length-algorithm-counter-types.md)
-   [統計計數器類型](statistical-counter-types.md)
-   [計時器演算法計數器類型](timer-algorithm-counter-types.md)

 

 
