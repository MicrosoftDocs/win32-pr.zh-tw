---
title: 損毀傾印分析
description: 本技術文章提供如何撰寫和使用小型傾印的相關資訊。
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023729"
---
# <a name="crash-dump-analysis"></a><span data-ttu-id="79c80-103">損毀傾印分析</span><span class="sxs-lookup"><span data-stu-id="79c80-103">Crash Dump Analysis</span></span>

<span data-ttu-id="79c80-104">在發行之前，並非所有的錯誤都可以找到，這表示在發行之前，您都可以找到擲回例外狀況的所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="79c80-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="79c80-105">幸運的是，Microsoft 在 Platform SDK a 函式中包含了一個函式，可協助開發人員收集使用者所探索到之例外狀況的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79c80-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="79c80-106">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)函式會將必要的損毀傾印資訊寫入檔案，而不會儲存整個進程空間。</span><span class="sxs-lookup"><span data-stu-id="79c80-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="79c80-107">此損毀傾印資訊檔案稱為小型傾印。</span><span class="sxs-lookup"><span data-stu-id="79c80-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="79c80-108">本技術文章提供如何撰寫和使用小型傾印的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79c80-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="79c80-109">撰寫小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="79c80-110">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="79c80-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="79c80-111">使用程式碼撰寫小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="79c80-112">使用 Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="79c80-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="79c80-113">分析小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="79c80-114">使用 Microsoft 公用符號伺服器</span><span class="sxs-lookup"><span data-stu-id="79c80-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="79c80-115">使用 WinDbg 來調試小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="79c80-116">使用 Copy-Protection 工具搭配小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="79c80-117">總結</span><span class="sxs-lookup"><span data-stu-id="79c80-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="79c80-118">撰寫小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-118">Writing a Minidump</span></span>

<span data-ttu-id="79c80-119">撰寫小型傾印的基本選項如下：</span><span class="sxs-lookup"><span data-stu-id="79c80-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="79c80-120">不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="79c80-120">Do nothing.</span></span> <span data-ttu-id="79c80-121">每當程式擲回未處理的例外狀況時，Windows 就會自動產生小型傾印。</span><span class="sxs-lookup"><span data-stu-id="79c80-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="79c80-122">自 Windows XP 起提供自動產生的小型傾印。</span><span class="sxs-lookup"><span data-stu-id="79c80-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="79c80-123">如果使用者允許，則會透過 Windows 錯誤報告 (WER) ，將小型傾印傳送給 Microsoft，而不是開發人員。</span><span class="sxs-lookup"><span data-stu-id="79c80-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="79c80-124">開發人員可以透過 [Windows 傳統型應用程式計畫](../appxpkg/windows-desktop-application-program.md)取得這些小型傾印的存取權。</span><span class="sxs-lookup"><span data-stu-id="79c80-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="79c80-125">使用 WER 需要：</span><span class="sxs-lookup"><span data-stu-id="79c80-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="79c80-126">開發人員使用 Authenticode 簽署其應用程式</span><span class="sxs-lookup"><span data-stu-id="79c80-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="79c80-127">應用程式在每個可執行檔和 DLL 中都有有效的 VERSIONINFO 資源</span><span class="sxs-lookup"><span data-stu-id="79c80-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="79c80-128">如果您針對未處理的例外狀況執行自訂常式，則強烈呼籲在例外狀況處理常式中使用 [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) 函式，也會將自動小型傾印傳送至 WER。</span><span class="sxs-lookup"><span data-stu-id="79c80-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="79c80-129">**ReportFault** 函式會處理連接至和傳送小型傾印至 WER 的所有問題。</span><span class="sxs-lookup"><span data-stu-id="79c80-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="79c80-130">未將小型傾印傳送至 WER 違反 Windows 遊戲的需求。</span><span class="sxs-lookup"><span data-stu-id="79c80-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="79c80-131">如需有關 WER 如何運作的詳細資訊，請參閱 [Windows 錯誤報告的運作方式](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx)。</span><span class="sxs-lookup"><span data-stu-id="79c80-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="79c80-132">如需註冊詳細資料的說明，請參閱 MSDN [ISV 區域](https://msdn.microsoft.com/) [Windows 錯誤報告簡介](https://msdn.microsoft.com/)。</span><span class="sxs-lookup"><span data-stu-id="79c80-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="79c80-133">使用 Microsoft Visual Studio Team System 中的產品。</span><span class="sxs-lookup"><span data-stu-id="79c80-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="79c80-134">在 [ **調試** 程式] 功能表上，按一下 [ **儲存** 傾印]，儲存傾印的複本。</span><span class="sxs-lookup"><span data-stu-id="79c80-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="79c80-135">使用本機儲存的傾印只是內部測試和偵錯工具的選項。</span><span class="sxs-lookup"><span data-stu-id="79c80-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="79c80-136">將程式碼新增至您的專案。</span><span class="sxs-lookup"><span data-stu-id="79c80-136">Add code to your project.</span></span> <span data-ttu-id="79c80-137">新增 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 函式和適當的例外狀況處理常式代碼，以將小型傾印直接儲存並傳送給開發人員。</span><span class="sxs-lookup"><span data-stu-id="79c80-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="79c80-138">本文示範如何執行此選項。</span><span class="sxs-lookup"><span data-stu-id="79c80-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="79c80-139">不過，請注意， **MiniDumpWriteDump** 目前無法使用 managed 程式碼，且僅適用于 windows XP、windows Vista、windows 7。</span><span class="sxs-lookup"><span data-stu-id="79c80-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="79c80-140">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="79c80-140">Thread safety</span></span>

<span data-ttu-id="79c80-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 是 DBGHELP 程式庫的一部分。</span><span class="sxs-lookup"><span data-stu-id="79c80-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="79c80-142">此程式庫並非安全線程，因此任何使用 **MiniDumpWriteDump** 的程式都應該在嘗試呼叫 **MiniDumpWriteDump** 之前，先同步處理所有線程。</span><span class="sxs-lookup"><span data-stu-id="79c80-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="79c80-143">使用程式碼撰寫小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="79c80-144">實際的實值相當簡單。</span><span class="sxs-lookup"><span data-stu-id="79c80-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="79c80-145">以下是如何使用 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)的簡單範例。</span><span class="sxs-lookup"><span data-stu-id="79c80-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


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



<span data-ttu-id="79c80-146">此範例示範 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 的基本使用方式，以及呼叫它所需的最小資訊。</span><span class="sxs-lookup"><span data-stu-id="79c80-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="79c80-147">傾印檔案的名稱是由開發人員所組成;不過，若要避免檔案名衝突，建議您從應用程式的名稱和版本號碼、進程和執行緒識別碼，以及日期和時間產生檔案名。</span><span class="sxs-lookup"><span data-stu-id="79c80-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="79c80-148">這也有助於將小型傾印依應用程式和版本分組。</span><span class="sxs-lookup"><span data-stu-id="79c80-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="79c80-149">開發人員決定要使用多少資訊來區分小型傾印檔案名。</span><span class="sxs-lookup"><span data-stu-id="79c80-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="79c80-150">請注意，上述範例中的路徑名稱是藉由呼叫 [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) 函式來取得為暫存檔案指定的目錄路徑所產生。</span><span class="sxs-lookup"><span data-stu-id="79c80-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="79c80-151">即使使用最低許可權的使用者帳戶，也可以使用此目錄，也可防止小型傾印在不再需要時佔用硬碟空間。</span><span class="sxs-lookup"><span data-stu-id="79c80-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="79c80-152">如果您在每日組建程式期間封存產品，也請務必包含組建的符號，如此一來，您就可以在必要時，將舊版本的產品進行調試。</span><span class="sxs-lookup"><span data-stu-id="79c80-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="79c80-153">您也必須採取步驟，以在產生符號時維持完整的編譯器優化。</span><span class="sxs-lookup"><span data-stu-id="79c80-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="79c80-154">這可以藉由在開發環境中開啟您的專案屬性來完成，而若要進行發行設定，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="79c80-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="79c80-155">在專案屬性頁的左側，按一下 [C/c + +]。</span><span class="sxs-lookup"><span data-stu-id="79c80-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="79c80-156">根據預設，這會顯示 **[一般** ] 設定。</span><span class="sxs-lookup"><span data-stu-id="79c80-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="79c80-157">在專案屬性頁的右邊，將 [ **偵錯工具資訊格式** ] 設定為 [ **程式資料庫] (/zi)**。</span><span class="sxs-lookup"><span data-stu-id="79c80-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="79c80-158">在 [屬性] 頁面的左側，展開 [ **連結器**]，然後 **按一下 [** 偵測]。</span><span class="sxs-lookup"><span data-stu-id="79c80-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="79c80-159">在 [屬性] 頁面的右邊，將 [ **產生偵錯工具資訊** ] 設定為 **[是] (/debug)**。</span><span class="sxs-lookup"><span data-stu-id="79c80-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="79c80-160">按一下 [ **優化**]，並將 [E Liminate 未參考 (資料的 **參考** ] 設定為 [**]： REF)**。</span><span class="sxs-lookup"><span data-stu-id="79c80-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="79c80-161">設定 **啟用 COMDAT 折** 迭以 **移除多餘的 comdat (/opt： ICF)**。</span><span class="sxs-lookup"><span data-stu-id="79c80-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="79c80-162">MSDN 有更多小型傾印 [**\_ 例外狀況 \_ 資訊**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) 結構和 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) 函式的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="79c80-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="79c80-163">使用 Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="79c80-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="79c80-164">Dumpchk.exe 是一種命令列公用程式，可用來確認已正確建立傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="79c80-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="79c80-165">如果 Dumpchk.exe 產生錯誤，則傾印檔案已損毀且無法進行分析。</span><span class="sxs-lookup"><span data-stu-id="79c80-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="79c80-166">如需使用 Dumpchk.exe 的詳細資訊，請參閱 [如何使用 Dumpchk.exe 檢查記憶體傾印](https://support.microsoft.com/kb/315271/)檔案。</span><span class="sxs-lookup"><span data-stu-id="79c80-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="79c80-167">Dumpchk.exe 包含在 Windows XP 產品光碟中，並可透過在 \\ \\ \\ \\ \\ windows Xp 產品 cd 上的支援工具資料夾中執行 Setup.exe，安裝至系統磁片磁碟機程式檔支援工具。</span><span class="sxs-lookup"><span data-stu-id="79c80-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="79c80-168">您也可以下載並安裝 windows[硬體開發人員中心](https://www.microsoft.com/whdc/)上[windows 調試](https://www.microsoft.com/whdc/devtools/debugging/)程式所提供的偵錯工具，以取得最新版本的 Dumpchk.exe。</span><span class="sxs-lookup"><span data-stu-id="79c80-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="79c80-169">分析小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-169">Analyzing a Minidump</span></span>

<span data-ttu-id="79c80-170">開啟小型傾印以進行分析，就像建立一個小型傾印一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="79c80-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="79c80-171">**分析小型傾印**</span><span class="sxs-lookup"><span data-stu-id="79c80-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="79c80-172">開啟 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="79c80-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="79c80-173">**在 [檔案**] 功能表上，按一下 [**開啟專案**]。</span><span class="sxs-lookup"><span data-stu-id="79c80-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="79c80-174">將 **類型的** 檔案設定 **為傾** 印檔案、流覽至傾印檔案、加以選取，然後按一下 [ **開啟]。**</span><span class="sxs-lookup"><span data-stu-id="79c80-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="79c80-175">執行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="79c80-175">Run the debugger.</span></span>

<span data-ttu-id="79c80-176">偵錯工具將會建立模擬的進程。</span><span class="sxs-lookup"><span data-stu-id="79c80-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="79c80-177">模擬的進程將會在造成損毀的指令上停止。</span><span class="sxs-lookup"><span data-stu-id="79c80-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="79c80-178">使用 Microsoft 公用符號伺服器</span><span class="sxs-lookup"><span data-stu-id="79c80-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="79c80-179">若要取得驅動程式或系統層級損毀的堆疊，可能必須設定 Visual Studio 以指向 Microsoft 公用符號伺服器。</span><span class="sxs-lookup"><span data-stu-id="79c80-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="79c80-180">**設定 Microsoft 符號伺服器的路徑**</span><span class="sxs-lookup"><span data-stu-id="79c80-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="79c80-181">在 [ **調試** ] 功能表上，按一下 [ **選項**]。</span><span class="sxs-lookup"><span data-stu-id="79c80-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="79c80-182">在 [ **選項** ] 對話方塊中，開啟 [ **調試** ] 節點，然後按一下 [ **符號**]。</span><span class="sxs-lookup"><span data-stu-id="79c80-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="79c80-183">除非您想要在進行偵錯工具時手動載入符號，否則請務必 **只在手動載入符號時搜尋上面的位置** 。</span><span class="sxs-lookup"><span data-stu-id="79c80-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="79c80-184">如果您在遠端符號伺服器上使用符號，可以藉由指定可將符號複製到其中的本機目錄，來改善效能。</span><span class="sxs-lookup"><span data-stu-id="79c80-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="79c80-185">若要這樣做，請輸入 **從符號伺服器到這個目錄** 的快取符號路徑。</span><span class="sxs-lookup"><span data-stu-id="79c80-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="79c80-186">若要連接到 Microsoft public 符號伺服器，您必須啟用此設定。</span><span class="sxs-lookup"><span data-stu-id="79c80-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="79c80-187">請注意，如果您要在遠端電腦上進行程式的偵錯工具，則快取目錄會參考遠端電腦上的目錄。</span><span class="sxs-lookup"><span data-stu-id="79c80-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="79c80-188">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="79c80-188">Click **OK**.</span></span>
6.  <span data-ttu-id="79c80-189">因為您使用的是 Microsoft public 符號伺服器，所以會出現 [使用者授權合約] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="79c80-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="79c80-190">按一下 **[是]** 接受合約並將符號下載至本機快取。</span><span class="sxs-lookup"><span data-stu-id="79c80-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="79c80-191">使用 WinDbg 來調試小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="79c80-192">您也可以使用 WinDbg （屬於 Windows 偵錯工具的偵錯工具）來對小型傾印進行 debug 錯。</span><span class="sxs-lookup"><span data-stu-id="79c80-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="79c80-193">WinDbg 可讓您在不需要使用 Visual Studio 的情況下進行 debug。</span><span class="sxs-lookup"><span data-stu-id="79c80-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="79c80-194">若要下載 Windows 調試工具，請參閱[Windows 硬體開發人員中心](https://www.microsoft.com/whdc/)上的[windows 調試工具](https://www.microsoft.com/whdc/devtools/debugging/)。</span><span class="sxs-lookup"><span data-stu-id="79c80-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="79c80-195">安裝 Windows 調試工具之後，您必須在 WinDbg 中輸入符號路徑。</span><span class="sxs-lookup"><span data-stu-id="79c80-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="79c80-196">**在 WinDbg 中輸入符號路徑**</span><span class="sxs-lookup"><span data-stu-id="79c80-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="79c80-197">**在 [檔案**] 功能表上，按一下 [**符號路徑**]。</span><span class="sxs-lookup"><span data-stu-id="79c80-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="79c80-198">在 [ **符號搜尋路徑** ] 視窗中，輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="79c80-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="79c80-199">"srv \* c： \\ cache \* https://msdl.microsoft.com/download/symbols ;"</span><span class="sxs-lookup"><span data-stu-id="79c80-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="79c80-200">使用 Copy-Protection 工具搭配小型傾印</span><span class="sxs-lookup"><span data-stu-id="79c80-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="79c80-201">開發人員也必須知道其禁止複製配置可能對小型傾印有何影響。</span><span class="sxs-lookup"><span data-stu-id="79c80-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="79c80-202">大部分的禁止複製配置都有自己的 descramble 工具，而開發人員可以透過 [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)來學習如何使用這些工具。</span><span class="sxs-lookup"><span data-stu-id="79c80-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="79c80-203">總結</span><span class="sxs-lookup"><span data-stu-id="79c80-203">Summary</span></span>

<span data-ttu-id="79c80-204">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)函式可能是在產品發行之後，收集和解決 bug 時非常實用的工具。</span><span class="sxs-lookup"><span data-stu-id="79c80-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="79c80-205">撰寫使用 **MiniDumpWriteDump** 的自訂例外狀況處理常式，可讓開發人員自訂資訊集合並改進偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="79c80-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="79c80-206">函式很有彈性，可用於任何以 c + + 為基礎的專案中，且應該視為任何專案的穩定性程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="79c80-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 