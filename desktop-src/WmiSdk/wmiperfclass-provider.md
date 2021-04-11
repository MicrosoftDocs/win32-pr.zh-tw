---
description: 從 Windows Vista 開始，這個提供者會建立 WMI 效能計數器類別。
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: WmiPerfClass 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026850"
---
# <a name="wmiperfclass-provider"></a>WmiPerfClass 提供者

從 Windows Vista 開始，這個提供者會建立 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。 [WMIPerfInst](wmiperfinst-provider.md)提供者會動態提供這些 WMI 效能類別的資料。 自動探索/AutoPurge (ADAP) 進程不再將效能計數器物件傳輸至 WMI 儲存機制中的 WMI 效能類別。 如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。

如需詳細資訊，請參閱 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。

雖然不建議您藉由建立 WMI 高效能提供者來開發新的效能物件，並相依于 [*ADAP 反向介面卡*](gloss-r.md) 程式以將資料傳輸至效能程式庫，但例外狀況是提供效能資料的 Windows Driver Model 驅動程式的開發。 雖然反向介面卡程式會繼續運作以提供回溯相容性，但建議的方法是使用 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。

此提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "WmiPerfClass"。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 提供者](wmi-providers.md)
</dt> <dt>

[效能程式庫和 WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> </dl>

 

 
