---
description: WMI 高效能格式化的效能 Data Provider 會計算指定之原始計數器資料樣本數目的統計計數器類型。
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: 統計計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027075"
---
# <a name="statistical-counter-types"></a>統計計數器類型

WMI 高效能格式化的 [效能 Data Provider](formatted-performance-data-provider.md) 會計算指定之原始計數器資料樣本數目的統計計數器類型。 計數器類型的演算法不需要繼承 timestamp 或 frequency 屬性 (例如 **timestamp \_ PerfTime** 或其他計數器類型所需的 **frequency \_ PerfTime**) 。

相反地，統計計數器類型支援識別要使用之樣本數的辨識 **符號** 。 針對效能物件呼叫 [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) 方法時，會收集範例。 針對腳本，請使用 [**SWbemRefresher**](swbemrefresher-refresh.md) 方法。 計算的資料包含從原始資料屬性對樣本 **SampleWindow** 數目執行的計算結果。 計算的原始資料會 keyfromnode.frm 在 **計數器** 辨識符號中指定的屬性名稱。

如需詳細資訊，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md) 和 [存取 WMI 預先安裝的效能類別](accessing-wmi-preinstalled-performance-classes.md)。



| CounterType 常數                    | Description                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COOKER \_ 平均](cooker-average.md)   | 加總 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別中某個屬性的重複觀察，並將總和除以觀察數目。                              |
| [COOKER \_ MAX](cooker-max.md)           | [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中某一組屬性觀察值的最大值。                                                                    |
| [COOKER \_ 分鐘](cooker-min.md)           | [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中，屬性的一組觀察值的最小值。                                                                   |
| [COOKER \_ 範圍](cooker-range.md)       | [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中，屬性的一組原始觀察值的 [最小](cooker-min.md)值與 [最大](cooker-max.md)值之間的差異。 |
| [COOKER \_ 變異數](cooker-variance.md) | 變異數的量值，可以用來表示在 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別中，屬性的一組原始觀察值的散佈。            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> <dt>

[更新腳本中的 WMI 資料](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[存取腳本中的效能資料](accessing-performance-data-in-script.md)
</dt> <dt>

[存取 c + + 中的效能資料](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
