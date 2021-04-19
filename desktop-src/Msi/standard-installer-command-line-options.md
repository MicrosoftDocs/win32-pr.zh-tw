---
<span data-ttu-id="de814-101">描述： Msiexec.exe 解釋封裝和安裝產品的可執行程式。注意 Msiexec 也會在傳回時會設定對應至系統錯誤碼的錯誤層級。</span><span class="sxs-lookup"><span data-stu-id="de814-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="de814-102">下表識別此程式的標準命令列選項。</span><span class="sxs-lookup"><span data-stu-id="de814-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="de814-103">命令列選項不區分大小寫。Windows Installer 2.0：從 Windows Installer 3.0 開始，可以使用本主題中所識別的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="de814-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="de814-104">Windows Installer Command-Line 選項適用于 Windows Installer&\# 160、3.0 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="de814-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="de814-105">assetid： b1707c88-1cca-45ab-bb23-6002bfd5204e title：標準安裝程式 Command-Line 選項 ms. 主題：文章 ms. 日期：05/31/2018</span><span class="sxs-lookup"><span data-stu-id="de814-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="de814-106">標準安裝程式 Command-Line 選項</span><span class="sxs-lookup"><span data-stu-id="de814-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="de814-107">解釋封裝和安裝產品的可執行程式是 Msiexec.exe。</span><span class="sxs-lookup"><span data-stu-id="de814-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="de814-108">Msiexec 也會在傳回時設定對應至 [系統錯誤碼](../debug/system-error-codes.md)的錯誤層級。</span><span class="sxs-lookup"><span data-stu-id="de814-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="de814-109">下表識別此程式的標準命令列選項。</span><span class="sxs-lookup"><span data-stu-id="de814-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="de814-110">命令列選項不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="de814-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="de814-111">**Windows Installer 2.0：** 從 Windows Installer 3.0 開始，可以使用本主題中所識別的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="de814-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="de814-112">Windows Installer 的 [命令列選項](command-line-options.md) 可用於 Windows Installer 3.0 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="de814-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de814-113">選項</span><span class="sxs-lookup"><span data-stu-id="de814-113">Option</span></span></th>
<th><span data-ttu-id="de814-114">參數</span><span class="sxs-lookup"><span data-stu-id="de814-114">Parameters</span></span></th>
<th><span data-ttu-id="de814-115">意義</span><span class="sxs-lookup"><span data-stu-id="de814-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de814-116"><strong>/help</strong></span><span class="sxs-lookup"><span data-stu-id="de814-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="de814-117">說明和快速參考選項。</span><span class="sxs-lookup"><span data-stu-id="de814-117">Help and quick reference option.</span></span> <span data-ttu-id="de814-118">顯示安裝命令的正確用法，包括所有參數和行為的清單。</span><span class="sxs-lookup"><span data-stu-id="de814-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="de814-119">使用方式的描述可顯示在使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="de814-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="de814-120">不當使用任何選項時，會叫用這個說明選項。</span><span class="sxs-lookup"><span data-stu-id="de814-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="de814-121">範例： <strong>msiexec/help</strong></span><span class="sxs-lookup"><span data-stu-id="de814-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-122">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/？</strong>。</span><span class="sxs-lookup"><span data-stu-id="de814-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de814-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="de814-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="de814-124">無訊息顯示選項。</span><span class="sxs-lookup"><span data-stu-id="de814-124">Quiet display option.</span></span> <span data-ttu-id="de814-125">安裝程式會執行安裝，而不顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="de814-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="de814-126">使用者不會看到任何提示、訊息或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="de814-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="de814-127">使用者無法取消安裝。</span><span class="sxs-lookup"><span data-stu-id="de814-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="de814-128">使用 <strong>/norestart</strong> 或 <strong>/forcerestart</strong> 標準命令列選項來控制重新開機。</span><span class="sxs-lookup"><span data-stu-id="de814-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="de814-129">如果未指定任何重新開機選項，安裝程式會在必要時重新開機電腦，而不會向使用者顯示任何提示或警告。</span><span class="sxs-lookup"><span data-stu-id="de814-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="de814-130">範例：</span><span class="sxs-lookup"><span data-stu-id="de814-130">Examples:</span></span> <br/> <span data-ttu-id="de814-131"><strong>msiexec/package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="de814-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="de814-132"><strong>Msiexec/uninstall Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="de814-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="de814-133"><strong>Msiexec/update msipatch .msp/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="de814-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="de814-134"><strong>Msiexec/uninstall msipatch .msp/package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="de814-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-135">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/qn</strong>。</span><span class="sxs-lookup"><span data-stu-id="de814-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de814-136"><strong>/passive</strong></span><span class="sxs-lookup"><span data-stu-id="de814-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="de814-137">被動式顯示選項。</span><span class="sxs-lookup"><span data-stu-id="de814-137">Passive display option.</span></span> <span data-ttu-id="de814-138">安裝程式會向使用者顯示進度列，指出正在進行安裝，但不會向使用者顯示任何提示或錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="de814-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="de814-139">使用者無法取消安裝。</span><span class="sxs-lookup"><span data-stu-id="de814-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="de814-140">使用 <strong>/norestart</strong> 或 <strong>/forcerestart</strong> 標準命令列選項來控制重新開機。</span><span class="sxs-lookup"><span data-stu-id="de814-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="de814-141">如果未指定任何重新開機選項，安裝程式會在必要時重新開機電腦，而不會向使用者顯示任何提示或警告。</span><span class="sxs-lookup"><span data-stu-id="de814-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="de814-142">範例： <strong>msiexec/package Application.msi/passive</strong> </span><span class="sxs-lookup"><span data-stu-id="de814-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-143">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/qb！-</strong> 在命令列上設定 <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S。</span><span class="sxs-lookup"><span data-stu-id="de814-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de814-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="de814-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="de814-145">永不重新開機選項。</span><span class="sxs-lookup"><span data-stu-id="de814-145">Never restart option.</span></span> <span data-ttu-id="de814-146">安裝程式在安裝後永遠不會重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="de814-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="de814-147">範例： msiexec/package Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="de814-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-148">對等的 Windows Installer 命令列具有在命令列上設定的 <a href="reboot.md"><strong>重新開機</strong></a>= ReallySuppress。</span><span class="sxs-lookup"><span data-stu-id="de814-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de814-149"><strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="de814-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="de814-150">一律重新開機選項。</span><span class="sxs-lookup"><span data-stu-id="de814-150">Always restart option.</span></span> <span data-ttu-id="de814-151">安裝程式一律會在每次安裝之後重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="de814-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="de814-152">範例： msiexec/package Application.msi <strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="de814-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-153">對等的 Windows Installer 命令列具有 <a href="reboot.md"><strong>重新開機</strong></a>= 強制設定在命令列上。</span><span class="sxs-lookup"><span data-stu-id="de814-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de814-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="de814-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="de814-155">在重新開機選項之前提示。</span><span class="sxs-lookup"><span data-stu-id="de814-155">Prompt before restarting option.</span></span> <span data-ttu-id="de814-156">顯示需要重新開機才能完成安裝的訊息，並詢問使用者是否要立即重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="de814-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="de814-157">此選項不能與 <strong>/quiet</strong> 選項一起使用。</span><span class="sxs-lookup"><span data-stu-id="de814-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-158">對等的 Windows Installer 命令列<a href="rebootprompt.md"><strong></strong></a>已  =  &quot; &quot; 在命令列上設定 REBOOTPROMPT。</span><span class="sxs-lookup"><span data-stu-id="de814-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de814-159"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="de814-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="de814-160">卸載產品選項。</span><span class="sxs-lookup"><span data-stu-id="de814-160">Uninstall product option.</span></span> <span data-ttu-id="de814-161">卸載產品。</span><span class="sxs-lookup"><span data-stu-id="de814-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-162">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 是 <strong>/x</strong>。</span><span class="sxs-lookup"><span data-stu-id="de814-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de814-163"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="de814-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="de814-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [;Update2 .msp |PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="de814-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="de814-165">卸載更新選項。</span><span class="sxs-lookup"><span data-stu-id="de814-165">Uninstall update option.</span></span> <span data-ttu-id="de814-166">卸載更新修補程式。</span><span class="sxs-lookup"><span data-stu-id="de814-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-167">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 是 <strong>/i</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= Update1 .msp |PatchGUID1[;Update2 .msp |PatchGUID2]，在命令列上設定。</span><span class="sxs-lookup"><span data-stu-id="de814-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de814-168"><strong>/log</strong></span><span class="sxs-lookup"><span data-stu-id="de814-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="de814-169">Log 選項。</span><span class="sxs-lookup"><span data-stu-id="de814-169">Log option.</span></span> <span data-ttu-id="de814-170">將記錄資訊寫入指定之現有路徑的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="de814-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="de814-171">記錄檔位置的路徑必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="de814-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="de814-172">安裝程式不會建立記錄檔的目錄結構。</span><span class="sxs-lookup"><span data-stu-id="de814-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="de814-173">記錄檔中會輸入下列資訊：</span><span class="sxs-lookup"><span data-stu-id="de814-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="de814-174">狀態訊息</span><span class="sxs-lookup"><span data-stu-id="de814-174">Status messages</span></span></li>
<li><span data-ttu-id="de814-175">非嚴重警告</span><span class="sxs-lookup"><span data-stu-id="de814-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="de814-176">所有錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="de814-176">All error messages</span></span></li>
<li><span data-ttu-id="de814-177">啟動動作</span><span class="sxs-lookup"><span data-stu-id="de814-177">Start up of actions</span></span></li>
<li><span data-ttu-id="de814-178">動作特定記錄</span><span class="sxs-lookup"><span data-stu-id="de814-178">Action-specific records</span></span></li>
<li><span data-ttu-id="de814-179">使用者要求</span><span class="sxs-lookup"><span data-stu-id="de814-179">User requests</span></span></li>
<li><span data-ttu-id="de814-180">初始 UI 參數</span><span class="sxs-lookup"><span data-stu-id="de814-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="de814-181">記憶體不足或嚴重的離開資訊</span><span class="sxs-lookup"><span data-stu-id="de814-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="de814-182">磁碟空間不足的訊息</span><span class="sxs-lookup"><span data-stu-id="de814-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="de814-183">終端機屬性</span><span class="sxs-lookup"><span data-stu-id="de814-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-184">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/l \*</strong>。</span><span class="sxs-lookup"><span data-stu-id="de814-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-185">如需可用於設定記錄模式之所有方法的詳細資訊，請參閱<a href="windows-installer-logging.md">Windows Installer 記錄</a>] 區段中的<a href="normal-logging.md">一般記錄</a>。</span><span class="sxs-lookup"><span data-stu-id="de814-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de814-186"><strong>/package</strong></span><span class="sxs-lookup"><span data-stu-id="de814-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="de814-187">安裝產品選項。</span><span class="sxs-lookup"><span data-stu-id="de814-187">Install product option.</span></span> <span data-ttu-id="de814-188">安裝或設定產品。</span><span class="sxs-lookup"><span data-stu-id="de814-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-189">對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 是 <strong>/i</strong>。</span><span class="sxs-lookup"><span data-stu-id="de814-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de814-190"><strong>/update</strong></span><span class="sxs-lookup"><span data-stu-id="de814-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="de814-191"><em><Update1.msp>[;Update2 .msp]</em></span><span class="sxs-lookup"><span data-stu-id="de814-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="de814-192">安裝修補程式選項。</span><span class="sxs-lookup"><span data-stu-id="de814-192">Install patches option.</span></span> <span data-ttu-id="de814-193">安裝一或多個修補程式。</span><span class="sxs-lookup"><span data-stu-id="de814-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de814-194">對等的 Windows Installer 命令列具有 <a href="patch.md"><strong>PATCH</strong></a> = [msipatch .msp] <;PatchGuid2> 在命令列上設定。</span><span class="sxs-lookup"><span data-stu-id="de814-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
