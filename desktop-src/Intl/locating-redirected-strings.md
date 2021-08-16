---
description: 本主題討論找出重新導向之登錄字串的程式設計指示。 如需詳細資訊，請參閱使用登錄字串重新導向。
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: 尋找重新導向的字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c4e1a46b2c12af839e4c5b562eba18a80c8e814e5a6071dca925a14a46d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788478"
---
# <a name="locating-redirected-strings"></a>尋找重新導向的字串

本主題討論找出重新導向之登錄字串的程式設計指示。 如需詳細資訊，請參閱 [使用登錄字串](using-registry-string-redirection.md)重新導向。

## <a name="load-a-language-neutral-registry-value"></a>載入 Language-Neutral 登錄值

在 Windows Vista 和更新版本上，MUI 應用程式會使用中性語言的登錄值，以允許存取儲存在字串資源表格中的特定語言字串。 如需詳細資訊，請參閱 [使用登錄字串](using-registry-string-redirection.md)重新導向建立 Language-Neutral 資源。

從登錄讀取語言中立值的應用程式程式碼，應該藉由呼叫 [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa)，以正確的使用者介面語言載入字串。 如果使用此函式，則您的應用程式不需要明確地處理資源載入。

如果您要將現有的應用程式更新為非語言相關的登錄使用方式，您通常會將現有的字串值（當地語系化為英文）或登錄中的其他單一語言保留為回溯相容性和回溯相容性。 在登錄中保留常值字串，可讓應用程式在呼叫 [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) 失敗時，切換回常值字串。 您必須決定如何執行這類的回復，因為 MUI 不會提供這類實行的支援。

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>使用 Shell API 從登錄設定快速鍵字串

您的應用程式可以使用 shell API 來建立快捷方式的字串，以連結 [ **開始** ] 功能表或桌面上的檔案或資料夾。 如需詳細資訊，請參閱 [使用登錄字串](using-registry-string-redirection.md)重新導向建立快捷方式字串的資源。

應用程式可以使用 [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) 來載入快捷方式的 MUI 相容顯示名稱。 它應該使用 [**IShellLink：： SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) 來設定相關聯的簡介。 呼叫會向登錄註冊字串。 請考慮下列範例，其中 "HKCR" 代表 HKEY \_ 類別根登錄機 \_ 碼：


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



第一行提供反向和回溯相容性的未當地語系化常值字串。 第二行顯示符合 MUI 規範的方式來註冊顯示名稱。 這一行指出 Msascui.exe (中儲存的字串識別碼104，適用于 Windows XP) 或其相關聯的語言特定檔案 (Windows Vista) 。 此字串識別碼對應至「我的網路位置」。 範例中的第三行會處理提示註冊。 % CLSID \_ 反間諜軟體% 指定的環境變數代表符合這個元件之類別識別碼的 GUID。

在上述範例中，應用程式會呼叫 [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname)來指定前兩個參數的可執行檔路徑，並將 *idsRes* 指定為 "@% ProgramFiles% \\ Windows 反間諜功能 \\MSASCui.exe，104"。 呼叫 [**IShellLink：： SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)，將內容提示的路徑指定為 "@% ProgramFiles% \\ Windows 反間諜功能 \\MSASCui.exe，208"。

## <a name="query-friendly-document-type-names-in-the-registry"></a>在登錄中查詢易記的檔案類型名稱

[使用登錄字串](using-registry-string-redirection.md)重新導向建立方便使用的檔案類型名稱資源時，會在建立易記檔案類型名稱的資源中討論。 若要查詢易記的檔案名稱，應用程式應該使用 [**IQueryAssociations：： Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init)，然後呼叫 [**IQueryAssociations：： GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring)。 **IQueryAssociations：： Init** 的呼叫會指定檔案類型，例如「.txt」。 **IQueryAssociations：： GetString** 的呼叫必須將 ASSOCSTR \_ FRIENDLYDOCNAME 指定為字串識別碼。

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>登錄未從登錄讀取的 Microsoft Management Console 嵌入式管理單元字串

您的應用程式可以使用 Microsoft Management Console (MMC) 嵌入式管理單元來裝載其管理工作。 大部分的字串會使用在 [使用登錄字串](using-registry-string-redirection.md)重新導向的 Microsoft Management Console Snap-Ins 的 [建立字串資源] 中所述的登錄設定，以資源的形式處理。 不過，某些嵌入式管理單元會註冊 MMC 無法從登錄讀取的登錄字串值。 在此情況下，嵌入式管理單元必須使用 [**ISnapinAbout**](/windows/win32/api/mmc/nn-mmc-isnapinabout) 介面（與 MUI 相容）來取得值。

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>從登錄設定 Windows 服務的顯示名稱和描述

如果您的 MUI 應用程式使用 Windows 服務，則必須顯示服務顯示名稱和描述。 相關聯的資源將在[使用登錄字串](using-registry-string-redirection.md)重新導向的「建立 Windows 服務的字串資源」中討論。

為了設定服務顯示名稱，MUI 應用程式會呼叫 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) 或 [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)。 名稱是格式為 "" 的字串 `@<PE-path>,-<stringID>[;<comment>]` 。 例如，如果您的服務是由路徑為% ProgramFiles%%%MyDll.dll 的 .dll 檔案所執行 \\ \\ ，而且語言特定顯示名稱的字串識別碼為347，則會將參數指定為 " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` "。  () 的雙反斜線 \\ \\ 是必要的，因為 c/c + + 會使用反斜線做為字串中的 escape 字元。

若要設定語言特定的服務描述，MUI 應用程式應讓 [**服務 \_ 描述**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona)結構的 **lpDescription** 成員表示 "" 格式的字串，並 `@<PE-path>,-<stringID>[;<comment>]` 參考適當的字串識別碼。 然後，應用程式會呼叫 [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) ，並將參數 *DWINFOLEVEL* 指定為服務設定 \_ \_ 描述，並將參數 *lpInfo* 指定為 **服務 \_ 描述** 結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[尋找 Win32 PE 資源](locating-win32-pe-resources.md)
</dt> <dt>

[使用登錄字串重新導向](using-registry-string-redirection.md)
</dt> </dl>

 

 
