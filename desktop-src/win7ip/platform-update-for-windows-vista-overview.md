---
title: 關於 Windows Vista 的平臺更新
description: 概要說明 Windows Vista 的平臺更新，以及 Windows Server 2008 及其功能的平臺更新。
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Windows Server 2008 的平臺更新
- Windows Vista 的平臺更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9751331bf764ee486afe20a9dccd7f6b4691fee15e5000ccf8157561656409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964567"
---
# <a name="about-platform-update-for-windows-vista"></a>關於 Windows Vista 的平臺更新

Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新為終端使用者作業系統更新，可支援在舊版 Windows 作業系統上使用所選 Windows 7 技術。 這些更新包含一組執行時間程式庫，可讓應用程式開發人員以最新版本、Windows 7 和 Windows server 2008 R2 以及舊版（Windows Vista 和 Windows Server 2008）為目標。

## <a name="summary-of-supported-api-by-technology"></a>支援的 API （依技術）摘要

Windows Vista 的平臺更新所支援的每項技術以及 Windows Server 2008 更新的平臺更新，都包含一組 API，可用於以舊版 Windows 為目標的應用程式。

如需在以舊版 Windows 為目標的應用程式中使用更新所支援之 api 的詳細資訊，請參閱[針對舊版 Windows 開發應用程式](developing-applications-for-previous-versions-of-windows.md)。

> [!Note]  
> 某些與技術相關聯的 api 可能不受支援，而且某些支援的 api 的行為、效能或需求可能會因 Windows 版本而異。 如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Windows Vista 的平臺更新所支援的技術

如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。

下表顯示 Windows vista 和 Windows XP 的平臺更新 Windows vista 所支援的技術。

| 技術                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [Windows自動化 API](#windows-automation-api)                                             | 是           | 是        |
| [Windows圖形、影像處理和 XPS 程式庫](#windows-graphics-imaging-and-xps-library)        | 是           | 否         |
| [Windows功能區和動畫管理員程式庫](#windows-ribbon-and-animation-manager-library) | 是           | 否         |
| [Windows可攜式裝置平臺](#windows-portable-devices-platform)                       | 是           | 否         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Windows Server 2008 的平臺更新所支援的技術

如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。

下表顯示 Windows server 2008 和 Windows server 2003 （具有 Windows Server 2008 的平臺更新）支援的技術。

| 技術                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [Windows自動化 API](#windows-automation-api)                                             | 是                 | 是                 |
| [Windows圖形、影像處理和 XPS 程式庫](#windows-graphics-imaging-and-xps-library)        | 是                 | 否                  |
| [Windows功能區和動畫管理員程式庫](#windows-ribbon-and-animation-manager-library) | 是                 | 否                  |
| [Windows可攜式裝置平臺](#windows-portable-devices-platform)                       | 否                  | 否                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>依技術支援的 API 說明

如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。

-   [Windows自動化 API](#windows-automation-api)
-   [Windows圖形、影像處理和 XPS 程式庫](#windows-graphics-imaging-and-xps-library)
-   [Windows功能區和動畫管理員程式庫](#windows-ribbon-and-animation-manager-library)
-   [Windows可攜式裝置平臺](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>Windows自動化 API

WindowsAutomation API 3.0 是一組 Dll 和 API 元素，可在) 產品上提供輔助技術 (，以提供更好的電腦存取權給有實體或認知難題、受損或殘障人士的個人。 此外，由於 Windows Automation API 3.0 可讓應用程式存取和管理其他應用程式的使用者介面 (UI) 元素，這是執行自動化測試控管的理想技術。

Microsoft Active Accessibility (MSAA) 和消費者介面自動化很類似，因為兩者都提供公開和收集使用者介面元素和控制項相關資訊的方法，以支援使用者介面協助工具和軟體測試自動化。 消費者介面自動化是消費者介面自動化規格的 Windows 執行。 它是一項較新的技術，可解決 MSAA 的許多限制。

如需 Windows automation api 3.0 的詳細資訊，請參閱[Windows automation api：總覽](/windows/desktop/WinAuto/windows-automation-api-overview)。

適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新，支援下列 Windows Automation API 3.0：

-   [Microsoft Active Accessibility (MSAA) ](#microsoft-active-accessibility-msaa)
-   [使用者介面自動化](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows適用于更新的版本

Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新，會在下表所示的 Windows 版本上啟用 Windows Automation API 3.0 支援。



<table>
<thead>
<tr class="header">
<th>Windows 版本</th>
<th>適用于 Update 的版本</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> 使用 SP2 的 Starter (x86) <br />
Home Basic SP2 (x86 和 amd64) <br />
使用 SP2 (x86 和 amd64) 的 Home 進階版<br />
使用 SP2 (x86 和 amd64) 的企業<br />
Enterprise SP2 (x86 和 amd64) <br />
SP2 (x86 和 amd64) 的終極<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> WindowsXP Home SP3 (x86) <br />
WindowsXP Professional SP3 (x86) <br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> WindowsServer 2008 SP2 (x86 和 amd64) <br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> WindowsServer 2003 SP2 (x86 和 amd64) <br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA) 

Microsoft Active Accessibility (MSAA) 是在 Windows 95 中首次引進的舊版技術。 它是一組 Api，可改善) 產品的輔助技術 (與在 Microsoft Windows 上執行的應用程式搭配運作的方式。 API 會提供程式設計介面和方法，以公開使用者介面專案的相關資訊。

如需 Microsoft Active Accessibility 的詳細資訊，請參閱 [技術總覽](/windows/desktop/WinAuto/technical-overview)。

### <a name="supported-microsoft-active-accessibility-api-elements"></a>支援的 Microsoft Active Accessibility API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="ui-automation"></a>UI 自動化

消費者介面自動化是一種較新的技術，可實消費者介面自動化規格並解決許多 Microsoft Active Accessibility 的限制。 它是一組 Api，可讓您以程式設計方式存取應用程式的使用者介面元素。 提供的 API 可協助輔助技術產品和自動化測試控管存取、識別和操作應用程式的標準和自訂 UI 元素。

如需消費者介面自動化的詳細資訊，請參閱[Windows Automation API：消費者介面自動化](../winauto/entry-uiauto-win32.md)。

### <a name="supported-ui-automation-api-elements"></a>支援的消費者介面自動化 API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="running-ui-automation-on-previous-windows-versions"></a>在先前的 Windows 版本上執行消費者介面自動化

由於通用控制項和 Windows 標準控制項在不同 Windows 版本上的執行方式有所差異，因此消費者介面自動化 proxy 針對這些控制項從某個版本抓取到另一個版本的資訊可能會有些微差異。

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows圖形、影像處理和 XPS 程式庫

Windows Vista 的平臺更新支援來自 Windows 圖形、影像處理和 XPS 程式庫的下列 Windows 7 api：

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [包裝](#packaging)
-   [Windows Imaging Component](#windows-imaging-component)
-   [XPS 檔](#xps-document)
-   [XPS 列印](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows適用于更新的版本

Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新，會在下表所示的 Windows 版本上啟用 Windows 圖形、影像處理和 XPS 程式庫支援。



<table>
<thead>
<tr class="header">
<th>Windows 版本</th>
<th>適用于 Update 的版本</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> 使用 SP2 的 Starter (x86) <br />
Home Basic SP2 (x86 和 amd64) <br />
使用 SP2 (x86 和 amd64) 的 Home 進階版<br />
使用 SP2 (x86 和 amd64) 的企業<br />
Enterprise SP2 (x86 和 amd64) <br />
SP2 (x86 和 amd64) 的終極<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> WindowsServer 2008 SP2 (x86 和 amd64) <br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

Direct2D API 是新的硬體加速、即時模式的2-d 圖形 API，可為2D 幾何、點陣圖和文字提供高效能和高品質的呈現。 Direct2D API 是設計來與使用 GDI、GDI+ 或 Direct3D 的現有程式碼交互操作。

如需 Direct2D 的詳細資訊，請參閱 [關於 Direct2D](/windows/desktop/Direct2D/direct2d-overview)。

### <a name="supported-direct2d-api-elements"></a>支援的 Direct2D API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="running-direct2d-on-previous-windows-versions"></a>在先前的 Windows 版本上執行 Direct2D

如果 Windows Vista 缺少 WDDM 1.1 驅動程式，Direct2D/GDI 互通性的效能會降低。

### <a name="direct3d"></a>Direct3D

Windows Vista 的平臺更新提供 Direct3D10 和 direct3d 10.1 程式碼路徑的 BGRA 介面支援。 Direct3D10Level9 可讓 Direct3D10 功能在 Direct3D9 硬體上運作。 Direct3D WARP10 是適用于 Direct3D10 應用程式的高效能軟體轉譯器。 Direct3D11 是最新版的 Direct3D，可提供新的功能，例如改良的多執行緒支援、鑲嵌式、DirectCompute 功能和動態著色器連結。

如果您建立使用 Direct3D 的應用程式，則需要 [DIRECTX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) 。

如需 Direct3D 的詳細資訊，請參閱 [direct3d](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx) 。

### <a name="supported-direct3d-api-elements"></a>支援的 Direct3D API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="directwrite"></a>DirectWrite

DirectWrite API 是新的文字 API，提供多層的功能，包括文字配置、腳本處理、圖像轉譯和字型系統。 DirectWrite 使用 OpenType 字型和子圖元 ClearType 轉譯來加強應用程式所提供的文字體驗。 使用 Direct2D 時，文字轉譯是硬體加速。

如需 DirectWrite 的詳細資訊，請參閱[DirectWrite 簡介](/windows/desktop/DirectWrite/introducing-directwrite)。

### <a name="supported-directwrite-api-elements"></a>支援的 DirectWrite API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="running-directwrite-on-previous-windows-versions"></a>在先前的 Windows 版本上執行 DirectWrite

下列行為問題可能會影響先前 Windows 版本上 DirectWrite API 的使用：

-   Windows 7 的新腳本可能無法在先前的 Windows 版本上完全正確呈現。
-   先前的 Windows 版本中未提供的地區設定會回復為預設行為。
-   在舊版 Windows 上無法使用 ClearType 調諧器。
-   在 Windows 舊版的某些情況下，GDI 互通性的記憶體成本較高。

### <a name="packaging"></a>包裝

Windows Vista 的平臺更新支援在非受控應用程式中使用 XPS 檔 api 執行工作所需的有限封裝 api 子集。

如需封裝 Api 的詳細資訊，請參閱 [封裝 Api 總覽](/previous-versions/windows/desktop/opc/packaging-api-overview)。

### <a name="supported-packaging-api-elements"></a>支援的封裝 API 元素

僅支援下列封裝介面：

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (僅支援下列方法) 
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

支援的封裝 Api 可以用來建立檔案的資料流程，以及建立以套件為基礎的 URI 並與其互動。

### <a name="running-packaging-api-on-previous-windows-versions"></a>在先前的 Windows 版本上執行封裝 API

在所有支援的平臺上，支援的封裝介面和方法的行為和效能都相同。

如果應用程式嘗試具現化或呼叫不支援的封裝介面或方法，則嘗試將會失敗。 如果呼叫的是不支援的 [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) 方法， \_ 將會傳回 E >notimpl 錯誤碼。

### <a name="windows-imaging-component"></a>Windows Imaging Component

Windows 影像處理元件 (WIC) 的新功能包括增強的安全性、支援高的色彩，以及更好的中繼資料互通性。 此外，Windows 影像處理元件藉由提供漸進式影像解碼、擴充的 PNG 功能、GIF 中繼資料、HD 相片更新，以及橫跨 APPn 區段的中繼資料支援，來拓寬其標準合規性。

如需有關 Windows 影像處理元件的詳細資訊，請參閱[Windows 影像處理元件總覽](/windows/desktop/wic/-wic-about-windows-imaging-codec)。

### <a name="supported-wic-api-elements"></a>支援的 WIC API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="xps-document"></a>XPS 檔

XPS 檔 Api 支援在非受控應用程式中建立、修改及儲存 XPS 檔

如需 XPS 檔 Api 的詳細資訊，請參閱 [Xps 檔程式設計指南。](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>支援的 XPS 檔 API 元素

舊版作業系統版本只支援 [XPS 數位簽章](/previous-versions/windows/desktop/dd372947(v=vs.85)) 介面。

### <a name="xps-print"></a>XPS 列印

xps 列印 api 支援從以 Windows 為基礎的應用程式列印 xps 檔。

如需 XPS 列印 Api 的詳細資訊，請參閱 [XPSPRINT API](/windows/desktop/printdocs/xpsprint-api)。

### <a name="supported-xps-print-api-elements"></a>支援的 XPS 列印 API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows功能區和動畫管理員程式庫

Windows Vista 的平臺更新支援來自 Windows 功能區和動畫庫的下列 Windows 7 api：

-   [Windows功能區架構](#windows-ribbon-and-animation-manager-library)
-   [Windows動畫管理員](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows適用于更新的版本

Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新，會在下表所示的 Windows 版本上啟用 Windows 功能區和動畫管理員程式庫支援。



<table>
<thead>
<tr class="header">
<th>Windows 版本</th>
<th>適用于 Update 的版本</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> 使用 SP2 的 Starter (x86) <br />
Home Basic SP2 (x86 和 amd64) <br />
使用 SP2 (x86 和 amd64) 的 Home 進階版<br />
使用 SP2 (x86 和 amd64) 的企業<br />
Enterprise SP2 (x86 和 amd64) <br />
SP2 (x86 和 amd64) 的終極<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> WindowsServer 2008 SP2 (x86 和 amd64) <br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Windows功能區架構

Windows 功能區 (功能區) 架構是一種豐富的命令呈現系統，可為傳統 Windows 應用程式的階層式功能表、工具列和工作窗格提供新式替代方法。

此架構是 Microsoft Win32 api 的集合，可為 Windows 開發人員提供新的使用者介面功能，並同時包含功能區和內容功能表系統。

如需功能區架構的詳細資訊，請參閱[Windows 功能區架構簡介](../windowsribbon/windowsribbon-introduction.md)。

### <a name="supported-ribbon-framework-api-elements"></a>支援的功能區架構 API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="windows-animation-manager"></a>Windows動畫管理員

Windows 的動畫管理員 (Windows 動畫) 是一種程式設計介面，可支援 Windows 應用程式之視覺元素的動畫。 Windows動畫的設計目的是簡化動畫順序的開發和維護，以及讓開發人員能夠執行一致且直覺的動畫。 Windows動畫可以與任何圖形平台搭配使用，包括 Direct2D、Direct3D 或 GDI+。

Windows動畫是單一執行緒 COM API，可提供開發人員建立、管理和驅動 UI 動畫所需的一切。

如需 Windows 動畫管理員的詳細資訊，請參閱[Windows 動畫簡介](/windows/desktop/UIAnimation/introducing-windows-animation-manager)。

### <a name="supported-animation-manager-api-elements"></a>支援的動畫管理員 API 元素

舊版 Windows 支援所有 api，其符合 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。

### <a name="windows-portable-devices-platform"></a>Windows可攜式裝置平臺

Windows Vista 的平臺更新支援 Windows 可攜式裝置的 Windows 7 延伸模組 (WPD) 平臺。 這項功能可讓電腦與連接的媒體和存放裝置進行通訊。 WPD 提供彈性且健全的方式，讓電腦與數位相機、音樂播放機、行動電話以及許多其他類型的連線裝置進行通訊。

如需 Windows 可攜式裝置的詳細資訊，請參閱[Windows 可攜式裝置](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/) 。

### <a name="windows-editions-eligible-for-the-updates"></a>Windows適用于更新的版本

適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新可讓 Windows 可攜式裝置 (WPD) 支援的版本，如下表所示。



<table>
<thead>
<tr class="header">
<th>Windows 版本</th>
<th>適用于 Update 的版本</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> 使用 SP2 的 Starter (x86) <br />
Home Basic SP2 (x86 和 amd64) <br />
使用 SP2 (x86 和 amd64) 的 Home 進階版<br />
使用 SP2 (x86 和 amd64) 的企業<br />
Enterprise SP2 (x86 和 amd64) <br />
SP2 (x86 和 amd64) 的終極<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>支援的 WPD API 元素

下表指出 Windows 7、Windows Vista 和 Windows vista 的功能，並以 Windows Vista 版本的 Windows 作業系統的平臺更新來支援這些功能。

| WPD 功能                    | Windows 7 | Windows Vista | Windowsvista （含 Windows vista 的平臺更新） |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| 透過 USB 的 MTP                   | 是       | 是           | 是                                                  |
| IP 上的 MTP                    | 是       | 是           | 是                                                  |
| 藍牙的 MTP             | 是       | 否            | 是                                                  |
| WPD 和 MTP 裝置服務    | 是       | 否            | 是                                                  |
| WPD 自動化                 | 是       | 否            | 否                                                   |
| 多函數/多重傳輸 | 是       | 否            | 否                                                   |
| Device Stage                   | 是       | 否            | 否                                                   |
| 裝置同步平臺           | 是       | 否            | 否                                                   |



 

針對 Windows 7 和 Windows Vista 版本，預設不會安裝 Microsoft Windows Media Player (N 和 KN 版本) ，您必須安裝[Windows 媒體格式 11 SDK]( ../audio-and-video.md) (， https://msdn.microsoft.com/windows/bb190326.aspx) 才能啟用 WPD 功能。 如需詳細資訊，請參閱[知識庫文章](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715) ，其原本是發佈為 Windows Vista 的解決方案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Vista 的平臺更新](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**概觀**
</dt> <dt>

[關於 Windows Vista 的平臺更新](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[有關 Windows Vista (KB 971644 的平臺更新的知識庫文章) ](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 