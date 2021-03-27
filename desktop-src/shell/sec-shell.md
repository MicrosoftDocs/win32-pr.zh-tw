---
description: 本主題提供與 Windows Shell 相關之安全性考慮的資訊。
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 安全性考慮： Microsoft Windows Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691200"
---
# <a name="security-considerations-microsoft-windows-shell"></a>安全性考慮： Microsoft Windows Shell

本主題提供與 Windows Shell 相關之安全性考慮的資訊。 本檔無法提供您所需的安全性問題相關資訊，而是將其作為此特定技術領域的起點和參考。

Shell 會控制系統的一些重要層面，包括有許多可能會在未適當處理的情況下呈現潛在的安全性風險。 本主題將概述一些較常見的問題，以及如何在您的應用程式中解決這些問題。 請記住，安全性並不限於以網際網路為基礎的攻擊。 在共用系統（包括可透過終端機服務存取的系統）上，您也必須確保使用者無法執行任何可能會危害共用系統的其他人。

-   [正確安裝您的應用程式](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [自動完成](#autocomplete)
-   [ShellExecute、ShellExecuteEx 和相關函數](#shellexecute-shellexecuteex-and-related-functions)
-   [移動和複製檔案](#moving-and-copying-files)
-   [撰寫安全的命名空間延伸模組](#writing-secure-namespace-extensions)
-   [安全性警示](#security-alerts)
-   [相關主題](#related-topics)

## <a name="installing-your-application-properly"></a>正確安裝您的應用程式

藉由正確安裝您的應用程式，可減輕大部分的潛在 Shell 安全性問題。

-   在 [Program Files] 資料夾下安裝應用程式。 

    | 作業系統                             | Location                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP、Windows Server 2003 及更早版本 | CSIDL \_ PROGRAM \_ FILES                                                                                                                                                                                                                      |
    | Windows Vista 和更新版本                      | FOLDERID \_ ProgramFiles、FOLDERID \_ PROGRAMFILESX86、FOLDERID \_ ProgramFilesX64、FOLDERID \_ ProgramFilesCommon、FOLDERID \_ ProgramFilesCommonX86 或 FOLDERID \_ ProgramFilesCommonX64。 如需詳細資訊，請參閱 [**KNOWNFOLDERID**](knownfolderid.md) 。 |

    

     

-   請勿在 [Program Files] 資料夾下儲存使用者資料。

    針對所有使用者通用的資料使用適當的 [資料] 資料夾。

    

    | 作業系統                             | Location               |
    |----------------------------------------------|------------------------|
    | Windows XP、Windows Server 2003 及更早版本 | CSIDL \_ 一般 \_ APPDATA |
    | Windows Vista 和更新版本                      | FOLDERID \_ ProgramData  |

    

     

    針對屬於特定使用者的資料，請使用適當的使用者資料檔案夾。

    

    | 作業系統                             | Location                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP、Windows Server 2003 及更早版本 | CSIDL \_ APPDATA、CSIDL \_ PERSONAL 及其他。               |
    | Windows Vista 和更新版本                      | FOLDERID \_ RoamingAppData、FOLDERID \_ 檔和其他檔。 |

    

     

-   如果您必須將安裝到 [Program Files] 資料夾以外的位置，請確定您已正確設定 (Acl 的存取控制清單) ，讓使用者無法存取檔案系統的不當部分。 特定使用者專屬的任何資料都應該有 ACL，以防止其他使用者存取它。
-   當您設定檔案關聯時，請務必適當地指定命令列。 使用完整路徑，並以引號括住包含空格的任何元素。 以個別的引號括住命令參數。 否則，字串可能會不正確地剖析，而且應用程式將無法正常啟動。 這裡顯示正確格式命令列的兩個範例。

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> 標準安裝資料夾的位置可能會因系統而異。 若要在特定的 Windows Vista 或更新版本的系統上取得標準資料夾的位置，請使用適當的 [**KNOWNFOLDERID**](knownfolderid.md)值來呼叫 [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 。 在 Windows XP、Windows Server 2003 或舊版的系統中，使用適當的 [**CSIDL**](csidl.md)值來呼叫 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)或 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 。

 

## <a name="shlwapi"></a>Shlwapi

Shell 輕量 API (Shlwapi) 包含許多字串操作函數。 不當使用這些函式可能會導致意外截斷的字串，而不會傳回截斷的通知。 在下列情況下，不應該使用 Shlwapi 函數。 列出的替代函式（有較少的風險）應該在其位置使用。



| Shlwapi 函式                                                 | 替代函數                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)、[**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata)、 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) 和相關函數             |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)、 [ **StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)、 [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) 和相關函數         |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)、 [ **wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa)、 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) 和相關函數 |



 

使用會傳回檔案路徑的函式（例如 [**pathrelativepathto 式**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) ），一律將緩衝區的大小設定為最大 \_ 路徑字元。 這麼做可確保緩衝區夠大，足以容納最大的可能檔案路徑，再加上終止的 null 字元。

如需有關替代字串函數的詳細資訊，請參閱[關於 >strsafe.h。](../menurc/strsafe-ovw.md)

## <a name="autocomplete"></a>自動完成

請勿使用密碼的自動完成功能。

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute、ShellExecuteEx 和相關函數

您可以使用數個 Shell 函數來啟動應用程式： [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)、 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)、 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)和 [**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw)。 請確定您為要執行的應用程式提供明確的定義。

-   提供可執行檔的路徑時，請提供完整路徑。 請勿依賴 Shell 來尋找檔案。
-   如果您提供的命令列字串包含空白字元，請使用引號括住字串。 否則，剖析器可能會將包含空格的單一元素解釋為多個元素。

## <a name="moving-and-copying-files"></a>移動和複製檔案

系統安全性的一個關鍵就是正確指派 Acl。 您也可以使用加密的檔案。 當您移動或複製檔案時，請確定它們已獲指派正確的 ACL，而且未不慎解密。 這包括將檔案移至 **資源回收筒** 以及檔案系統中。 使用 [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (windows Vista 或更新版本) 或 [**SHFILEOPERATION**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (windows XP 及更早的) 。 請勿使用 [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)，這可能不會為目的地檔案設定預期的 ACL。

## <a name="writing-secure-namespace-extensions"></a>撰寫安全的命名空間延伸模組

Shell 命名空間延伸模組是將資料呈現給使用者的功能強大且有彈性的方式。 但是，如果未正確寫入，它們可能會導致系統失敗。 以下是一些要牢記在心的重點：

-   請勿假設影像之類的資料已正確格式化。
-   請勿假設最大 \_ 路徑相當於字串中的 *位元組* 數目。 這是 *字元* 數。

## <a name="security-alerts"></a>安全性警示

下表列出某些功能（如果使用不正確），會危及應用程式的安全性。



| 功能                                                                        | 降低                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)、 [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | 相依于檢查一連串預設位置以尋找特定檔案的搜尋，可以在詐騙攻擊中使用。 使用完整路徑，以確保您可以存取所需的檔案。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | 第一個引數 *psz1* 必須夠大，才能容納 *psz2* 和結尾 ' \\ 0 '，否則可能會發生緩衝區溢位。 請改用下列其中一個替代方案。 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)、 [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa)、 [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna)、 [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa)、 [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata)、 [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)、 [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)或 [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa)。                                                                                                                                                             |
| [**StrCatBuff**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | 最終字串不保證會以 null 終止。 請改用下列其中一個替代方案。 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)、 [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa)、 [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna)、 [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa)、 [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata)、 [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)、 [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)或 [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa)。                                                                                                                                                                                                                                  |
| [**StrCatChainW**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | 最終字串不保證會以 null 終止。 請改用下列其中一個替代方案。 [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa)、 [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa)、 [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)或 [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa)。                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | 第一個引數 *psz1* 必須夠大，才能容納 *psz2* 和結尾 ' \\ 0 '，否則可能會發生緩衝區溢位。 請改用下列其中一個替代方案。 [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya)、 [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa)、 [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna)、 [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa)、 [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)、 [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)、 [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)或 [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa)。                                                                                                                                             |
| [**StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | 複製的字串不保證會以 null 終止。 請改用下列其中一個替代方案。 [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya)、 [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa)、 [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna)、 [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa)、 [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)、 [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)、 [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)、 [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa)。                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) 假設 *lpsz* 是以 null 終止的字串。 此外，傳回的字串不保證會以 null 終止。 請改用下列其中一個替代方案。 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)、 [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa)、 [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna)、 [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa)、 [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)、 [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)、 [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)或 [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa)。                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | 第一個引數 *pszFront* 必須夠大，才能容納 *pszBack* 和結尾 ' \\ 0 '，否則可能會發生緩衝區溢位。 請注意，最後一個引數 *cchMax* 是要複製到 *pszFront* 中的字元數，而不一定是 *pszFront* 的大小（以位元組為單位）。 請改用下列其中一個替代方案。 [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata)、 [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa)、 [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna)、 [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa)、 [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata)、 [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)、 [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)或 [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa)。 |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | 複製的字串不保證會以 null 終止。 請改用下列其中一個替代方案。 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)、 [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa)、 [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa)、 [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa)、 [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa)、 [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa)、 [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)或 [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa)。                                                                                                                                                                                 |
| [**wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | 複製的字串不保證會以 null 終止。 請改用下列其中一個替代方案。 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)、 [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa)、 [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa)、 [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa)、 [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa)、 [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa)、 [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)或 [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa)。                                                                                                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 安全性](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[安全性開發人員中心](https://msdn.microsoft.com/security/)
</dt> <dt>

[Microsoft Solution Accelerator](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[資訊安全技術中心](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[關於 >strsafe.h。h](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
