---
title: 主題檔案格式
description: 本檔討論主題 ( 的格式。主題) 檔。 主題檔案是一個 .ini 文字檔，可分為區段，以指定顯示在 Windows 桌面上的視覺元素。 區段名稱會以方括弧括住 ( \\ ) 在 .ini 檔案中。
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "103842852"
---
# <a name="theme-file-format"></a>主題檔案格式

本檔討論主題 ( 的格式。主題) 檔。 主題檔案是一個 .ini 文字檔，可分為區段，以指定顯示在 Windows 桌面上的視覺元素。 區段名稱會以方括弧括住 \[ \] ， (.Ini 檔案中的) 。

Windows 7 引進了新的檔案格式 themepack，可協助使用者共用主題。 您只能在 Windows 7 Home Premium 或更高版本的個人化主控台中選取主題，或只在安裝桌面元件時，在 Windows Server 2008 R2 上選取主題。

本文將討論下列主題。

-   [建立主題檔案](#creating-a-theme-file)
-   [主題檔案的描述](#description-of-a-theme-file)
    -   [\[主題 \] 區段](#theme-section)
    -   [\[主控台 \\ 色彩 \] 區段](#control-panelcolors-section)
    -   [\[主控台資料 \\ 指標 \] 區段](#control-panelcursors-section)
    -   [\[主控台 \\ Desktop \] 區段](#control-paneldesktop-section)
    -   [\[投影片 \] 區段](#slideshow-section)
    -   [\[計量 \] 區段](#metrics-section)
    -   [\[視覺化樣式 \] 區段](#visual-styles-section)
    -   [\[聲音 \] 和 \[ AppEvents \] 區段 (音效) ](#sounds-and-appevents-sections-sounds)
    -   [\[開機 \] 區段](#boot-section)
    -   [\[MasterThemeSelector \] 區段](#masterthemeselector-section)
-   [主題檔案的範例](#example-of-a-theme-file)
-   [安裝主題檔案](#installing-theme-files)
-   [主題套件](#theme-packs)
-   [相關主題](#related-topics)

## <a name="creating-a-theme-file"></a>建立主題檔案

主題檔案可讓您變更某些桌面元素的外觀。 您可以透過兩種方式來建立或修改主題檔案：

-   修改主控台中的個人化或顯示設定，並將設定儲存為主題檔案。 如需相關指示，請參閱 Windows 說明。
-   手動建立一個主題檔，以進一步控制您主題的詳細資料。

若要讓您的主題可供其他使用者使用，您必須提供您的主題檔案，以及背景圖片、螢幕保護裝置和圖示檔案。 您可以使用 [主題套件](#theme-packs)來完成此動作。

## <a name="description-of-a-theme-file"></a>主題檔案的描述

主題檔案有數個必要和選用的區段。 以下說明主題檔案的區段，並提供如何針對不同的元素指定變更的範例。

### <a name="theme-section"></a>\[主題 \] 區段

> [!Note]  
> 此為選擇性區段。 如果您未在您的主題檔案中包含此區段，系統會使用預設設定。

 

[ \[ 主題] \] 區段會識別自訂主題的名稱，並指定您主題的品牌標誌和桌面圖示。

主題區段的第一個 \[ 部分 \] 包含下列兩個元素：



| 元素                                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName = 名稱<br/> 或<br/> DisplayName = @module 、-stringid 指定<br/> 範例： DisplayName = @themeui.dll 、-2013 | DisplayName 是將會顯示在個人化主控台中的主題名稱。 它可以是字串或當地語系化名稱的參考。<br/> 此為選擇性欄位。 如果遺失，則會使用主題檔案名作為主題名稱。<br/>                                                                                                                                                                                                                                         |
| BrandImage = 影像的路徑<br/> 範例： BrandImage = c： \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 和更新版本** BrandImage 會指定在個人化主控台的主題預覽中所併入之品牌化圖形檔案的路徑。<br/> 圖示圖形必須是 PNG 檔。 圖形會調整為80x240 圖元，因此建議您提供該大小的影像。 主題資源庫會遵循您品牌圖示的透明區域。<br/> 此為選擇性欄位。 如果遺失，則不會顯示任何標誌作為主題圖示。<br/> |



 

[主題] 區段的其餘 \[ \] 部分會指定桌面功能的自訂圖示，例如 [電腦]、[我的檔]、[網路] 和 [資源回收筒。 如果您未指定自訂桌面圖示，桌面會顯示系統預設桌面圖示。

以下是主題檔案如何設定 **電腦** 圖示的兩個範例。


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



以下是 Windows 7 中預設桌面圖示的值。


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a>\[主控台 \\ 色彩 \] 區段

> [!Note]  
> 此為選擇性區段。 如果您未在您的主題檔案中包含此區段，系統會使用預設設定。 如果您的主題使用 Aero 視覺化樣式，您應該避免覆寫這個區段中的預設值。

 

您可以自訂元素的色彩，例如捲軸、文字和按鈕。 這個主題檔會指定要針對這些元素變更的 RGB 值。 這些值會覆寫視覺化樣式的預設值，而且當您的主題是以 Windows 傳統、Windows 7 Basic 或高對比主題為基礎時，就會使用這些值。

以下是如何設定色彩的範例。


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a>\[主控台資料 \\ 指標 \] 區段

> [!Note]  
> 此為選擇性區段。 如果您未在您的主題檔案中包含此區段，系統會使用預設資料指標。

 

主題也可以變更資料指標的外觀。 若要這樣做，您可以建立檔案來取代預設的 Windows 資料指標。 下列範例是來自訂稱為 *體育* 主題之資料指標的主題檔案。


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a>\[主控台 \\ Desktop \] 區段

> [!Note]  
> 此為必要區段。 如果您未在您的主題檔案中包含此區段，系統會忽略您的主題，而不會在主控台中顯示主題。

 

您可以建立自訂桌面背景，並指定影像檔案的路徑。 下列範例顯示如何修改桌面外觀。


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a>\[投影片 \] 區段

**Windows 7 和更新版本。**

> [!Note]  
> 此為選擇性區段。 如果您未在您的主題檔案中包含此區段，系統會使用 \[ 主控台 desktop 區段中指定的桌面背景 \\ 影像 \] 。 如果您包含此區段，您必須在這裡指定投影片放映設定。

 

您主題的背景可以是一張投影片，其中的影像儲存在本機或 RSS 摘要所提供的影像。 檔案的 [投影片] \[ \] 區段包含下列屬性：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interval = 毫秒數</td>
<td>必要。 間隔是決定背景變更頻率的數位。 它是以毫秒為單位來測量。</td>
</tr>
<tr class="even">
<td>隨機 = 0 或1</td>
<td>必要。 隨機識別是否為背景洗牌。<br/> 0 = 停用<br/> 1 = 啟用<br/></td>
</tr>
<tr class="odd">
<td>Rss 摘要 = RSS 摘要的 URL</td>
<td>如果未指定 ImagesRootPath，則為必要項。 Rss 摘要指定要作為背景投影片放映使用的 RSS 摘要。 若要讓摘要能夠運作，您必須參考符合 &quot; &quot; <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS 平臺</a>所使用之主機殼標準的高解析度映射。 由於這項限制，必須以手動方式建立包含 RSS 摘要的主題檔案。 <br/>
<blockquote>
[!Note]<br />
您無法同時指定 Rss 摘要和 ImagesRootPath。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>ImagesRootPath = 映射資料夾的路徑</td>
<td>如果未指定 Rss 摘要，則為必要項。 ImagesRootPath 指定一組您想要用來做為背景投影片放映的影像路徑。 子資料夾中的影像不包含在投影片放映中。<br/> ImagesRootPath 支援路徑中的環境變數替代。<br/>
<blockquote>
[!Note]<br />
您無法同時指定 Rss 摘要和 ImagesRootPath。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>專案<em>N</em>路徑 = 路徑 (s) 至特定映射 (s) </td>
<td>與 ImagesRootPath 搭配使用。 <br/> 專案<em>N</em>路徑指定特定影像的路徑，讓您可以將投影片放映限制為特定影像，而不是資料夾中的所有影像。 如果未指定路徑，則會在投影片放映中使用 ImagesRootPath 路徑中的所有影像，包括建立和安裝主題之後加入的影像。<br/> 專案<em>N</em>路徑支援路徑中的環境變數替代。 <em>N</em> 為0、1、2等等。 <br/></td>
</tr>
</tbody>
</table>



 

下列範例示範如何指定將投影片放映的投影片放映，以包含一組儲存在本機的影像。


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



下列範例是主題檔案的範本，該檔案會使用 RSS 摘要中的影像來建立桌面背景投影片放映。 遵循下列步驟來自訂範本：

1.  複製下列範例，並將它貼到文字編輯器中。
2.  將 {themename} 取代為您要在個人化主控台主題圖庫中顯示的名稱。
3.  以相容 RSS 摘要的完整路徑取代 {rssfeedurl}。
4.  將變更儲存為副檔名為 ". 主題" 的檔案。


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a>\[計量 \] 區段

> [!Note]  
> 此為選擇性區段。 如果您未在您的主題檔案中包含此區段，系統會使用預設的視覺化樣式設定。

 

您可以在主題檔案中指定系統計量。 系統計量是各種顯示元素的維度，例如視窗框線寬度、圖示高度或捲軸寬度。 NonclientMetrics 和 IconMetrics 值是 NONCLIENTMETRICS 和 ICONMETRICS 在 winuser 中定義的二進位結構。 以下是如何變更系統計量的範例。


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a>\[視覺化樣式 \] 區段

> [!Note]  
> 此為必要區段。 如果您未在您的主題檔案中包含此區段，系統會忽略您的主題，而不會在主控台中顯示主題。

 

您可以在 msstyles 檔案中提供有關桌面元素大小和色彩的特定資訊。 您可以使用 msstyles 檔案來取代主題檔案的 [色彩] 和 [大小] 區段，讓您更詳細地修改桌面元素。 這些檔案是在主題檔案的視覺化樣式區段中指定。 以下是視覺化樣式區段的範例。


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



將 Path 元素加入至 msstyles 檔案是選擇性的。 如果您提供路徑，您應該從主題檔案中移除 [度量] 和 [色彩] 區段。 移除這些區段時，主題的色彩、字型和大小會來自 msstyles 檔案，並符合 msstyles 作者的意圖。 無法移除 [度量] 和 [色彩] 區段可能會導致 Windows 或應用程式有繪製問題。

**Windows Vista/windows 7：** 當路徑指向 Aero. msstyles 時，您可以指定所需的半透明色彩，如下列範例所示。

**Windows 7：** 當路徑指向 Aero. msstyles 時，您也可以指定所需的透明度值，如下列範例所示。


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



如果 ColorizationColor 和透明度值完全符合系統色彩，個人化主控台會顯示色彩的系統名稱。 否則，色彩會標示為「自訂」。

以下顯示 Windows 7 基本主題的 >visualstyles 一節。


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



以下顯示 Windows 傳統主題的 >visualstyles 一節。


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



以下顯示高對比黑色主題的 >visualstyles 區段。


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[聲音 \] 和 \[ AppEvents \] 區段 (音效) 

> [!Note]  
> 此為選擇性區段。 如果您的主題檔案中未包含此區段，系統會使用預設的音效設定。

 

使用者可以在主控台中選取 **音效** 圖示，以將聲音與應用程式中發生的事件產生關聯。 例如，當應用程式開啟時，可以播放 .wav 檔。 主題檔案可以指定 .wav 檔來取代預設的 .wav 檔。 下列範例示範如何執行。


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



**Windows 7 和更新版本：** 您可以指定音效配置名稱，而不是個別列出每個音效。


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



SchemeName 值會指定音效配置名稱或當地語系化的音效配置名稱（如上述範例所示）。

### <a name="boot-section"></a>\[開機 \] 區段

> [!Note]  
> **螢幕保護裝置在 Windows 10 年度更新版和之後已淘汰。**

 

> [!Note]  
> 此為選擇性區段。 如果您未在您的主題檔案中包含此區段，則不會使用任何螢幕保護裝置。

 

在 [主題] 檔案中，您可以指定 Windows 要使用的螢幕保護裝置。 以下範例說明這點。


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[MasterThemeSelector \] 區段

> [!Note]  
> 此為必要區段。 如果您未在您的主題檔案中包含此區段，系統會忽略您的主題，而不會在主控台中顯示主題。

 

主題檔案的主要主題選取器區段應該一律包含為指出檔案有效的標記。 您沒有此參數的值選擇。 如下所示。


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>主題檔案的範例

下列範例顯示完整的主題檔案。


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a>安裝主題檔案

當 Windows 初始化時，作業系統會列舉% WinDir% 資源的第一層子目錄， \\ \\ 以找出可用的主題。 系統預設主題檔案位於% WinDir% \\ 資源 \\ 主題。 使用者主題檔案儲存在% WinDir% \\ Users \\ <username> \\ AppData \\ Local \\ Microsoft \\ Windows 主題中 \\ 。

主題檔案具有檔案關聯;因此，主題安裝程式應用程式可以在 ShellExecute 的主題檔案上呼叫 [](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) ，以在指定的主題主控台中開啟 **個人** 化視窗。

## <a name="theme-packs"></a>主題套件

**Windows 7 和更新版本。** 主題套件是一個 .cab 檔案，其中不僅包含主題檔案，還包含在另一部電腦上執行該主題所需的檔案，例如音效檔和影像。 使用者可以透過個人化主控台建立主題套件。

支援的檔案類型包括下列各項：



| 檔案類型    | 分機                           |
|--------------|-------------------------------------|
| 佈景主題        | .theme                              |
| Image        | .jpg、jpeg、.bmp、.dib、.tif、.png |
| 音效        | .wav                                |
| 滑鼠游標 | 。                          |
| 桌面圖示 | .ico                                |
| 品牌標誌   | .png                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[視覺化樣式總覽](visual-styles-overview.md)
</dt> </dl>

