---
title: AccChecker 主控台
description: AccChecker 主控台 (AccCheckConsole.exe) 是一種命令列工具，可用於驗證應用程式 UI 的協助工具執行。
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- AccChecker 主控台
- AccChecker 命令列工具
- 命令列、AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839440"
---
# <a name="the-accchecker-console"></a><span data-ttu-id="bacc5-106">AccChecker 主控台</span><span class="sxs-lookup"><span data-stu-id="bacc5-106">The AccChecker Console</span></span>

<span data-ttu-id="bacc5-107">AccChecker 主控台 (AccCheckConsole.exe) 是一種命令列工具，可用於驗證應用程式 UI 的協助工具執行。</span><span class="sxs-lookup"><span data-stu-id="bacc5-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="bacc5-108">命令列接受各種輸入 (例如 HWND、視窗標題和驗證常式) ，並提供對應至錯誤記錄計數的結束代碼。</span><span class="sxs-lookup"><span data-stu-id="bacc5-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="bacc5-109">命令列語法</span><span class="sxs-lookup"><span data-stu-id="bacc5-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="bacc5-110">命令列錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bacc5-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="bacc5-111">命令列範例</span><span class="sxs-lookup"><span data-stu-id="bacc5-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="bacc5-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="bacc5-112">Related topics</span></span>](#related-topics)

![accchecker 主控台命令列工具](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="bacc5-114">命令列語法</span><span class="sxs-lookup"><span data-stu-id="bacc5-114">Command-line Syntax</span></span>

<span data-ttu-id="bacc5-115">AccChecker 主控台具有下列命令列語法。</span><span class="sxs-lookup"><span data-stu-id="bacc5-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="bacc5-116">**AccCheckConsole \[ 選項 \] (-hwnd <hwnd> \| -進程 <name>) \[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="bacc5-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="bacc5-117">命令列選項如下所示。</span><span class="sxs-lookup"><span data-stu-id="bacc5-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="bacc5-118">選項。</span><span class="sxs-lookup"><span data-stu-id="bacc5-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="bacc5-119">描述</span><span class="sxs-lookup"><span data-stu-id="bacc5-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bacc5-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span><span class="sxs-lookup"><span data-stu-id="bacc5-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="bacc5-121">驗證具有指定之控制碼 (HWND) 的視窗。</span><span class="sxs-lookup"><span data-stu-id="bacc5-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="bacc5-122">控制碼可以用十六進位或十進位來指定。</span><span class="sxs-lookup"><span data-stu-id="bacc5-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="bacc5-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-視窗 <title></span><span class="sxs-lookup"><span data-stu-id="bacc5-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="bacc5-124">驗證具有指定之標題的視窗。</span><span class="sxs-lookup"><span data-stu-id="bacc5-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="bacc5-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -進程 <name></span><span class="sxs-lookup"><span data-stu-id="bacc5-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="bacc5-126">驗證具有指定名稱之進程的主視窗。</span><span class="sxs-lookup"><span data-stu-id="bacc5-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="bacc5-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span><span class="sxs-lookup"><span data-stu-id="bacc5-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="bacc5-128">列出所有可用的驗證常式。</span><span class="sxs-lookup"><span data-stu-id="bacc5-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="bacc5-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -啟用 <name></span><span class="sxs-lookup"><span data-stu-id="bacc5-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="bacc5-130">執行指定的驗證常式。</span><span class="sxs-lookup"><span data-stu-id="bacc5-130">Runs the specified verification routine.</span></span> <span data-ttu-id="bacc5-131">此選項可指定一次以上。</span><span class="sxs-lookup"><span data-stu-id="bacc5-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="bacc5-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -停用 <name></span><span class="sxs-lookup"><span data-stu-id="bacc5-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="bacc5-133">除了指定的驗證常式之外，全部執行。</span><span class="sxs-lookup"><span data-stu-id="bacc5-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="bacc5-134">此選項可指定一次以上。</span><span class="sxs-lookup"><span data-stu-id="bacc5-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="bacc5-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info \| 警告 \| err) </span><span class="sxs-lookup"><span data-stu-id="bacc5-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="bacc5-136">將記錄的最低事件評等。</span><span class="sxs-lookup"><span data-stu-id="bacc5-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="bacc5-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span><span class="sxs-lookup"><span data-stu-id="bacc5-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="bacc5-138">將輸出寫入指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="bacc5-138">Write the output to the specified log file.</span></span> <span data-ttu-id="bacc5-139">此選項可指定一次以上。</span><span class="sxs-lookup"><span data-stu-id="bacc5-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="bacc5-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-隱藏 <file></span><span class="sxs-lookup"><span data-stu-id="bacc5-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="bacc5-141">使用指定的 XML 檔案來抑制錯誤。</span><span class="sxs-lookup"><span data-stu-id="bacc5-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="bacc5-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span><span class="sxs-lookup"><span data-stu-id="bacc5-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="bacc5-143">請勿將記錄輸出寫入至 stdout。</span><span class="sxs-lookup"><span data-stu-id="bacc5-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="bacc5-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span><span class="sxs-lookup"><span data-stu-id="bacc5-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="bacc5-145">顯示快速協助。</span><span class="sxs-lookup"><span data-stu-id="bacc5-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="bacc5-146">命令列錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bacc5-146">Command-line Error Codes</span></span>

<span data-ttu-id="bacc5-147">以下是使用 "echo% errorlevel%" 時，從 AccCheckConsole 傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bacc5-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="bacc5-148">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bacc5-148">Error code</span></span>                       | <span data-ttu-id="bacc5-149">描述</span><span class="sxs-lookup"><span data-stu-id="bacc5-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="bacc5-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="bacc5-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="bacc5-151">沒有錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="bacc5-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="bacc5-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="bacc5-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="bacc5-153">已要求使用方式語句。</span><span class="sxs-lookup"><span data-stu-id="bacc5-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="bacc5-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="bacc5-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="bacc5-155">錯誤與警告。</span><span class="sxs-lookup"><span data-stu-id="bacc5-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="bacc5-156"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="bacc5-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="bacc5-157">錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="bacc5-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="bacc5-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="bacc5-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="bacc5-159">警告但沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="bacc5-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="bacc5-160"><span id="5"></span>5</span><span class="sxs-lookup"><span data-stu-id="bacc5-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="bacc5-161">不正確命令列。</span><span class="sxs-lookup"><span data-stu-id="bacc5-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="bacc5-162">命令列範例</span><span class="sxs-lookup"><span data-stu-id="bacc5-162">Command-line Examples</span></span>

<span data-ttu-id="bacc5-163">以下是數個 AccChecker 主控台命令列範例。</span><span class="sxs-lookup"><span data-stu-id="bacc5-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="bacc5-164">在具有指定名稱的視窗上執行所有驗證。</span><span class="sxs-lookup"><span data-stu-id="bacc5-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="bacc5-165">**AccCheckConsole-視窗「未命名-記事本」**</span><span class="sxs-lookup"><span data-stu-id="bacc5-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="bacc5-166">針對 HWND 執行驗證的子集，並指定隱藏專案檔。</span><span class="sxs-lookup"><span data-stu-id="bacc5-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="bacc5-167">**AccCheckConsole-hwnd 0x00382f00-enable CheckTabbing-enable CheckName-抑制 suppress.xml**</span><span class="sxs-lookup"><span data-stu-id="bacc5-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="bacc5-168">從新的驗證 DLL 執行所有驗證。</span><span class="sxs-lookup"><span data-stu-id="bacc5-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="bacc5-169">**AccCheckConsole-視窗「未命名-記事本」 VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="bacc5-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="bacc5-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="bacc5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bacc5-171">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="bacc5-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





