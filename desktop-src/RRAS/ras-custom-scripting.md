---
title: RAS 自訂腳本
description: 開發人員可以建立位於 RAS 用戶端電腦上的自訂腳本 DLL。 此 DLL 可在建立連接的過程中與伺服器進行通訊。
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ac0bd83b8d7c48ee8b0468d89a70d19a5e5e6555b9a8bc8ac86d66c8cd666e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673278"
---
# <a name="ras-custom-scripting"></a>RAS 自訂腳本

開發人員可以建立位於 RAS 用戶端電腦上的自訂腳本 DLL。 此 DLL 可在建立連接的過程中與伺服器進行通訊。

**Windows NT：** 無法使用自訂腳本。

## <a name="setting-up-the-dll"></a>設定 DLL

若要設定 DLL，請在下列登錄機碼底下建立名稱 **CustomScriptDllPath** 的值：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

此值的類型應為 **REG \_ EXPAND \_ SZ**。 此值應該包含自訂腳本 DLL 的路徑。 每部 RAS 用戶端電腦都只支援一個自訂腳本 DLL。

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a>伺服器、RAS 和 Custom-Scripting DLL 之間的互動

自訂腳本 DLL 應匯出單一進入點： [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)。 RAS 會在連接程式的 RASCS 互動狀態期間呼叫此函式 \_ 。 RASCS \_ 互動狀態為暫停狀態，可讓使用者與自訂腳本 DLL 所顯示的使用者介面互動。 如需連接狀態的詳細資訊，請參閱 [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) 。

RAS 會以參數形式傳遞至 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) 函式：

-   用戶端電腦上用於連接之埠的控制碼。
-   識別連接之電話簿和專案的字串。
-   RAS 也會將控制碼傳遞至視窗，讓 DLL 能呈現使用者介面。
-   DLL 可以用來與伺服器通訊的一組函式指標。

如需這些參數的詳細資訊，請參閱 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) 。

RAS 會將 [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) 結構的指標傳遞至 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)的最後一個參數。 此結構包含 [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings)型別函式的指標。 自訂腳本 DLL 會呼叫這個函式，以修改連接所使用之通訊埠上的通訊設定。

RAS 會協調伺服器與自訂腳本 DLL 之間的互動。 一般來說，伺服器會起始對話。 例如，伺服器可能會要求使用者的使用者名稱和密碼。

使用自訂腳本建立連接時，伺服器不需要執行 Windows NT 4.0 或 Windows 2000。

## <a name="custom-scripting-user-interface-must-support-idcancel"></a>自訂腳本消費者介面必須支援 IDCANCEL

如果自訂撥號程式顯示使用者介面，則使用者介面必須支援 \_ LOWORD (*WParam*) 等於 IDCANCEL 的 WM 命令訊息。

## <a name="configuring-the-connection"></a>設定連接

[**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)進入點可以從 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)或從 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)的 Windows XP 上叫用。

若要從 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)叫用 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) ，請 \_ 在連接的電話簿專案中，設定 RASEO CustomScript 選項。 如需電話簿輸入選項的說明，請參閱 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))的 **dwfOptions** 成員。 使用 [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) 和 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函式，以程式設計方式設定此選項。

**Windows XP：** 若要從 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)叫用 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) ，則對 **RasDial** 的呼叫必須指定 [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85))結構，而且此結構必須指定 RDEOPT \_ UseCustomScripting 旗標。 此外，連接的電話簿專案必須指定 RASEO \_ CustomScript 選項，如前面段落中所述。

## <a name="invoking-the-custom-scripting-dll"></a>叫用自訂腳本 DLL

如果使用者針對已設定 RASEO CustomScript 的電話簿專案啟用連線，RAS 會叫用 \_ 自訂腳本 DLL。 在此案例中，RAS 會從 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)叫用自訂腳本 DLL。

若要以程式設計方式叫用自訂腳本 DLL，請使用 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) 函數建立連接。 在 Windows XP 上， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)函數也會叫用自訂腳本 DLL。

 

 