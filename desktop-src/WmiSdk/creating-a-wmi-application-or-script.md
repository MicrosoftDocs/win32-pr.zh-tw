---
description: 適用于 ActiveX 物件的任何指令碼語言（如 VBScript）都可以存取 WMI 資料。 應用程式可以在 c + + 中使用適用于 wmi 的 COM API 或 Visual Basic 中的 wmi，使用 >wbemdisp.tlb .tlb 類型程式庫和適用于 wmi 的腳本 API 來存取 wmi。 .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: 建立 WMI 應用程式或腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddde26b2a8495126b4aa26c132adb49860627230d698431df5d713e653f1d874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412128"
---
# <a name="creating-a-wmi-application-or-script"></a>建立 WMI 應用程式或腳本

適用于 ActiveX 物件的任何指令碼語言（如 VBScript）都可以存取 WMI 資料。 應用程式可以在 c + + 中使用[適用于 wmi 的 COM API](com-api-for-wmi.md)或 Visual Basic 中的 wmi，使用 >wbemdisp.tlb .tlb[類型程式庫](using-the-wmi-scripting-type-library.md)和[適用于 wmi 的腳本 API](scripting-api-for-wmi.md)來存取 wmi。 . 您可以撰寫腳本、使用中的伺服器頁 (ASP) ，或 (HTA) 的 HTML 應用程式，以透過 WMI 取得資料。 您也可以使用 Windows PowerShell 來取得資料或撰寫腳本。 如需詳細資訊，請參閱[WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)和[使用 Windows PowerShell 的開始使用](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true)。 TechNet ScriptCenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) 包含上百個腳本範例。 如需列印和線上資源的詳細資訊，請參閱 [進一步的資訊](further-information.md)。

下列程式說明如何連接至 WMI 服務和資料存放區。

**連接到 WMI 服務和資料存放區**

1.  在特定電腦上找出 WMI 服務。
2.  連線一或多個 WMI 命名空間。

在 c + +、Visual Basic、.NET Framework 語言或使用腳本時，這些作業會有所不同。 腳本和 Visual Basic 應用程式必須存取類別，而這些類別的實例是由現有提供者提供資料。 但以 c + + 撰寫的應用程式可以達成更多目的。 例如，以 c + + 撰寫的應用程式可以傳送事件，但是 WMI 腳本只能訂閱接收事件。

WMI 提供者只能使用 c + + 或 .NET Framework 來撰寫。 如需有關以 c # 或 Visual Basic .net 撰寫應用程式的詳細資訊，請參閱[WMI .net 總覽](/previous-versions/bb404655(v=vs.90))。

如需建立 WMI 應用程式和腳本的詳細資訊，請參閱：

-   [使用 c + + 建立 WMI 應用程式](creating-a-wmi-application-using-c-.md)
-   [建立 WMI 腳本](creating-a-wmi-script.md)
-   [建立受控 WMI 用戶端](creating-a-managed-wmi-client.md)

若要執行大部分的工作，請使用預先安裝的 [WMI 類別](wmi-classes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI](using-wmi.md)
</dt> </dl>

 

 
