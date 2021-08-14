---
title: 自訂撥號
description: Windows 2000 和更新版本的作業系統，可讓開發人員提供自己的自訂撥號程式，以與遠端存取服務 (RAS) 搭配使用。
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- 自訂撥號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791498"
---
# <a name="custom-dialers"></a>自訂撥號

Windows 2000 和更新版本的作業系統，可讓開發人員提供自己的自訂撥號程式，以與遠端存取服務 (RAS) 搭配使用。 自訂的撥號程式會實作為單一動態連結程式庫 (DLL) ，以匯出下列進入點：

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

自訂撥號 DLL 必須匯出所有的進入點，而且必須將進入點實作為 Unicode 函數。 如需這些函式的詳細資訊，請參閱 Windows SDK 遠端存取服務參考中各項功能的參考頁面。

為了讓 RAS 連線使用自訂撥號程式，連接的電話簿專案必須包含自訂撥號 DLL 的路徑。 使用 [RAS API 函式 [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa)和 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) ]，在 [電話簿] 專案的 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))結構的 **szCustomDialDll** 成員中設定此路徑。

## <a name="updating-the-registry-for-custom-dialers"></a>更新自訂撥號的登錄

為了讓系統能夠撥號使用自訂撥號程式的連線，自訂撥號 DLL 的路徑必須存在於下列登錄值中。

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

由於 **CustomDLL** 的類型為 **REG \_ multiple \_ SZ**，因此可以保留多個自訂撥號 dll 的路徑。 除了連線的電話簿專案以外，您還需要設定此登錄值中自訂撥號 DLL 的路徑。

根據預設，此登錄值只能由具有系統管理員或系統許可權的使用者寫入。 基於安全考慮，請勿變更此登錄機碼的許可權。

## <a name="using-custom-dialers-at-system-logon"></a>在系統登入時使用自訂的撥號

Windows 2000 和更新版本的作業系統可讓使用者在登入時建立 RAS 連接。 若要這樣做，使用者會使用 [**登入資訊**] 對話方塊中的 [**撥號網路**] 來檢查登入。 當使用者按一下 [確定] 按鈕之後，系統會顯示可用的連接。

## <a name="security-considerations"></a>安全性考量

在大多數情況下，自訂撥號程式會使用叫用它之使用者的安全性許可權來操作。 但是，如果在登入時叫用自訂撥號程式，它就會以系統許可權運作。 因此，請設計自訂的撥號程式，使其無法用來違反系統安全性。 例如，撥號程式不應顯示使用者介面，以允許使用者對電腦檔案系統的寫入權限。 提供這類存取的使用者介面包括 [**尋找** 檔案] 對話方塊、[**開啟** 檔案] 對話方塊，**以及 Windows 說明**]。

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>自訂的撥號程式消費者介面必須支援 IDCANCEL

如果自訂撥號程式顯示使用者介面，則使用者介面必須支援 \_ LOWORD (*WParam*) 等於 IDCANCEL 的 WM 命令訊息。

 

 