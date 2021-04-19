---
description: Wilogutl.exe 有助於分析 Windows Installer 安裝中的記錄檔，並顯示在記錄檔中找到之錯誤的建議解決方案。
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975570"
---
# <a name="wilogutlexe"></a><span data-ttu-id="48f2c-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="48f2c-103">Wilogutl.exe</span></span>

<span data-ttu-id="48f2c-104">Wilogutl.exe 有助於分析 Windows Installer 安裝中的記錄檔，並顯示在記錄檔中找到之錯誤的建議解決方案。</span><span class="sxs-lookup"><span data-stu-id="48f2c-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="48f2c-105">不會顯示非重大錯誤。</span><span class="sxs-lookup"><span data-stu-id="48f2c-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="48f2c-106">Wilogutl.exe 可以在無訊息模式下執行，也可以使用使用者介面 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="48f2c-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="48f2c-107">此工具會在 UI 和無訊息模式中，以文字檔的形式產生報表。</span><span class="sxs-lookup"><span data-stu-id="48f2c-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="48f2c-108">它最適合用於詳細的 Windows Installer 記錄檔，但也適用于不詳細的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="48f2c-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="48f2c-109">如需詳細資訊，請參閱[記錄](logging.md)。</span><span class="sxs-lookup"><span data-stu-id="48f2c-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="48f2c-110">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="48f2c-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="48f2c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="48f2c-111">Syntax</span></span>

<span data-ttu-id="48f2c-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="48f2c-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="48f2c-113">您可以使用下列命令列以安靜模式執行。</span><span class="sxs-lookup"><span data-stu-id="48f2c-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="48f2c-114">**wilogutl/q/l** *c： \\ mymsilog。記錄* **/o** *c \\ outputdir \\*</span><span class="sxs-lookup"><span data-stu-id="48f2c-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="48f2c-115">**wilogutl/q/l** *c： \\ mymsilog .log*</span><span class="sxs-lookup"><span data-stu-id="48f2c-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="48f2c-116">命令列選項</span><span class="sxs-lookup"><span data-stu-id="48f2c-116">Command-Line Options</span></span>

<span data-ttu-id="48f2c-117">Wilogutl.exe 使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="48f2c-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="48f2c-118">虛線分隔符號可以用來取代斜線。</span><span class="sxs-lookup"><span data-stu-id="48f2c-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="48f2c-119">選項</span><span class="sxs-lookup"><span data-stu-id="48f2c-119">Option</span></span> | <span data-ttu-id="48f2c-120">Description</span><span class="sxs-lookup"><span data-stu-id="48f2c-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f2c-121">無</span><span class="sxs-lookup"><span data-stu-id="48f2c-121">none</span></span>   | <span data-ttu-id="48f2c-122">在 UI 模式中執行，不需要命令列選項。</span><span class="sxs-lookup"><span data-stu-id="48f2c-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="48f2c-123">/q</span><span class="sxs-lookup"><span data-stu-id="48f2c-123">/q</span></span>     | <span data-ttu-id="48f2c-124">指定無訊息模式。</span><span class="sxs-lookup"><span data-stu-id="48f2c-124">Specifies the quiet mode.</span></span> <span data-ttu-id="48f2c-125">Wilogutl.exe 會產生報表檔案，而且不會顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="48f2c-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="48f2c-126">/l</span><span class="sxs-lookup"><span data-stu-id="48f2c-126">/l</span></span>     | <span data-ttu-id="48f2c-127">指定要分析之記錄檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="48f2c-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="48f2c-128">使用無訊息模式時，需要這個選項。</span><span class="sxs-lookup"><span data-stu-id="48f2c-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="48f2c-129">/o</span><span class="sxs-lookup"><span data-stu-id="48f2c-129">/o</span></span>     | <span data-ttu-id="48f2c-130">指定報告檔案的輸出目錄。</span><span class="sxs-lookup"><span data-stu-id="48f2c-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="48f2c-131">只有在以無訊息模式執行時，才會使用這個輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="48f2c-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="48f2c-132">如果選項不存在，就會將報告放在 C： \\ WiLogResults 目錄中。</span><span class="sxs-lookup"><span data-stu-id="48f2c-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="48f2c-133">以 UI 模式執行時，Wilogutl.exe 會顯示下列對話方塊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48f2c-134">Name</span><span class="sxs-lookup"><span data-stu-id="48f2c-134">Name</span></span></th>
<th><span data-ttu-id="48f2c-135">描述</span><span class="sxs-lookup"><span data-stu-id="48f2c-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48f2c-136">Windows Installer 詳細資訊記錄分析器</span><span class="sxs-lookup"><span data-stu-id="48f2c-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="48f2c-137">Windows Installer 詳細資訊記錄分析器] 對話方塊可讓使用者選取要分析的記錄檔：</span><span class="sxs-lookup"><span data-stu-id="48f2c-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="48f2c-138">[ <strong>開啟</strong> ] 按鈕會在 [記事本] 中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="48f2c-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="48f2c-139">您可以使用預覽區域來確認已選取正確的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="48f2c-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="48f2c-140">[ <strong>分析</strong> ] 按鈕會開始記錄檔分析，並顯示詳細的 [記錄檔] 視圖對話方塊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48f2c-141">詳細記錄檔視圖</span><span class="sxs-lookup"><span data-stu-id="48f2c-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="48f2c-142">[詳細記錄檔視圖] 對話方塊會顯示記錄的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="48f2c-143">使用 [<strong>上</strong><strong>一步] 和 [下一步]</strong>按鈕，流覽多個錯誤。</span><span class="sxs-lookup"><span data-stu-id="48f2c-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="48f2c-144">若要顯示非嚴重錯誤，請選取 [ <strong>顯示忽略的調試錯誤</strong> ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="48f2c-145">系統會顯示用來執行記錄安裝之電腦上的安裝程式版本。</span><span class="sxs-lookup"><span data-stu-id="48f2c-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="48f2c-146">如果使用較高的許可權來執行已記錄的安裝，則會選取 [提高許可權的 <strong>安裝</strong> ] 核取方塊，並在 [ <strong>用戶端許可權詳細資料</strong> ] 和 [ <strong>伺服器端許可權詳細資料</strong> ] 文字方塊中提供資訊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="48f2c-147">[詳細記錄檔視圖] 對話方塊包含下列按鈕：</span><span class="sxs-lookup"><span data-stu-id="48f2c-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="48f2c-148"><strong>狀態</strong> - 顯示 [功能和元件狀態] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="48f2c-149"><strong>屬性</strong> - 顯示 [屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="48f2c-150"><strong>原則</strong> - 顯示 [原則] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="48f2c-151"><strong>HTML 批註記錄</strong> - 檔將記錄顯示為批註的 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="48f2c-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="48f2c-152"><strong>儲存結果</strong> - 將報表檔案儲存至指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="48f2c-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="48f2c-153"><strong>錯誤訊息</strong> - 說明顯示安裝程式錯誤訊息說明。</span><span class="sxs-lookup"><span data-stu-id="48f2c-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="48f2c-154"><strong></strong>說明 -顯示 Windows Installer 安裝程式記錄分析器的說明。</span><span class="sxs-lookup"><span data-stu-id="48f2c-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="48f2c-155"><strong>如何讀取記錄</strong> - 檔顯示記錄檔說明文件。</span><span class="sxs-lookup"><span data-stu-id="48f2c-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48f2c-156">功能和元件狀態</span><span class="sxs-lookup"><span data-stu-id="48f2c-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="48f2c-157">[ <strong>功能和元件狀態</strong> ] 對話方塊會顯示功能和元件的狀態：</span><span class="sxs-lookup"><span data-stu-id="48f2c-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="48f2c-158">[ <strong>功能</strong> ] 欄會顯示安裝套件中的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="48f2c-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="48f2c-159">[ <strong>元件</strong> ] 欄會顯示安裝套件中的元件名稱。</span><span class="sxs-lookup"><span data-stu-id="48f2c-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="48f2c-160">[ <strong>已安裝</strong> ] 欄會顯示安裝結束時的功能或元件狀態。</span><span class="sxs-lookup"><span data-stu-id="48f2c-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="48f2c-161">[ <strong>要求</strong> ] 欄會在安裝功能或元件的狀態時，顯示使用者的選取專案。</span><span class="sxs-lookup"><span data-stu-id="48f2c-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="48f2c-162">[ <strong>動作</strong> ] 欄會顯示安裝程式針對功能或元件所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="48f2c-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="48f2c-163">如需詳細資訊，請參閱 <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> 和 <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="48f2c-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48f2c-164">屬性</span><span class="sxs-lookup"><span data-stu-id="48f2c-164">Properties</span></span></td>
<td><span data-ttu-id="48f2c-165">[屬性] 對話方塊會在安裝結束時顯示 Windows Installer <a href="properties.md">屬性</a> 及其值。</span><span class="sxs-lookup"><span data-stu-id="48f2c-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="48f2c-166">您可以依名稱或依值排序屬性：</span><span class="sxs-lookup"><span data-stu-id="48f2c-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="48f2c-167">[ <strong>客戶</strong> 端] 索引標籤會顯示安裝的用戶端部分的屬性和值。</span><span class="sxs-lookup"><span data-stu-id="48f2c-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="48f2c-168">[ <strong>伺服器</strong> ] 索引標籤會顯示安裝期間伺服器部分的屬性和值。</span><span class="sxs-lookup"><span data-stu-id="48f2c-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="48f2c-169">[ <strong>嵌套</strong> ] 索引標籤會顯示任何 <a href="concurrent-installations.md">並行安裝</a>的屬性和值。</span><span class="sxs-lookup"><span data-stu-id="48f2c-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48f2c-170">原則</span><span class="sxs-lookup"><span data-stu-id="48f2c-170">Policies</span></span></td>
<td><span data-ttu-id="48f2c-171">[原則] 對話方塊會在安裝後顯示 <a href="system-policy.md">系統原則</a> 集：</span><span class="sxs-lookup"><span data-stu-id="48f2c-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="48f2c-172">針對原則設定 0 (零) 組值表示原則未啟用。</span><span class="sxs-lookup"><span data-stu-id="48f2c-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="48f2c-173">值 1 (1) 表示已啟用原則。</span><span class="sxs-lookup"><span data-stu-id="48f2c-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="48f2c-174">值為？</span><span class="sxs-lookup"><span data-stu-id="48f2c-174">A value of ?</span></span> <span data-ttu-id="48f2c-175"> (問號) 表示原則值不會記錄在記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="48f2c-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="48f2c-176">如果您需要的原則值不在記錄檔中，請嘗試使用 Regedit.exe 檢查電腦上的登錄機碼是否安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="48f2c-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="48f2c-177">報表檔案</span><span class="sxs-lookup"><span data-stu-id="48f2c-177">Report Files</span></span>

<span data-ttu-id="48f2c-178">在 [**詳細記錄檔視圖**] 對話方塊中執行無訊息模式分析或按一下 [**儲存結果**] 按鈕時，Windows Installer 安裝程式分析器] 工具會產生三個文字檔和一個 HTML 批註記錄檔。</span><span class="sxs-lookup"><span data-stu-id="48f2c-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="48f2c-179">下表將識別報表檔案中的名稱和內容。</span><span class="sxs-lookup"><span data-stu-id="48f2c-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="48f2c-180">Name</span><span class="sxs-lookup"><span data-stu-id="48f2c-180">Name</span></span>                      | <span data-ttu-id="48f2c-181">描述</span><span class="sxs-lookup"><span data-stu-id="48f2c-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f2c-182">logfilename \_summary.txt</span><span class="sxs-lookup"><span data-stu-id="48f2c-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="48f2c-183">摘要說明記錄檔。</span><span class="sxs-lookup"><span data-stu-id="48f2c-183">Summarizes the log file.</span></span> <span data-ttu-id="48f2c-184">列出詳細記錄檔視圖對話方塊和第一個錯誤所顯示的資訊。</span><span class="sxs-lookup"><span data-stu-id="48f2c-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="48f2c-185">logfilename \_errors.txt</span><span class="sxs-lookup"><span data-stu-id="48f2c-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="48f2c-186">識別錯誤的數目、錯誤和建議的解決方案。</span><span class="sxs-lookup"><span data-stu-id="48f2c-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="48f2c-187">此檔案會列出重大和非重大錯誤。</span><span class="sxs-lookup"><span data-stu-id="48f2c-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="48f2c-188">logfilename \_policies.txt</span><span class="sxs-lookup"><span data-stu-id="48f2c-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="48f2c-189">識別在安裝結束時設定的原則名稱和值，如同在 [原則] 對話方塊中所設定。</span><span class="sxs-lookup"><span data-stu-id="48f2c-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="48f2c-190">詳細資料 \_logfilename.htm</span><span class="sxs-lookup"><span data-stu-id="48f2c-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="48f2c-191">HTML 批註記錄，其中包含色彩編碼的圖例。</span><span class="sxs-lookup"><span data-stu-id="48f2c-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="48f2c-192">傳回值</span><span class="sxs-lookup"><span data-stu-id="48f2c-192">Return Values</span></span>

<span data-ttu-id="48f2c-193">如果傳遞了不正確命令列引數給無訊息模式作業，Wilogutl.exe 不會執行任何動作，且進程會傳回下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="48f2c-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="48f2c-194">值</span><span class="sxs-lookup"><span data-stu-id="48f2c-194">Value</span></span> | <span data-ttu-id="48f2c-195">意義</span><span class="sxs-lookup"><span data-stu-id="48f2c-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="48f2c-196">1</span><span class="sxs-lookup"><span data-stu-id="48f2c-196">1</span></span>     | <span data-ttu-id="48f2c-197">指定了錯誤的輸出目錄。</span><span class="sxs-lookup"><span data-stu-id="48f2c-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="48f2c-198">2</span><span class="sxs-lookup"><span data-stu-id="48f2c-198">2</span></span>     | <span data-ttu-id="48f2c-199">指定了不正確的記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="48f2c-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="48f2c-200">3</span><span class="sxs-lookup"><span data-stu-id="48f2c-200">3</span></span>     | <span data-ttu-id="48f2c-201">已通過/q，但缺少記錄檔名稱所需的參數/l。</span><span class="sxs-lookup"><span data-stu-id="48f2c-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="48f2c-202">4</span><span class="sxs-lookup"><span data-stu-id="48f2c-202">4</span></span>     | <span data-ttu-id="48f2c-203">傳遞了/l，但缺少安靜模式所需的參數/q。</span><span class="sxs-lookup"><span data-stu-id="48f2c-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="48f2c-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="48f2c-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48f2c-205">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="48f2c-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="48f2c-206">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="48f2c-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




