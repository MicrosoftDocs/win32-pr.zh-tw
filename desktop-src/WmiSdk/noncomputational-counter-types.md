---
description: Noncomputational 計數器類型沒有相關聯的公式。 原始值直接有意義。
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Noncomputational 計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a05da34058ceeb99ab60d8cc3d4f72cb3eec85194e48bb707a929eb2f68aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555158"
---
# <a name="noncomputational-counter-types"></a>Noncomputational 計數器類型

Noncomputational 計數器類型沒有相關聯的公式。 原始值直接有意義。

[**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)類別中的 **FilesToBeIndexed** 屬性是 **性能 \_ 計數器 \_ RAWCOUNT** 計數器類型的範例。 它包含尚未編制索引的檔案計數。

計數器類型是由 Winperf 中定義的常數（位於 Microsoft Windows 軟體開發套件 (SDK) ）所指定。 下表列出所提供的 noncomputational 計數器類型。



| CounterType                                                                                                 | 描述                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [效能 \_計數器 \_ TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816<br/>                | 此計數器類型會以 Unicode 顯示可變長度的文字字串。 它不會顯示計算的值。               |
| [效能 \_\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536 的計數器<br/>           | 不需要計算的原始計數器值，且代表只是最後觀察到之值的一個樣本。 |
| [效能 \_計數器 \_ 大型 \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | 與 **性能 \_ 計數器 \_ RAWCOUNT** 相同，但較大的值是64位表示。                                    |
| [效能 \_計數器 \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | 最近觀察到的十六進位格式值。 但不會顯示平均值                                     |
| [效能 \_計數器 \_ 大型 \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256<br/> | 與 **性能 \_ 計數器 \_ RAWCOUNT \_ HEX** 相同，但十六進位中的64位標記法與大型值搭配使用。        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> </dl>

 

