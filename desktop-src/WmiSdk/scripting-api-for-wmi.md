---
description: WMI 腳本參考包含 WMI 腳本 API 的定義。
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: 適用于 WMI 的腳本 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35045aa8528c5a3c27475fff753478bd2202d9137cec6b019039aac52775f70a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640538"
---
# <a name="scripting-api-for-wmi"></a>適用于 WMI 的腳本 API

WMI 腳本參考包含 WMI 腳本 API 的定義。 如果您使用 Microsoft Visual Basic、Visual Basic for Applications Visual Basic 腳本版本 (VBScript) ，或任何其他支援動態指令碼技術的指令碼語言來撰寫應用程式，請使用此 API。

> [!Note]  
> PowerShell 也可用於使用 WMI 編寫腳本。 Get-WMI Cmdlet 和三種類型加速器 (\[ wmi \] 、 \[ wmiclass \] 和 \[ wmisearcher \]) 啟用 wmi 的基本系統管理存取權。 如需詳細資訊，請參閱[使用 Windows PowerShell 編寫腳本](https://TechNet.Microsoft.Com/library/bb978526.aspx)。

 

除了 [**SWbemDateTime**](swbemdatetime.md) 以外，WMI 腳本物件也不會標示為安全，以在 INTERNET EXPLORER 的 HTML 網頁上執行腳本。 因此，除非 Internet Explorer 中的安全性層級減少，否則腳本將會失敗。 **SWbemDateTime** 標示為 safe 以進行初始化和腳本處理。 不過，在 Active Server Pages (ASP) 的伺服器端程式碼上，使用 **GetObject** 和 **CreateObject** 呼叫中的所有 WMI 腳本物件。

-   [腳本 API 物件模型](scripting-api-object-model.md)
-   [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)
-   [腳本 API 物件](scripting-api-objects.md)
-   [腳本 API 常數](scripting-api-constants.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 參考](wmi-reference.md)
</dt> <dt>

[WMI 傳回碼](wmi-return-codes.md)
</dt> </dl>

 

 



