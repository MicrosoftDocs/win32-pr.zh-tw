---
description: 某些公式需要計數器屬性和基底屬性。
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: 基底計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194350"
---
# <a name="base-counter-types"></a>基底計數器類型

某些公式需要計數器屬性和基底屬性。 基底值是計數器類型公式中的分母。 在衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)的原始資料 [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)中，基底屬性必須緊接在計數器屬性之後。 基底屬性和先前的計數器必須有相同的名稱，並附加 **\_ 基底**。

例如， [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)中的 **AvgDiskBytesPerRead** 屬性包含在讀取作業期間從磁片傳輸的原始值（以位元組為單位）。 它有基底屬性 **AvgDiskBytesPerRead \_ 基底**，其代表累積的作業數目。 當 WMI 套用指定之計數器類型的公式時， **效能 \_ 平均 \_ 基底** **AvgDiskBytesPerRead** 會除以 **AvgDiskBytesPerRead \_ 基底** ，以產生平均值。 此值會出現在 [系統監視器] 中，並儲存在對應的 [ [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) ] 屬性中。 基底屬性只會用於原始資料類別。

在衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別中， **計數器** 限定詞會指定原始類別中的分子屬性，而 **基底** 限定詞會指定基底分母屬性。

下表列出 **CounterType** 常數值。



| CounterType 常數                                                                                      | Description                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [效能 \_平均 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939458<br/>        | 用來計算效能 **\_ 平均 \_ 計時器** 和效能 **\_ 平均 \_ 大量** 計數器類型的基底值。                                                                                             |
| [效能 \_計數器 \_ 多重 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1107494144<br/> | 用來計算 **性能 \_ 計數器 \_ 多重 \_ 計時器** 的基底值、 **性能 \_ 計數器 \_ 多個計時器的 \_ \_ 庫存**、效能 **\_ 100NSEC \_ 多重 \_ 計時器**，以及效能 **\_ 100NSEC \_ 多重 \_ 計時器 \_** 的類型計數器類型。 |
| [效能 \_大型 \_ 原始 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939712<br/>     | 在計算效能 **\_ 原始 \_ 分數** 64 位時，所找到的基底值。                                                                                                                         |
| [效能 \_原始 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939459<br/>            | 用來計算 **性能 \_ 原始 \_ 分數** 計數器類型的基底值。                                                                                                                           |
| [效能 \_範例 \_ 基底](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位1073939457<br/>         | 用來計算效能 **\_ 範例 \_ 計數器** 和效能 **\_ 樣本 \_ 分數** 計數器類型的基底值。                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> <dt>

[計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 

