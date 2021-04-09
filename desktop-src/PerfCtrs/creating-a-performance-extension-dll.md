---
description: 提供者是提供計數器資料給取用者的效能 DLL。
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: 建立效能延伸模組 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d397f1581454aca1b25c447b35f250eefd215f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849294"
---
# <a name="creating-a-performance-extension-dll"></a>建立效能延伸模組 DLL

> [!IMPORTANT]
> 由於有顯著的效能和可靠性限制，提供本主題所描述的效能計數器資料的方法，可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用使用 [2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md) 來建立新的效能計數器，以及遷移現有的效能計數器來使用該方法所述的方法。

[V1 提供者](providing-counter-data.md)會使用提供計數器資料給取用者的效能 DLL。 效能 DLL 必須匯出 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))、 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)和 [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) 函數。 一般來說，您會使用模組定義 ( .def) 檔案，從 DLL 匯出函式。 當取用者查詢效能資料時，系統會呼叫這些函數。

當取用者第一次呼叫 [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)，或取用者使用 [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya)或 [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya)函式來開啟時 `HKEY_PERFORMANCE_DATA` ，系統會針對電腦上 [註冊](adding-performance-counters.md)的每個提供者呼叫 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))函數。 如果提供者在的區段中指定了支援的物件清單，就會發生例外狀況 `[objects]` 。INI 檔案。 在此情況下，只有在其中一個查詢的物件符合清單中的物件時，系統才會呼叫提供者。

[**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85))函數可讓每個提供者有機會初始化其效能資料結構。 然後，如果 **OpenPerformanceData** 函數傳回成功，系統就會呼叫提供者的 [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) 函式。 後續呼叫 [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) 會導致系統呼叫 **CollectPerformanceData** 函式。

當取用者完成收集效能資料時，它會指定 `HKEY_PERFORMANCE_DATA` [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) 函數的呼叫。 這會導致系統為每個提供者呼叫 [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) 函數。 然後，提供者就會卸載。

多個取用者可能會同時收集效能資料。 系統只會在每次載入或卸載 DLL 時，呼叫 [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) 和 [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) 函數一次。

> [!Note]
> 請務必在 c + + 程式碼中包含 extern "C"，以防止編譯器將裝飾新增至函式名稱;否則，系統可能會找不到您的函式。

> [!Note]
> 如果載入您的效能 DLL、尋找您的函式或呼叫您的函式時發生錯誤，系統會在相同的進程中停用後續集合的提供者。 此外，如果在具有特殊許可權的進程中執行時，系統會將停用的 **效能計數器** 值新增至您的 **效能** 金鑰，以防止未來載入提供者。

如需撰寫效能 DLL 的詳細資訊，請參閱下列主題：

- [執行 OpenPerformanceData 函數](implementing-openperformancedata.md)
- [執行 CollectPerformanceData 函數](implementing-collectperformancedata.md)
- [DLL 中的錯誤處理](error-handling-in-the-dll.md)
- [限制對效能延伸模組 Dll 的存取](restricting-access-to-performance-extension--dlls.md)
- [效能 DLL 範例](performance-dll-samples.md)
