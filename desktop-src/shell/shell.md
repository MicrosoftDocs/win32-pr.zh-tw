---
description: 表示 Shell 中的物件。 系統會提供方法來控制 Shell，並在 Shell 中執行命令。 也有方法可以取得其他與 Shell 相關的物件。
title: 命令介面物件 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: fe2fbaa1bad61ac9c22d36919e49cf493a26a778a8e97d69d1b200c0c62205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857717"
---
# <a name="shell-object"></a>Shell 物件

表示 Shell 中的物件。 系統會提供方法來控制 Shell，並在 Shell 中執行命令。 也有方法可以取得其他與 Shell 相關的物件。

## <a name="members"></a>成員

**Shell** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Shell** 物件具有這些方法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">方法</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></td>
<td style="text-align: left;">將檔案加入最近使用的 (MRU) 清單中。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 <a href="folder.md"><strong>資料夾</strong></a> 物件。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></td>
<td style="text-align: left;">判斷目前的使用者是否可以啟動和停止命名服務。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">將桌面上的所有視窗都串聯在一起。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>Cascade Windows</strong>] 相同。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">執行指定的主控台 ( * .cpl) 應用程式。 如果應用程式已經開啟，則會啟動執行中的實例。 <br/>
<blockquote>
<p>[!Note]<br />
從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。 若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。 例如：</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">從其銜接站彈出電腦。 這與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>退出</strong>電腦] 的方式相同，如果您的電腦支援此命令。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>探索</strong></a></td>
<td style="text-align: left;">在 Windows 檔案總管視窗中開啟指定的資料夾。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></td>
<td style="text-align: left;">取得指定 Internet Explorer 原則的值。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">向使用者顯示 [ <strong>執行</strong> ] 對話方塊。 這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>執行</strong>] 的效果相同。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>搜尋結果：電腦</strong> ] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>Findfiles.ps1</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>尋找：所有</strong> 檔案] 對話方塊。 這等同于按一下 [<strong>開始</strong>] 功能表，然後選取 [<strong>搜尋</strong> (] 或其對等專案（在 Windows XP 之前的系統）。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>尋找印表機</strong> ] 對話方塊。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">捕獲全域 Shell 設定。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></td>
<td style="text-align: left;">捕獲系統資訊。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>説明</strong></a></td>
<td style="text-align: left;">顯示 Windows 說明及支援中心。 這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [說明 <strong>及支援</strong>] 的效果相同。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></td>
<td style="text-align: left;">從登錄抓取群組的限制設定。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></td>
<td style="text-align: left;">傳回值，這個值表示特定服務是否正在執行。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">最小化桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [<strong>最小化</strong>舊系統上的所有 Windows] 或 [Windows 2000 或 Windows XP 中工作列快速啟動區域中的 [<strong>顯示桌面</strong>] 圖示相同。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>命名 空間</strong></a></td>
<td style="text-align: left;">建立並傳回指定資料夾的 <a href="folder.md"><strong>資料夾</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>打開</strong></a></td>
<td style="text-align: left;">開啟指定的資料夾。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">重新整理 [ <strong>開始</strong> ] 功能表的內容。 只能搭配 Windows XP 之前的系統使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></td>
<td style="text-align: left;">顯示應用程式搜尋窗格。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></td>
<td style="text-align: left;">啟動命名服務。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></td>
<td style="text-align: left;">停止已命名的服務。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>日期和時間屬性</strong> ] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ <strong>調整日期/時間</strong>]。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">在指定的檔案上執行指定的作業。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></td>
<td style="text-align: left;">顯示瀏覽器列。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">顯示<strong>關機 Windows</strong> ] 對話方塊。 這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>關機</strong>]。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>暫止</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [<strong>並排 Windows</strong>]。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">垂直並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [<strong>並排 Windows</strong>]。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></td>
<td style="text-align: left;">顯示或隱藏桌面。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>工作列] 和 [開始功能表屬性</strong> ] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>屬性</strong>] 相同。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">將所有桌面視窗還原到最後一個 <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> 命令之前的相同狀態。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [復原]，將舊版系統上的<strong>所有 Windows</strong> ，或第二次按一下 Windows 2000 或 Windows XP 中工作列快速啟動區域中的 [<strong>顯示桌面</strong>] 圖示。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">建立並傳回 <a href="shellwindows.md"><strong>ShellWindows</strong></a> 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>Windows 安全性</strong>] 對話方塊。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></td>
<td style="text-align: left;">將開啟的視窗顯示在您可以切換的3D 堆疊中。<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>屬性

**Shell** 物件具有這些屬性。



| 屬性                                            | 存取類型          | 描述                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Application**](shell-application.md)<br/> | 唯讀<br/> | 包含物件的應用程式物件。<br/>                        |
| [**父代**](shell-parent.md)<br/>           | 唯讀<br/> | 取得物件，表示目前物件的父系。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
