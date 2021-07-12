---
description: 討論為 Windows Vista 和更新版本的系統開啟主控台專案，以及涵蓋舊版主控台命令的方法。
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: 執行主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb6ae2fa08231d3876e1a5a636e404f519f4a6
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581756"
---
# <a name="executing-control-panel-items"></a>執行主控台專案

> [!Note]  
> 如果您要尋找主控台專案的標準和模組名稱清單，請參閱 [主控台專案](controlpanel-canonical-names.md)的正式名稱。

 

有兩種方式可以開啟主控台專案：

-   使用者可以開啟主控台然後按一下或按兩下專案的圖示來開啟專案。
-   使用者或應用程式可以直接從命令列提示字元中執行，以啟動主控台專案。

應用程式可以使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) 函數，以程式設計方式開啟主控台。


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



下列範例顯示應用程式如何使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)函式來啟動名為 **MyCpl.cpl** 的主控台專案。


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



透過命令列開啟主控台專案時，您可以指示它開啟至專案中的特定索引標籤。 由於某些 Windows Vista 主控台專案中的特定索引標籤的新增和移除，在 Windows XP 中，索引標籤的編號可能已變更。 例如，下列範例會在 Windows XP 上的系統專案中，以及 Windows Vista 的第三個索引標籤上，啟動第四個索引標籤。


```
control.exe sysdm.cpl,,3
```



本主題將討論下列內容：

-   [WindowsVista 標準名稱](#windows-vista-canonical-names)
-   [Windows Vista 的新命令](#new-commands-for-windows-vista)
-   [舊版主控台命令](#legacy-control-panel-commands)
-   [相關主題](#related-topics)

## <a name="windows-vista-canonical-names"></a>WindowsVista 標準名稱

在 Windows Vista 和更新版本中，從命令列啟動主控台專案的慣用方法是使用主控台專案的正式名稱。 標準名稱是主控台專案在登錄中宣告的非當地語系化字串。 使用標準名稱的值，是它會將主控台專案的模組名稱抽象化。 專案可以在 .dll 中執行，並在稍後根據為 .exe 或變更其模組名稱。 只要正式名稱維持不變，就不需要更新使用該正式名稱開啟該名稱的任何程式。

依照慣例，正式名稱的格式為 "CorporationName. ControlPanelItemName"。

下列範例顯示應用程式如何使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)來啟動主控台專案 **Windows Update** 。


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



若要使用其正式名稱啟動主控台專案，請使用： "% systemroot% \\ system32 \\control.exe/name *canonicalName*"

若要在專案中開啟特定的子頁面，或使用其他參數開啟它，請使用： "% systemroot% \\ system32 \\control.exe/name **canonicalName** /page **pageName**"

應用程式也可以執行 [**IOpenControlPanel：： open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) 方法來啟動主控台專案，包括開啟特定子頁面的能力。

如需主控台專案標準名稱的完整清單，請參閱 [主控台專案的正式名稱](controlpanel-canonical-names.md)。

## <a name="new-commands-for-windows-vista"></a>Windows Vista 的新命令

在 Windows Vista 中，Windows XP 上的 .cpl 模組所存取的某些選項現在會實作為 .exe 檔。 這可讓標準使用者在嘗試啟動檔案時提供系統管理員認證，以提供額外的安全性。 不需要額外安全性的選項，可透過 Windows XP 中使用的相同命令列來存取。 以下是 Windows Vista 中用來存取主控台專案的特定索引標籤的命令清單：

### <a name="personalization"></a>個人化

-   字型大小和 DPI：% windir% \\ system32 \\DpiScaling.exe
-   螢幕解析度：% windir% \\ system32 \\control.exe desk.cpl，設定，@Settings
-   顯示設定：% windir% \\ system32 \\control.exe desk.cpl、設定、@Settings
-   主題：% windir% \\ system32 \\control.exe desk.cpl，主題，@Themes
-   螢幕保護裝置：% windir% \\ system32 \\control.exe desk.cpl、螢幕保護裝置程式@screensaver
-   多重監視器：% windir% \\ system32 \\control.exe desk.cpl，監視，@Monitor
-   色彩配置：% windir% \\ system32 \\control.exe/name Microsoft. 個人化/page pageColorization
-   桌面背景：% windir% \\ system32 \\control.exe/name Microsoft. 個人化/page pageWallpaper

> [!Note]  
> Starter 和 Basic 版本不支援 control.exe/name Microsoft 個人化命令。

 

### <a name="system"></a>系統

-   效能：% windir% \\ system32 \\SystemPropertiesPerformance.exe
-   遠端存取：% windir% \\ system32 \\SystemPropertiesRemote.exe
-   電腦名稱稱：% windir% \\ system32 \\SystemPropertiesComputerName.exe
-   系統保護：% windir% \\ system32 \\SystemPropertiesProtection.exe
-   Advanced system properties：% windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>[程式和功能]

-   新增或移除程式：% windir% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures
-   Windows 功能：% windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>地區及語言選項

-   鍵盤：% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p： "鍵盤"
-   位置：% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p： "location"
-   系統管理：% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p： "系統管理"

### <a name="folder-options"></a>資料夾選項

-   資料夾搜尋：% windir% \\ system32 \\rundll32.exe shell32.dll，選項 \_ RunDLL 2
-   檔案關聯：% windir% \\ system32 \\control.exe/name Microsoft. DefaultPrograms/page pageFileAssoc
-   View：% windir% \\ system32 \\rundll32.exe shell32.dll，Options \_ RunDLL 7
-   一般：% windir% \\ system32 \\rundll32.exe shell32.dll，選項 \_ RunDLL 0

### <a name="power-options"></a>電源選項

-   編輯目前的計畫設定：% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pagePlanSettings
-   系統設定：% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageGlobalSettings
-   建立電源計劃：% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageCreateNewPlan
-   Advanced 設定 page 沒有標準命令，它會以較舊的方式存取：% windir% \\ system32 \\control.exe powercfg.cpl，，3

## <a name="legacy-control-panel-commands"></a>舊版主控台命令

當您使用 [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) 函數時，系統可以辨識特殊的主控台命令。 這些命令會早 Windows Vista。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe 桌面</td>
<td>啟動 <strong>顯示內容</strong> 視窗。
<blockquote>
[!Note]<br />
Starter 和 Basic 版本不支援此命令。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>control.exe 色彩</td>
<td>啟動已預先選取 [<strong>外觀</strong>] 索引標籤的 [<strong>顯示內容</strong>] 視窗。</td>
</tr>
<tr class="odd">
<td>control.exe 日期/時間</td>
<td>啟動 [ <strong>日期和時間] 屬性</strong> 視窗。</td>
</tr>
<tr class="even">
<td>control.exe 國際</td>
<td>啟動 [ <strong>地區及語言選項</strong> ] 視窗。</td>
</tr>
<tr class="odd">
<td>control.exe 滑鼠</td>
<td>啟動 <strong>滑鼠 [屬性</strong> ] 視窗。</td>
</tr>
<tr class="even">
<td>control.exe 鍵盤</td>
<td>啟動 [ <strong>鍵盤屬性</strong> ] 視窗。</td>
</tr>
<tr class="odd">
<td>control.exe 印表機</td>
<td>顯示 [ <strong>印表機和傳真</strong> ] 資料夾。</td>
</tr>
<tr class="even">
<td>control.exe 字型</td>
<td>顯示 [ <strong>字型</strong> ] 資料夾。</td>
</tr>
</tbody>
</table>



 

針對 Windows 2000 和更新版本的系統：



| 命令                    | 描述                                              |
|----------------------------|----------------------------------------------------------|
| control.exe 資料夾        | 啟動 [ **資料夾選項** ] 視窗。                  |
| control.exe netware        | 如果已安裝) ，則啟動 **Novell NetWare** 視窗 (。   |
| control.exe 電話語音      | 啟動 [**電話和數據機選項**] 視窗。         |
| control.exe admintools     | 顯示 [系統 **管理工具** ] 資料夾。            |
| control.exe schedtasks     | 顯示 [ **排定** 的工作] 資料夾。                 |
| control.exe netconnections | 顯示 [ **網路連接** ] 資料夾。             |
| control.exe 紅外線       | 如果已安裝) ，會啟動 [ **紅外線監視器** ] 視窗 (。 |
| control.exe userpasswords  | 啟動 [ **使用者帳戶** ] 視窗。                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[使用 CPLApplet](using-cplapplet.md)
</dt> <dt>

[主控台訊息處理](message-processing.md)
</dt> <dt>

[擴充系統主控台專案](extending-system-control-panel-items.md)
</dt> <dt>

[指派主控台分類](assigning-control-panel-categories.md)
</dt> <dt>

[建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)
</dt> <dt>

[在 Windows Vista 下存取保管庫模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
