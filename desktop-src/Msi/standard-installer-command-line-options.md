---
描述： Msiexec.exe 解釋封裝和安裝產品的可執行程式。注意 Msiexec 也會在傳回時會設定對應至系統錯誤碼的錯誤層級。 下表識別此程式的標準命令列選項。 命令列選項不區分大小寫。Windows Installer 2.0：從 Windows Installer 3.0 開始，可以使用本主題中所識別的命令列選項。 Windows Installer Command-Line 選項適用于 Windows Installer&\# 160、3.0 及更早版本。
assetid： b1707c88-1cca-45ab-bb23-6002bfd5204e title：標準安裝程式 Command-Line 選項 ms. 主題：文章 ms. 日期：05/31/2018
---

# <a name="standard-installer-command-line-options"></a>標準安裝程式 Command-Line 選項

解釋封裝和安裝產品的可執行程式是 Msiexec.exe。

> [!Note]  
> Msiexec 也會在傳回時設定對應至 [系統錯誤碼](../debug/system-error-codes.md)的錯誤層級。

 

下表識別此程式的標準命令列選項。 命令列選項不區分大小寫。

**Windows Installer 2.0：** 從 Windows Installer 3.0 開始，可以使用本主題中所識別的命令列選項。 Windows Installer 的 [命令列選項](command-line-options.md) 可用於 Windows Installer 3.0 及更早版本。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>參數</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/help</strong></td>
<td> </td>
<td>說明和快速參考選項。 顯示安裝命令的正確用法，包括所有參數和行為的清單。 使用方式的描述可顯示在使用者介面中。 不當使用任何選項時，會叫用這個說明選項。<br/> 範例： <strong>msiexec/help</strong><br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/？</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>無訊息顯示選項。 安裝程式會執行安裝，而不顯示使用者介面。 使用者不會看到任何提示、訊息或對話方塊。 使用者無法取消安裝。 使用 <strong>/norestart</strong> 或 <strong>/forcerestart</strong> 標準命令列選項來控制重新開機。 如果未指定任何重新開機選項，安裝程式會在必要時重新開機電腦，而不會向使用者顯示任何提示或警告。<br/> 範例： <br/> <strong>msiexec/package Application.msi/quiet</strong><br/> <strong>Msiexec/uninstall Application.msi/quiet</strong><br/> <strong>Msiexec/update msipatch .msp/quiet</strong><br/> <strong>Msiexec/uninstall msipatch .msp/package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/qn</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>被動式顯示選項。 安裝程式會向使用者顯示進度列，指出正在進行安裝，但不會向使用者顯示任何提示或錯誤訊息。 使用者無法取消安裝。 使用 <strong>/norestart</strong> 或 <strong>/forcerestart</strong> 標準命令列選項來控制重新開機。 如果未指定任何重新開機選項，安裝程式會在必要時重新開機電腦，而不會向使用者顯示任何提示或警告。 <br/> 範例： <strong>msiexec/package Application.msi/passive</strong> <br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/qb！-</strong> 在命令列上設定 <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>永不重新開機選項。 安裝程式在安裝後永遠不會重新開機電腦。<br/> 範例： msiexec/package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer 命令列具有在命令列上設定的 <a href="reboot.md"><strong>重新開機</strong></a>= ReallySuppress。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>一律重新開機選項。 安裝程式一律會在每次安裝之後重新開機電腦。<br/> 範例： msiexec/package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer 命令列具有 <a href="reboot.md"><strong>重新開機</strong></a>= 強制設定在命令列上。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>在重新開機選項之前提示。 顯示需要重新開機才能完成安裝的訊息，並詢問使用者是否要立即重新開機系統。 此選項不能與 <strong>/quiet</strong> 選項一起使用。<br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer 命令列<a href="rebootprompt.md"><strong></strong></a>已  =  &quot; &quot; 在命令列上設定 REBOOTPROMPT。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>卸載產品選項。 卸載產品。<br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 是 <strong>/x</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [;Update2 .msp |PatchGUID2]</em></td>
<td>卸載更新選項。 卸載更新修補程式。<br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 是 <strong>/i</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= Update1 .msp |PatchGUID1[;Update2 .msp |PatchGUID2]，在命令列上設定。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Log 選項。 將記錄資訊寫入指定之現有路徑的記錄檔。 記錄檔位置的路徑必須已經存在。 安裝程式不會建立記錄檔的目錄結構。<br/> 記錄檔中會輸入下列資訊：<br/>
<ul>
<li>狀態訊息</li>
<li>非嚴重警告</li>
<li>所有錯誤訊息</li>
<li>啟動動作</li>
<li>動作特定記錄</li>
<li>使用者要求</li>
<li>初始 UI 參數</li>
<li>記憶體不足或嚴重的離開資訊</li>
<li>磁碟空間不足的訊息</li>
<li>終端機屬性</li>
</ul>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 為 <strong>/l *</strong>。
</blockquote>
<br/>
<blockquote>
[!Note]<br />
如需可用於設定記錄模式之所有方法的詳細資訊，請參閱<a href="windows-installer-logging.md">Windows Installer 記錄</a>] 區段中的<a href="normal-logging.md">一般記錄</a>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>安裝產品選項。 安裝或設定產品。<br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer <a href="command-line-options.md">命令列選項</a> 是 <strong>/i</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/update</strong></td>
<td><em><Update1.msp>[;Update2 .msp]</em></td>
<td>安裝修補程式選項。 安裝一或多個修補程式。 <br/>
<blockquote>
[!Note]<br />
對等的 Windows Installer 命令列具有 <a href="patch.md"><strong>PATCH</strong></a> = [msipatch .msp] <;PatchGuid2> 在命令列上設定。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
