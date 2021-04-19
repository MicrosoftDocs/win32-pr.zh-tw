---
description: 適用于 Windows Installer 3.0 及更早版本之 msiexec.exe 的命令列選項。 提供顯示選項、參數和描述的表格。 顯示如何安裝產品和其他工作的範例。
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: 命令列選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fe56026c21e4120963c86b4de08decc85b2a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979268"
---
# <a name="command-line-options"></a>命令列選項

解釋封裝和安裝產品的可執行程式是 Msiexec.exe。 請注意，Msiexec 也會在傳回時會設定對應至 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)的錯誤層級。 命令列選項不區分大小寫。

下表中的命令列選項適用于 Windows Installer 3.0 及更早版本。 從 Windows Installer 3.0 開始也提供 [標準安裝程式 Command-Line 選項](standard-installer-command-line-options.md) 。



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
<td><strong>/I</strong></td>
<td><em>套件 |ProductCode</em></td>
<td>安裝或設定產品。<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p | o | e | d | c | a | u | m | s | v]<em>封裝</em> |<em>ProductCode</em></td>
<td>修復產品。 此選項會忽略在命令列上輸入的任何屬性值。 此選項的預設引數清單是 ' omus reinstall '。 此選項會共用與 <a href="reinstallmode.md"><strong>REINSTALLMODE</strong></a> 屬性相同的引數清單。<br/> p-只有在遺失檔案時才重新安裝。<br/> o-如果遺失檔案或已安裝較舊的版本，則重新安裝。<br/> e-如果遺失檔案或已安裝相同或較舊的版本，則重新安裝。<br/> d-如果遺失檔案或安裝不同的版本，請重新安裝。<br/> c-如果遺失檔案或儲存的總和檢查碼不符合計算值，則重新安裝。 只有<a href="file-table.md">在檔案資料表的</a>[屬性] 資料行中，修復具有<strong>msidbFileAttributesChecksum</strong>的檔案。<br/> a-強制重新安裝所有檔案。<br/> u-重寫所有必要的使用者特定登錄專案。<br/> m-重寫所有必要的電腦特定登錄專案。<br/> s-覆寫所有現有的快捷方式。<br/> v-從來源執行，然後重新快取本機封裝。 在第一次安裝應用程式或功能時，請勿使用 [ <strong>v</strong> 重新安裝] 選項。<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>套件</em></td>
<td><a href="administrative-installation.md">系統管理安裝</a> 選項。 在網路上安裝產品。<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>套件 |ProductCode</em></td>
<td>卸載產品。</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u | m]<em>Packageor</em><br/> [u | m]<em>封裝</em><strong>/t</strong><em>轉換清單</em><br/> <em>or</em><br/> [u | m]<em>封裝</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>通告產品。 此選項會忽略在命令列上輸入的任何屬性值。<br/> u-通告給目前的使用者。<br/> m-通告給電腦的所有使用者。<br/> g 語言識別項。<br/> t-將轉換套用至已公告的封裝。<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i | w | e | a | r | u | c | m | o | p | v | x | + |！ |*] <em>Logfile</em></td>
<td>將記錄資訊寫入指定之現有路徑的記錄檔。 記錄檔位置的路徑必須已經存在。 安裝程式不會建立記錄檔的目錄結構。 旗標會指出要記錄哪些資訊。 如果未指定旗標，則預設值為 ' iwearmo '。<br/> i-狀態訊息。<br/> w-非嚴重警告。<br/> e-所有錯誤訊息。<br/> 動作的啟動。<br/> r-動作特定的記錄。<br/> u-使用者要求。<br/> c-初始 UI 參數。<br/> m-記憶體不足或嚴重的離開資訊。<br/> o-磁碟空間不足的訊息。<br/> p-終端機屬性。<br/> v-Verbose 輸出。<br/> x-額外的調試資訊。 <strong>Windows Installer 2.0：</strong> 不支援。 X 選項可 Windows Installer 3.0.3790.2180 版和更新版本中使用。<br/> <br/> + - 附加至現有的檔案。<br/> ! -將每一行排清到記錄檔。<br/> &quot;*&quot; -萬用字元，記錄除了 v 和 x 選項以外的所有資訊。若要包含 v 和 x 選項，請指定 &quot; /l* vx &quot; 。<br/>
<blockquote>
[!Note]<br />
如需可用於設定記錄模式之所有方法的詳細資訊，請參閱<a href="windows-installer-logging.md">Windows Installer 記錄</a>區段中的<a href="normal-logging.md">一般記錄</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>一樣</strong></td>
<td><em>檔案名</em>
<blockquote>
[!Note]<br />
<em>檔案名</em>的長度不能超過8個字元。
</blockquote>
<br/></td>
<td>產生 SMS 狀態的 mif 檔案。 必須與安裝 (-i) 一起使用、移除 ( x) 、系統管理安裝 (-a) ，或重新安裝 (-f) 選項。 ISMIF32.DLL 會安裝為 SMS 的一部分，而且必須在路徑上。<br/> 狀態 mif 檔案的欄位會填入下列資訊：<br/> 製造商- <a href="author-summary.md"><strong>作者</strong></a><br/> 產品 <a href="revision-number-summary.md"><strong>修訂編號</strong></a><br/> 版本- <a href="subject-summary.md"> <strong></strong>主旨</a><br/> 地區設定 <a href="template-summary.md"><strong>範本</strong></a><br/> 序號-未設定<br/> 安裝-由 ISMIF32.DLL 設定為 &quot; DateTime&quot;<br/> InstallStatus- &quot; 成功 &quot; 或 &quot; 失敗&quot;<br/> 描述-依下列順序的錯誤訊息： 1) 安裝程式所產生的錯誤訊息。 如果安裝無法開始或使用者結束，則會從 Msi.dll 2) 資源。 3) 系統錯誤訊息檔。 4) 格式的訊息： &quot; 安裝程式錯誤% i &quot; ，其中% i 是從 Msi.dll 傳回的錯誤。<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage [;P atchpackage2</em> ]</td>
<td>套用修補程式。 若要將修補程式套用至已安裝的系統管理映射，您必須合併下列選項：<br/> /p <em> <PatchPackage> [;p atchpackage2] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n | b | r | f</td>
<td>設定 <a href="user-interface-levels.md">使用者介面層級</a>。<br/> 問： qn-沒有 UI<br/> qb- <a href="b-gly.md"><em>基本 UI</em></a>。 使用 qb！ 隱藏 [ <strong>取消</strong> ] 按鈕。<br/> 在安裝結束時，不顯示任何強制回應對話方塊的 qr <a href="r-gly.md"><em>減少 UI</em></a> 。<br/> qf- <a href="f-gly.md"><em>完整 UI</em></a> 和任何撰寫的 <a href="fatalerror-dialog.md">FatalError</a>、 <a href="userexit-dialog.md">UserExit</a>或 <a href="exit-dialog.md">結束</a> 強制回應對話方塊。<br/> qn +-沒有 UI，除了顯示于結尾的強制回應對話方塊。<br/> qb +- <a href="b-gly.md"><em>基本 UI</em></a> ，並在結尾顯示模式對話方塊。 如果使用者取消安裝，就不會顯示模式方塊。 使用 qb +！ 或 qb！ + 隱藏 [ <strong>取消</strong> ] 按鈕。<br/> qb--沒有強制回應對話方塊的 <a href="b-gly.md"><em>基本 UI</em></a> 。 請注意，/qb + 不是支援的 UI 層級。 使用 qb-！ 或 qb！-隱藏 [ <strong>取消</strong> ] 按鈕。<br/> 請注意！ 選項適用于 Windows Installer 2.0，且僅適用于基本 UI。 它對完整的 UI 而言是不正確。<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> 或 <strong>/h</strong></td>
<td> </td>
<td>顯示 Windows Installer 的著作權資訊。<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>模組</em></td>
<td>呼叫系統函數 <strong>DllRegisterServer</strong> ，以在命令列上傳遞的自我註冊模組。 指定 DLL 的完整路徑。 例如，針對目前資料夾中的 MY_FILE.DLL，您可以使用：<br/> <strong>msiexec/y .\MY_FILE.DLL</strong><br/> 此選項只會用於無法使用 .msi 檔案的登錄資料表新增的登錄資訊。<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>模組</em></td>
<td>呼叫系統函數 <strong>DllUnRegisterServer</strong> ，以取消註冊命令列上所傳入的模組。 指定 DLL 的完整路徑。 例如，針對目前資料夾中的 MY_FILE.DLL，您可以使用： <br/> <strong>msiexec/z .\MY_FILE.DLL</strong><br/> 此選項只會用於無法使用 .msi 檔案的登錄表移除的登錄資訊。<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>通告產品的新實例。 必須搭配/t 使用 從 Windows Server 2003 和 Windows XP Service Pack 1 隨附的 Windows Installer 版本開始提供 (SP1) 。<br/></td>
</tr>
<tr class="even">
<td><strong>n</strong></td>
<td><em>ProductCode</em></td>
<td>指定產品的特定實例。 用來透過產品程式碼變更轉換，來識別使用多重實例支援所安裝的實例。 從隨附于 Windows Server 2003 和 Windows XP SP1 的 Windows Installer 版本開始提供。 <br/></td>
</tr>
</tbody>
</table>



 

Options/i、/x、/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] 、/j \[ u \| m \] 、/a、/p、/y 和/z 不應一起使用。 這項規則的唯一例外是修補 [系統管理安裝](administrative-installation.md) 需要同時使用/p 和/a /T、/c 和/g 選項只能與/j. 搭配使用 /L 和/q 選項可以搭配/i、/x、/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] 、/j \[ u \| m \] 、/a 和/p 使用。 選項/n 可搭配/i、/f、/x 和/p 使用

若要從：Example.msi 安裝產品 \\ ，請安裝產品，如下所示：

**msiexec/i A： \\Example.msi**

您只能使用命令列來修改 [公用屬性](public-properties.md) 。 命令列上的所有屬性名稱都會轉譯為大寫，但值會保留區分大小寫。 如果您在命令列中輸入 **MyProperty** ，安裝程式會覆寫 MyProperty 的值，而不是屬性工作表中 **MyProperty** 的值。 如需詳細資訊，請參閱 [關於屬性](about-properties.md)。

若要安裝屬性設定為 VALUE 的產品，請在命令列上使用下列語法。 您可以將屬性放在選項和其引數以外的任何位置。

正確的語法：

**msiexec/i A： \\Example.msi PROPERTY = VALUE**

語法不正確：

**msiexec/i PROPERTY = VALUE A： \\Example.msi**

屬於常值字串的屬性值必須以引號括住。 在這些標記之間的字串中包含任何空白字元。

**msiexec/i A： \\Example.msi PROPERTY = "內嵌式空白字元"**

若要使用命令列清除公用屬性，請將其值設定為空字串。

**msiexec/i A： \\Example.msi PROPERTY = ""**

針對以文字引號分隔的文字區段，使用第二組引號括住區段。

**msiexec/i A： \\Example.msi PROPERTY = "Embedded" "引號" "空白字元"**

下列範例顯示覆雜的命令列。

**msiexec/i testdb.msi INSTALLLEVEL = 3/l \* msi. log 的名稱 = "Acme" "widget" "和" "Gizmos" ""**

下列範例顯示公告選項。 請注意，參數不區分大小寫。

**msiexec/JM msisample.msi/T 轉換。 mst/LIME logfile.txt**

下列範例示範如何安裝要公告之產品的新實例。 這項產品的撰寫是為了支援多個實例轉換。

**msiexec/JM msisample.msi/T： instance1 .mst; 自訂 .mst/c/LIME logfile.txt**

下列範例示範如何修補使用多個實例轉換所安裝之產品的實例。

**msiexec/p msipatch .msp; msipatch2 .msp/n {00000001-0002-0000-0000-624474736554} /qb**

當您將修補程式套用至特定產品時，不能在命令列中同時指定/i 和/p 選項。 在此情況下，您可以將修補程式套用至產品，如下所示。

**msiexec/i A： \\Example.msi PATCH = msipatch .msp; msipatch2 .msp/qb**

使用/p 選項時，無法在命令列中設定 [**PATCH**](patch.md) 屬性。 如果在使用/p 選項時設定 **patch** 屬性， **patch** 屬性的值會被忽略並覆寫。

 

