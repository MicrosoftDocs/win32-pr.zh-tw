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
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475294"
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




| 方法 | 描述 | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a> | 建立對話方塊，讓使用者選取資料夾，然後傳回選取的資料夾 <a href="folder.md"><strong>資料夾</strong></a> 物件。<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a> | 將桌面上的所有視窗都串聯在一起。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [串聯 <strong>視窗</strong>] 相同。<br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | 執行指定的主控台應用程式。 如果應用程式已經開啟，則會啟動執行中的實例。 <br /><blockquote><p>[!Note]<br />從 Windows Vista 開始，大部分的主控台應用程式都是 Shell 專案，無法使用此功能開啟。 若要開啟這些主控台的應用程式，請將正式名稱傳遞給 control.exe。 例如：</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a> | 從其銜接站彈出電腦。 這與按一下 [ <strong>開始</strong> ] 功能表並選取 [ <strong>退出</strong>電腦] 的方式相同，如果您的電腦支援此命令。<br /> | 
| <a href="ishelldispatch-explore.md"><strong>探索</strong></a> | 在 Windows 檔案總管視窗中開啟指定的資料夾。<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a> | 向使用者顯示 [ <strong>執行</strong> ] 對話方塊。<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a> | 顯示 [ <strong>搜尋結果：電腦</strong> ] 對話方塊。 此對話方塊會顯示指定電腦的搜尋結果。<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>Findfiles.ps1</strong></a> | 顯示 [ <strong>尋找：所有</strong> 檔案] 對話方塊。 這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>搜尋</strong>]。<br /> | 
| <a href="ishelldispatch-help.md"><strong>説明</strong></a> | 顯示 [說明及支援] 視窗 Windows。 這個方法與按一下 [ <strong>開始</strong> ] 功能表並選取 [說明 <strong>及支援</strong>] 的效果相同。<br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a> | 最小化桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [<strong>最小化</strong>舊系統上的所有 Windows] 或按一下工作列上的 [<strong>顯示桌面</strong>] 圖示相同。<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>命名 空間</strong></a> | 建立並傳回指定資料夾的 <a href="folder.md"><strong>資料夾</strong></a> 物件。<br /> | 
| <a href="ishelldispatch-open.md"><strong>打開</strong></a> | 開啟指定的資料夾。<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a> | 重新整理 [ <strong>開始</strong> ] 功能表的內容。 只能搭配 Windows XP 之前的系統使用。<br /> | 
| <a href="ishelldispatch-settime.md"><strong>SetTime</strong></a> | 顯示 [ <strong>日期和時間</strong> ] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ <strong>調整日期/時間</strong>]。<br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a> | 顯示<strong>關機 Windows</strong> ] 對話方塊。 這等同于按一下 [ <strong>開始</strong> ] 功能表，然後選取 [ <strong>關機</strong>]。<br /> | 
| <a href="ishelldispatch-suspend.md"><strong>暫止</strong></a> | Td | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a> | 以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>顯示視窗堆疊</strong>]。<br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a> | 垂直並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排 <strong>顯示視窗</strong>]。<br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a> | 顯示 [ <strong>工作列] 和 [開始功能表屬性</strong> ] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ <strong>屬性</strong>] 相同。<br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a> | 將所有桌面視窗還原到最後一個 <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> 命令之前的狀態。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [<strong>復原] 最小化</strong>舊版系統上的所有 Windows () 或第二次按一下工作列中的 [<strong>顯示桌面</strong>] 圖示。<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | 建立並傳回 <a href="shellwindows.md"><strong>ShellWindows</strong></a> 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。<br /> | 




 

### <a name="properties"></a>屬性

**IShellDispatch** 物件具有這些屬性。



| 屬性                                                     | 存取類型          | Description                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Application**](ishelldispatch-application.md)<br/> | 唯讀<br/> | 包含代表應用程式的物件。<br/>                    |
| [**父代**](ishelldispatch-parent.md)<br/>           | 唯讀<br/> | 抓取物件，該物件表示目前物件的父系。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell 物件**](shell.md)
</dt> </dl>

 

 
