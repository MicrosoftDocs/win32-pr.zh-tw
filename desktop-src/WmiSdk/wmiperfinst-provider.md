---
description: 從 Windows Vista 開始，WmiPerfInst 提供者會將原始和格式化的效能計數器資料動態提供給衍生自 Win32 效能的 WMI 效能計數器類別 \_ 。
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: WmiPerfInst 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a781fc1dc48f0e16d1c25e03eff1b2ab3c80fcd7058d1b49f95912b392d241
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049746"
---
# <a name="wmiperfinst-provider"></a>WmiPerfInst 提供者

從 Windows Vista 開始，WmiPerfInst 提供者會將原始和格式化的效能計數器資料動態提供給衍生自 [**Win32 效能 \_**](/windows/desktop/CIMWin32Prov/win32-perf)的 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)。 此提供者會取代[格式化的效能 Data Provider](formatted-performance-data-provider.md)（也稱為「處理後計數器提供者」）和[效能計數器提供者](performance-counter-provider.md)。

WmiPerfInst 提供者會提供資料給 [WMIPerfClass](wmiperfclass-provider.md) 提供者所提供的 WMI 類別。 此提供者是效能資料協助程式 (PDH) 實例與 WmiPerfClass 提供者所提供之 WMI 效能類別之間的橋樑。 當 WmiPerfInst 收到資料的查詢時，它會載入類別，並使用類別和屬性 [限定詞](qualifiers-specific-to-wmi-performance-classes.md) 來找出 PDH 實例。 如需詳細資訊，請參閱 [使用 PDH 函數來使用計數器資料](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)。

不建議您藉由建立 WMI 高效能提供者來開發新的效能物件，並相依于 [*ADAP 反向介面卡*](gloss-r.md) 程式以將資料傳輸至效能程式庫。 例外狀況是當您正在開發 Windows Driver Model 的驅動程式，而且想要提供效能資料時。 雖然反向介面卡程式會繼續運作以提供回溯相容性，但建議的方法是使用 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。

此提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例名稱為 "WmiPerfInst"。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 提供者](wmi-providers.md)
</dt> <dt>

[效能程式庫和 WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> </dl>

 

 
