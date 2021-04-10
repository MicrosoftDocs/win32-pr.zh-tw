---
description: 下表列出
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: 效能計數器工具
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944244"
---
# <a name="performance-counters-tools"></a>效能計數器工具

## <a name="data-collection-tools"></a>資料收集工具

使用或操作 Windows 效能計數器資料時，下列工具很有用。

|工具|描述
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | 用來收集和查看效能計數器資料的 GUI 工具。 `perfmon.exe` 使用效能監視器嵌入式管理單元啟動 MMC，以提供效能監視器、資料收集器集合工具和報表工具的存取權。
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |用來收集和列印效能計數器資料的命令列工具。 可以用來列出可用的 countersets、列出可用的計數器、將計數器資料列印到主控台，或將計數器資料收集到記錄檔 (CSV、.TDF、.BLG) 。
| [重新記錄](/windows-server/administration/windows-commands/relog) |命令列工具，可用於轉換和合併記錄檔 (CSV、.TDF、.BLG) 透過 `typeperf.exe` 或透過 api 來捕捉 `PDH.dll` 。
| [LogMan](/windows-server/administration/windows-commands/logman) |用來控制資料收集器集合工具的命令列工具。

## <a name="data-provider-tools"></a>資料提供者工具

下列工具適用于發佈 Windows 效能計數器資料時。

|工具|描述
|----|-----------
| [CtrPP](ctrpp.md) | Windows SDK 中的命令列組建工具，可驗證及編譯您的效能計數器 V2 提供者資訊清單。 此工具會產生 `.h` `.rc` 建立 V2 提供者所需的標頭和資源腳本。
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | 命令列工具，用來將提供者安裝到系統上。
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | 命令列工具，用來從系統卸載您的提供者。
