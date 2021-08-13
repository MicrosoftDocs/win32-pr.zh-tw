---
description: Windows事件可為應用程式提供標準、集中式的方式 (以及記錄重要軟體和硬體事件的作業系統) 。
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: '事件記錄 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c1aa4808727a220ec104cb3e7bfdff2741dcb2366ca1468288a082baab813b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636922"
---
# <a name="event-logging-windows-installer"></a>事件記錄 (Windows Installer) 

[Windows 事件](../events/windows-events.md)提供一個標準、集中的方式，讓應用程式 (和作業系統) 記錄重要的軟體和硬體事件。 事件記錄服務會將來自各種來源的事件儲存在稱為 *事件記錄* 檔的單一集合中。 在 Windows Vista 之前，您可以使用 Windows (ETW) 或[事件記錄](../eventlog/event-logging.md)[的事件追蹤](../etw/event-tracing-portal.md)來記錄事件。 WindowsVista 引進了一種新的事件模型，可統一 ETW 和[Windows 事件記錄](../wes/windows-event-log.md)檔 API。

安裝程式也會將專案寫入事件記錄檔。 這些會記錄事件，如下所示：

-   安裝成功或失敗;移除或修復產品。
-   產品設定期間所發生的錯誤。
-   偵測損毀的設定資料。

如果寫入大量的資訊，事件記錄檔可能會被填滿，且安裝程式會顯示「應用程式記錄檔已滿」訊息。

安裝程式可能會在事件記錄檔中寫入下列專案。 所有事件記錄檔訊息都有唯一的事件識別碼。 在 [錯誤資料表](error-table.md) 中，針對失敗的安裝所傳回的所有一般錯誤都會記錄在應用程式事件記錄檔中，且訊息識別碼等於錯誤 + 10000。 例如，成功完成安裝錯誤資料表中的錯誤號碼為1707。 成功的安裝會記錄在應用程式事件記錄檔中，訊息識別碼為 11707 (1707 + 10000) 。

如需如何在針對部署進行疑難排解時，在使用者電腦上啟用詳細資訊記錄的詳細資訊，請參閱[Windows Installer 的最佳做法](windows-installer-best-practices.md)。



<table>
<thead>
<tr class="header">
<th>事件識別碼</th>
<th>訊息</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>在元件 ' %3 ' 的要求期間，偵測到產品 ' %1 '，功能 ' %2 ' 失敗</td>
<td>警告訊息。 如需詳細資訊，請參閱 <a href="searching-for-a-broken-feature-or-component.md">搜尋中斷的功能或元件</a>。</td>
</tr>
<tr class="even">
<td>1002</td>
<td> (名稱： ' %1 '，值： ' %2 ' ) 在索引鍵 ' %3 ' 中的非預期或遺漏值</td>
<td>出現非預期或遺漏值的錯誤訊息。</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>機碼 ' %2 ' 中有非預期或遺漏的子機碼 ' %1 '</td>
<td>出現非預期或遺漏子機碼的錯誤訊息。</td>
</tr>
<tr class="even">
<td>1004</td>
<td>偵測產品 ' %1 '，功能 ' %2 '，元件 ' %3 ' 失敗<strong>：</strong>從 Windows Installer 版本2.0 開始，此訊息為：產品 ' %1 '，功能 ' %2 '，元件 ' %3 ' 的偵測失敗。 資源 ' %4 ' 不存在。<br/></td>
<td>警告訊息。 另請參閱 <a href="searching-for-a-broken-feature-or-component.md">搜尋中斷的功能或元件</a>。</td>
</tr>
<tr class="odd">
<td>1005</td>
<td>安裝作業起始重新開機</td>
<td>安裝程式起始系統重新開機的告知性訊息。</td>
</tr>
<tr class="even">
<td>1006</td>
<td>無法對封包 ' %1 ' 的數位簽章進行驗證。 WinVerifyTrust 無法在電腦上使用。</td>
<td>警告訊息。 在 <a href="msidigitalsignature-table.md">MsiDigitalSignature 資料表</a> 中撰寫的封包會執行 <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust</strong></a> 檢查。 因為電腦未安裝適當的加密 Dll，所以無法執行此動作。</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>軟體限制原則不允許安裝 %1。 Windows Installer 只允許執行不受限制的專案。 軟體限制原則所傳回的授權層級為 %2。</td>
<td>指出系統管理員已將軟體限制原則設定為不允許此安裝的錯誤訊息。</td>
</tr>
<tr class="even">
<td>1008</td>
<td>因為軟體限制原則處理中發生錯誤，所以不允許安裝 %1。 無法信任物件。</td>
<td>一則錯誤訊息，指出嘗試根據軟體限制原則驗證封裝時發生問題。</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>此版本的 Windows 不支援部署64位套件。 腳本 ' %1 ' 適用于64位封裝。</td>
<td>錯誤訊息，指出64位封裝的腳本只能在64位電腦上執行。</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{未處理的例外狀況報告}</td>
<td>未處理之例外狀況的錯誤訊息，這是報表。</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows未正確註冊安裝程式 proxy 資訊</td>
<td>未正確註冊 proxy 資訊的錯誤訊息。</td>
</tr>
<tr class="even">
<td>1015</td>
<td>無法連接到伺服器。 錯誤：% d</td>
<td>安裝無法連接到伺服器的參考訊息。</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>偵測產品 ' %1 '、功能 ' %2 '、元件 ' %3 ' 失敗。 找不到來源來源元件中的資源 ' %4 '，因為找不到有效且可存取的來源。</td>
<td>警告訊息。 如需詳細資訊，請參閱 <a href="searching-for-a-broken-feature-or-component.md">搜尋中斷的功能或元件</a>。</td>
</tr>
<tr class="even">
<td>1017</td>
<td>使用者 SID 已從 ' %1 ' 變更為 ' %2 '，但無法更新受管理的應用程式和使用者資料金鑰。 錯誤 = ' %3 '。</td>
<td>錯誤訊息，表示嘗試在使用者的 SID 變更後更新使用者的註冊時發生錯誤。</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>無法安裝應用程式 ' %1 '，因為它與此版本的 Windows 不相容。</td>
<td>錯誤訊息，表示安裝與目前正在執行的 Windows 版本不相容。 請洽詢所安裝軟體的製造商以取得更新。</td>
</tr>
<tr class="even">
<td>1019</td>
<td>產品： %1-已成功移除更新 ' %2 '。</td>
<td>安裝程式已移除更新的告知性訊息。<strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>產品： %1-無法移除更新 ' %2 '。 錯誤碼 %3。 記錄檔 %4 中有其他資訊可供使用。</td>
<td>錯誤訊息，表示安裝程式無法移除更新。 記錄檔中會提供其他資訊。<strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>產品： %1-無法移除更新 ' %2 '。 錯誤碼 %3。</td>
<td>錯誤訊息，表示安裝程式無法移除更新。 如需有關如何開啟記錄的詳細資訊，請參閱針對<a href="windows-installer-best-practices.md">部署進行疑難排解時，在使用者的電腦上啟用詳細資訊記錄。</a><strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>產品： %1-已成功安裝更新 ' %2 '。</td>
<td>安裝程式已成功安裝更新的告知性訊息。 <strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>產品： %1-無法安裝更新 ' %2 '。 錯誤碼 %3。 記錄檔 %4 中有其他資訊可供使用。</td>
<td>指出安裝程式無法安裝更新的錯誤訊息。 記錄檔中會提供其他資訊。<strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>產品： %1-無法安裝更新 ' %2 '。 錯誤碼 %3。</td>
<td>指出安裝程式無法安裝更新的錯誤訊息。 如需有關如何開啟記錄的詳細資訊，請參閱針對<a href="windows-installer-best-practices.md">部署進行疑難排解時，在使用者的電腦上啟用詳細資訊記錄。</a><strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>產品： %1。 下列進程正在使用檔案 %2：名稱： %3，識別碼 %4。</td>
<td><strong>Windows Installer 2.0：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows安裝程式判斷其設定資料登錄機碼未正確地受到保護。 金鑰的擁有者必須是本機系統或 Builtin\administrators。 將會刪除現有的金鑰，並以適當的安全性設定重新建立。</td>
<td>警告訊息。<strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows安裝程式判斷出其設定資料內的登錄子機碼 %1 未正確地受到保護。 金鑰的擁有者必須是本機系統或 Builtin\administrators。 將會刪除現有的子機碼及其所有內容。</td>
<td>警告訊息。<strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows安裝程式判斷其設定資料快取資料夾未正確地受到保護。 金鑰的擁有者必須是本機系統或 Builtin\administrators。 將會刪除現有的資料夾，並以適當的安全性設定重新建立。</td>
<td>警告訊息<strong><a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>產品： %1。 需要重新開機。</td>
<td>警告訊息指出需要重新開機系統才能完成安裝，而且重新開機已延後到稍後。<strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>產品： %1。 應用程式嘗試安裝較新版本的受保護 Windows 檔案 %2。 您可能需要更新作業系統，此應用程式才能正常運作。  (套件版本： %3，作業系統保護的版本： %4) 。</td>
<td>警告訊息，指出安裝嘗試取代受<a href="windows-resource-protection-on-windows-vista.md">Windows 資源保護</a>保護的重要檔案。 可能需要作業系統更新才能使用此應用程式。 <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>產品： %1。 元件 ' %3 ' 的元件 ' %2 ' 正在使用中。</td>
<td>警告訊息，指出安裝嘗試更新目前正在使用的元件。 系統必須重新開機，才能完成此元件的更新。<strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>重新整理在安裝 ' %1 ' 期間更新的環境變數時發生錯誤。</td>
<td>警告訊息，指出某些登入電腦的使用者可能需要登出再重新登入，才能完成環境變數的更新。<strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/></td>
</tr>
<tr class="even">
<td>1033</td>
<td>產品： %1。 版本： %2。 語言： %3。 安裝完成，狀態為： %4。 製造商： %5。</td>
<td>欄位 1- <a href="productname.md"><strong>ProductName</strong></a> 欄位 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> 欄位 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/> 現場 5- <a href="manufacturer.md"><strong>製造商</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 及更早版本</a>：</strong>無法使用欄位5。<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>產品： %1。 版本： %2。 語言： %3。 移除完成，狀態為： %4。 製造商： %5。</td>
<td>欄位 1- <a href="productname.md"><strong>ProductName</strong></a> 欄位 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> 欄位 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/> 現場 5- <a href="manufacturer.md"><strong>製造商</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 及更早版本</a>：</strong>無法使用欄位5。<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>產品： %1。 版本： %2。 語言： %3。 設定變更已完成，狀態為： %4。 製造商： %5。</td>
<td>欄位 1- <a href="productname.md"><strong>ProductName</strong></a> 欄位 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> 欄位 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> 現場 5- <a href="manufacturer.md"><strong>製造商</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 及更早版本</a>：</strong>無法使用欄位5。<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>產品： %1。 版本： %2。 語言： %3。 更新： %4。 更新安裝完成，狀態為： %5。 製造商： %6。</td>
<td>欄位 1- <a href="productname.md"><strong>ProductName</strong></a> 欄位 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> 欄位 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> 欄位 4-如果 patch 封裝中有 <a href="msipatchmetadata-table.md">MsiPatchMetadata 資料表</a> ，這就是使用者易記名稱。 否則，這是 patch 的 patch code GUID。<br/> 欄位 5-更新安裝的狀態。<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/> 現場 6- <a href="manufacturer.md"><strong>製造商</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 及更早版本</a>：</strong>無法使用欄位6。<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>產品： %1。 版本： %2。 語言： %3。 更新： %4。 更新移除完成，狀態為： %5。 製造商： %6。</td>
<td>欄位 1- <a href="productname.md"><strong>ProductName</strong></a> 欄位 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> 欄位 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> 欄位 4-如果 patch 封裝中有 <a href="msipatchmetadata-table.md">MsiPatchMetadata 資料表</a> ，這就是使用者易記名稱。 否則，這是 patch 的 patch code GUID。<br/> 欄位 5-更新移除的狀態。<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/> 現場 6- <a href="manufacturer.md"><strong>製造商</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 及更早版本</a>：</strong>無法使用欄位6。<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>產品： %1。 版本： %2。 語言： %3。 需要重新開機。 重新開機類型： %4。 重新開機原因： %5。 製造商： %6。</td>
<td>欄位 1- <a href="productname.md"><strong>ProductName</strong></a> 欄位 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> 欄位 3- <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> 欄位 4-指出重新開機類型的常數： <br/> <dl> <strong>msirbRebootImmediate</strong> (1) -立即重新開機電腦。<br />
<strong>msirbRebootDeferred</strong> (2) -使用者或 <a href="reboot.md"><strong>系統</strong></a>管理員已使用 UI 或 restart = ReallySuppress 來延遲需要重新開機電腦。<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0) -未指定的原因需要重新開機。<br />
<strong>msirbRebootInUseFilesReason</strong> (1) -需要重新開機才能取代使用中的檔案。<br />
<strong>msirbRebootScheduleRebootReason</strong> (2) -套件包含 <a href="schedulereboot-action.md">ScheduleReboot</a> 動作。<br />
<strong>msirbRebootForceRebootReason</strong> (3) -套件包含 <a href="forcereboot-action.md">ForceReboot</a> 動作。<br />
<strong>msirbRebootCustomActionReason</strong> (4) -稱為 <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>MsiSetMode</strong></a> 函數的自訂動作。<br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 及更早版本</a>：</strong>無法使用。<br/> 現場 6- <a href="manufacturer.md"><strong>製造商</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 及更早版本</a>：</strong>無法使用欄位6。<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>安裝程式在安裝此封裝時發生未預期的錯誤。 這可能表示封裝有問題。 錯誤碼為 [1]。 {{引數為： [2]，[3]，[4]}}</td>
<td>指出發生內部錯誤的錯誤訊息。 此訊息的文字是以錯誤資料表中為錯誤5撰寫的文字為基礎。</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>產品 [2] –安裝作業已順利完成</td>
<td>安裝產品成功的告知性訊息。</td>
</tr>
<tr class="even">
<td>11708</td>
<td>產品 [2] –安裝操作失敗</td>
<td>產品安裝失敗的錯誤訊息。</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>產品 [2]--已成功完成設定。</td>
<td>設定產品設定成功的告知性訊息。</td>
</tr>
</tbody>
</table>



 

您可以使用 Msidb.exe 或 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)，將事件的當地語系化錯誤字串匯入到資料庫中。 SDK 包含當地語系化 [錯誤和 ActionText 表](localizing-the-error-and-actiontext-tables.md) 一節中所列之每種語言的當地語系化資源字串。 如果未填入對應至事件的錯誤字串，則安裝程式會針對 [**ProductLanguage**](productlanguage.md) 屬性所指定的語言載入當地語系化的字串。

 

 
