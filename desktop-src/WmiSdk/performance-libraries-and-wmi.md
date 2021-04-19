---
description: WMIPerfClass 提供者和 WMIPerfInst 提供者會動態提供 WMI 效能計數器類別的效能計數器資料。
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: 效能程式庫和 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979032"
---
# <a name="performance-libraries-and-wmi"></a>效能程式庫和 WMI

[WMIPerfClass 提供者](wmiperfclass-provider.md)和[WMIPerfInst 提供者](wmiperfinst-provider.md)會動態提供 WMI[效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes)的效能計數器資料。

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>WMIPerfClass 和 WMIPerfInst 提供者

[WMIPerfClass 提供者](wmiperfclass-provider.md) 會在系統初始化時建立 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 。 [WMIPerfInst 提供者](wmiperfinst-provider.md)會動態提供這些類別的效能計數器資料。 WMIPerfClass 提供者提供者會提供第1版和第2版 [效能計數器](/windows/desktop/PerfCtrs/performance-counters-portal)的類別。

第1版計數器可在登錄的 **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services** 下找到。 提供效能資料的服務具有 **效能** 子機碼。 從第1版計數器建立的 WMI 效能類別沒有「計數器」作為其名稱的一部分。

在登錄中的 [ **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**] 下找到識別第2版效能計數器提供者的 **GUID**。

WMIPerfClass 會註冊為一般 WMI 類別提供者。 WMIPerfInst 是一種 WMI 執行個體提供者，可為第1版和第2版計數器的效能資料協助程式 (PDH) 提供資料。 如需詳細資訊，請參閱 [使用 PDH 函數來使用計數器資料](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> </dl>

 

 
