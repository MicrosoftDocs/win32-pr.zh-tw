---
title: 損毀傾印分析
description: 本技術文章提供如何撰寫和使用小型傾印的相關資訊。
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c68891e2e20938036bd016e6e786a2cdad0096ae44af0e8974a88052963be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075518"
---
# <a name="crash-dump-analysis"></a>損毀傾印分析

在發行之前，並非所有的錯誤都可以找到，這表示在發行之前，您都可以找到擲回例外狀況的所有錯誤。 幸運的是，Microsoft 在 Platform SDK a 函式中包含了一個函式，可協助開發人員收集使用者所探索到之例外狀況的相關資訊。 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)函式會將必要的損毀傾印資訊寫入檔案，而不會儲存整個進程空間。 此損毀傾印資訊檔案稱為小型傾印。 本技術文章提供如何撰寫和使用小型傾印的相關資訊。

-   [撰寫小型傾印](#writing-a-minidump)
-   [執行緒安全](#thread-safety)
-   [使用程式碼撰寫小型傾印](#writing-a-minidump-with-code)
-   [使用 Dumpchk.exe](#using-dumpchkexe)
-   [分析小型傾印](#analyzing-a-minidump)
    -   [使用 Microsoft 公用符號伺服器](#using-the-microsoft-public-symbol-server)
    -   [使用 WinDbg 來調試小型傾印](#debugging-a-minidump-with-windbg)
    -   [使用 Copy-Protection 工具搭配小型傾印](#using-copy-protection-tools-with-minidumps)
-   [總結](#summary)

## <a name="writing-a-minidump"></a>撰寫小型傾印

撰寫小型傾印的基本選項如下：

-   不執行任何動作。 當程式擲回未處理的例外狀況時，Windows 自動產生小型傾印。 自 Windows XP 起提供自動產生的小型傾印。 如果使用者允許，則會透過 Windows 錯誤報告 (WER) ，將小型傾印傳送給 Microsoft，而不是開發人員。 開發人員可以透過[Windows 傳統型應用程式計畫](../appxpkg/windows-desktop-application-program.md)取得這些小型傾印的存取權。

    使用 WER 需要：

    -   開發人員使用 Authenticode 簽署其應用程式
    -   應用程式在每個可執行檔和 DLL 中都有有效的 VERSIONINFO 資源

    如果您針對未處理的例外狀況執行自訂常式，則強烈呼籲在例外狀況處理常式中使用 [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) 函式，也會將自動小型傾印傳送至 WER。 **ReportFault** 函式會處理連接至和傳送小型傾印至 WER 的所有問題。 未將小型傾印傳送至 WER 會違反 Windows 遊戲的需求。

    如需有關 WER 如何運作的詳細資訊，請參閱[Windows 錯誤報告的運作方式](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx)。 如需註冊詳細資料的說明，請參閱 MSDN [ISV 區域](https://msdn.microsoft.com/) [Windows 錯誤報告簡介](https://msdn.microsoft.com/)。

-   使用 Microsoft Visual Studio Team System 中的產品。 在 [ **調試** 程式] 功能表上，按一下 [ **儲存** 傾印]，儲存傾印的複本。 使用本機儲存的傾印只是內部測試和偵錯工具的選項。
-   將程式碼新增至您的專案。 新增 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 函式和適當的例外狀況處理常式代碼，以將小型傾印直接儲存並傳送給開發人員。 本文示範如何執行此選項。 不過，請注意， **MiniDumpWriteDump** 目前無法使用 managed 程式碼，且僅適用于 Windows XP、Windows Vista Windows 7。

## <a name="thread-safety"></a>執行緒安全

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 是 DBGHELP 程式庫的一部分。 此程式庫並非安全線程，因此任何使用 **MiniDumpWriteDump** 的程式都應該在嘗試呼叫 **MiniDumpWriteDump** 之前，先同步處理所有線程。

## <a name="writing-a-minidump-with-code"></a>使用程式碼撰寫小型傾印

實際的實值相當簡單。 以下是如何使用 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)的簡單範例。


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



此範例示範 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 的基本使用方式，以及呼叫它所需的最小資訊。 傾印檔案的名稱是由開發人員所組成;不過，若要避免檔案名衝突，建議您從應用程式的名稱和版本號碼、進程和執行緒識別碼，以及日期和時間產生檔案名。 這也有助於將小型傾印依應用程式和版本分組。 開發人員決定要使用多少資訊來區分小型傾印檔案名。

請注意，上述範例中的路徑名稱是藉由呼叫 [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) 函式來取得為暫存檔案指定的目錄路徑所產生。 即使使用最低許可權的使用者帳戶，也可以使用此目錄，也可防止小型傾印在不再需要時佔用硬碟空間。

如果您在每日組建程式期間封存產品，也請務必包含組建的符號，如此一來，您就可以在必要時，將舊版本的產品進行調試。 您也必須採取步驟，以在產生符號時維持完整的編譯器優化。 這可以藉由在開發環境中開啟您的專案屬性來完成，而若要進行發行設定，請執行下列動作：

1.  在專案屬性頁的左側，按一下 [C/c + +]。 根據預設，這會顯示 **[一般** ] 設定。 在專案屬性頁的右邊，將 [ **偵錯工具資訊格式** ] 設定為 [ **程式資料庫] (/zi)**。
2.  在 [屬性] 頁面的左側，展開 [ **連結器**]，然後 **按一下 [** 偵測]。 在 [屬性] 頁面的右邊，將 [ **產生偵錯工具資訊** ] 設定為 **[是] (/debug)**。
3.  按一下 [ **優化**]，並將 [E Liminate 未參考 (資料的 **參考** ] 設定為 [**]： REF)**。
4.  設定 **啟用 COMDAT 折** 迭以 **移除多餘的 comdat (/opt： ICF)**。

MSDN 有更多小型傾印 [**\_ 例外狀況 \_ 資訊**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) 結構和 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 函式的詳細資訊。

## <a name="using-dumpchkexe"></a>使用 Dumpchk.exe

Dumpchk.exe 是一種命令列公用程式，可用來確認已正確建立傾印檔案。 如果 Dumpchk.exe 產生錯誤，則傾印檔案已損毀且無法進行分析。 如需使用 Dumpchk.exe 的詳細資訊，請參閱 [如何使用 Dumpchk.exe 檢查記憶體傾印](https://support.microsoft.com/kb/315271/)檔案。

Dumpchk.exe 包含在 Windows xp 產品光碟中，並可透過在 \\ \\ \\ \\ \\ Windows XP 產品 cd 上的支援工具資料夾中執行 Setup.exe，安裝至系統磁片磁碟機程式檔支援工具。 您也可以從[Windows 硬體開發人員中心](https://www.microsoft.com/whdc/)的[Windows 調試](https://www.microsoft.com/whdc/devtools/debugging/)程式下載並安裝可用的偵錯工具，以取得最新版本的 Dumpchk.exe。

## <a name="analyzing-a-minidump"></a>分析小型傾印

開啟小型傾印以進行分析，就像建立一個小型傾印一樣簡單。

**分析小型傾印**

1.  開啟 Visual Studio。
2.  **在 [檔案**] 功能表上，按一下 [**開啟 Project**]。
3.  將 **類型的** 檔案設定 **為傾** 印檔案、流覽至傾印檔案、加以選取，然後按一下 [ **開啟]。**
4.  執行偵錯工具。

偵錯工具將會建立模擬的進程。 模擬的進程將會在造成損毀的指令上停止。

### <a name="using-the-microsoft-public-symbol-server"></a>使用 Microsoft 公用符號伺服器

若要取得驅動程式或系統層級損毀的堆疊，可能必須設定 Visual Studio 以指向 Microsoft 公用符號伺服器。

**設定 Microsoft 符號伺服器的路徑**

1.  在 [ **調試** ] 功能表上，按一下 [ **選項**]。
2.  在 [ **選項** ] 對話方塊中，開啟 [ **調試** ] 節點，然後按一下 [ **符號**]。
3.  除非您想要在進行偵錯工具時手動載入符號，否則請務必 **只在手動載入符號時搜尋上面的位置** 。
4.  如果您在遠端符號伺服器上使用符號，可以藉由指定可將符號複製到其中的本機目錄，來改善效能。 若要這樣做，請輸入 **從符號伺服器到這個目錄** 的快取符號路徑。 若要連接到 Microsoft public 符號伺服器，您必須啟用此設定。 請注意，如果您要在遠端電腦上進行程式的偵錯工具，則快取目錄會參考遠端電腦上的目錄。
5.  按一下 [確定]。
6.  因為您使用的是 Microsoft public 符號伺服器，所以會出現 [使用者授權合約] 對話方塊。 按一下 **[是]** 接受合約並將符號下載至本機快取。

### <a name="debugging-a-minidump-with-windbg"></a>使用 WinDbg 來調試小型傾印

您也可以使用 WinDbg （屬於 Windows 偵錯工具的偵錯工具）來對小型傾印進行 debug。 WinDbg 可讓您在不需要使用 Visual Studio 的情況下進行 debug。 若要下載 Windows 調試工具，請參閱[Windows 硬體開發人員中心](https://www.microsoft.com/whdc/)上的[Windows 調試工具](https://www.microsoft.com/whdc/devtools/debugging/)。

安裝 Windows 調試工具之後，您必須在 WinDbg 中輸入符號路徑。

**在 WinDbg 中輸入符號路徑**

1.  **在 [檔案**] 功能表上，按一下 [**符號路徑**]。
2.  在 [ **符號搜尋路徑** ] 視窗中，輸入下列內容：

    "srv \* c： \\ cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>使用 Copy-Protection 工具搭配小型傾印

開發人員也必須知道其禁止複製配置可能對小型傾印有何影響。 大部分的禁止複製配置都有自己的 descramble 工具，而開發人員可以透過 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)來學習如何使用這些工具。

## <a name="summary"></a>總結

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)函式可能是在產品發行之後，收集和解決 bug 時非常實用的工具。 撰寫使用 **MiniDumpWriteDump** 的自訂例外狀況處理常式，可讓開發人員自訂資訊集合並改進偵錯工具。 函式很有彈性，可用於任何以 c + + 為基礎的專案中，且應該視為任何專案的穩定性程式的一部分。

 

 