---
description: 表示 Shell 中的物件。
title: 'IShellDispatch 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840889"
---
# <a name="ishelldispatch-object"></a>IShellDispatch 物件

表示 Shell 中的物件。 系統會提供方法來控制 Shell，並在 Shell 中執行命令。 也有方法可以取得其他與 Shell 相關的物件。

> [!Note]  
> **IShellDispatch** 是透過 [**Shell**](shell.md) 物件來執行和存取。

 

## <a name="members"></a>成員

**IShellDispatch** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IShellDispatch** 物件有這些方法。



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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></td>
<td style="text-align: left;">建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 <a href="folder.md"><strong>資料夾</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></td>
<td style="text-align: left;">將桌面上的所有視窗都串聯在一起。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 <strong>視窗</strong>] 相同。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">執行指定的主控台應用程式。 如果應用程式已經開啟，則會啟動執行中的實例。 <br/>
<blockquote>
<p>[!Note]<br />
從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。 若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。 例如：</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></td>
<td style="text-align: left;">從其銜接站彈出電腦。 這與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>退出</strong>電腦] 的方式相同，如果您的電腦支援此命令。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>探討</strong></a></td>
<td style="text-align: left;">在 Windows 檔案總管視窗中開啟指定的資料夾。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></td>
<td style="text-align: left;">向使用者顯示 [ <strong>執行</strong> ] 對話方塊。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>搜尋結果：電腦</strong> ] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>Findfiles.ps1</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>尋找：所有</strong> 檔案] 對話方塊。 這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>搜尋</strong>]。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Help</strong></a></td>
<td style="text-align: left;">顯示 [Windows 說明及支援] 視窗。 這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [說明 <strong>及支援</strong>] 的效果相同。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></td>
<td style="text-align: left;">最小化桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 <strong>所有視窗最小化</strong> ]，或按一下工作列上的 [ <strong>顯示桌面</strong> ] 圖示。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>命名 空間</strong></a></td>
<td style="text-align: left;">建立並傳回指定資料夾的 <a href="folder.md"><strong>資料夾</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>打開</strong></a></td>
<td style="text-align: left;">開啟指定的資料夾。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></td>
<td style="text-align: left;">重新整理 [ <strong>開始</strong> ] 功能表的內容。 只能與 Windows XP 之前的系統搭配使用。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>日期和時間</strong> ] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ <strong>調整日期/時間</strong>]。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></td>
<td style="text-align: left;">顯示 <strong>關機 Windows</strong> ] 對話方塊。 這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>關機</strong>]。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>暫止</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></td>
<td style="text-align: left;">以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>顯示視窗堆疊</strong>]。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></td>
<td style="text-align: left;">垂直並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排 <strong>顯示視窗</strong>]。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></td>
<td style="text-align: left;">顯示 [ <strong>工作列] 和 [開始功能表屬性</strong> ] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>屬性</strong>] 相同。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></td>
<td style="text-align: left;">將所有桌面視窗還原到最後一個 <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> 命令之前的狀態。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>復原最小化</strong> 舊系統上的所有 Windows (]) 或第二次按一下工作列中的 [ <strong>顯示桌面</strong> ] 圖示。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">建立並傳回 <a href="shellwindows.md"><strong>ShellWindows</strong></a> 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>屬性

**IShellDispatch** 物件具有這些屬性。



| 屬性                                                     | 存取類型          | 描述                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | 唯讀<br/> | 包含代表應用程式的物件。<br/>                    |
| [**父代**](ishelldispatch-parent.md)<br/>           | 唯讀<br/> | 抓取物件，該物件表示目前物件的父系。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell 物件**](shell.md)
</dt> </dl>

 

 
