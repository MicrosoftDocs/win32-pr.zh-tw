---
title: " (Windows 控制項的屬性識別碼) "
description: 本主題包含已定義值的相關資訊，這些值可用來抓取視覺化樣式的屬性。 定義可在 Vssym32 中找到。
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0869ac80332a5dbdb146ee255f5c9e73f4a812
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685352"
---
# <a name="property-identifiers-windows-controls"></a> (Windows 控制項的屬性識別碼) 

本主題包含已定義值的相關資訊，這些值可用來抓取視覺化樣式的屬性。 定義可在 Vssym32 中找到。

## <a name="property-types"></a>屬性類型

下表列出基本的屬性類型。 第一個資料行中的值通常不會由應用程式使用，但是會提供分類屬性識別碼的方法。



| 資料類型       | 描述                              | 傳回的類型                          | 抓取函式                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ BOOL       | **TRUE** 或 **FALSE**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool)、 [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| TMT \_ 色彩      | RGB 色彩值                          | [**COLORREF**](/windows/desktop/gdi/colorref) 結構 | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor)、 [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | 磁片資料流程                              | **HINSTANCE**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| TMT \_ 列舉       | 列舉值                         | 列舉型別                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue)。                                                                        |
| TMT \_ 檔案名   | 相對於主題目錄的檔案名 | **WCHAR** 陣列                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| TMT \_ 字型       | 字型描述                         | [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont)、 [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ HBITMAP    | 點陣圖                                   | **HBITMAP** 控制碼                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ INT        | 帶正負號                            | 整數                                | [**GetThemeInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint)、 [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint)、 [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ INTLIST    | 整數清單                         | [**INTLIST**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist) 結構   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| TMT \_ 邊界    | 邊界：左邊、頂端、右邊和底部    | [**邊界**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) 結構   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| TMT \_ 位置   | 專案的位置                      | [**點**](/previous-versions//dd162805(v=vs.85)) 結構       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ RECT       | 矩形的大小和位置         | [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| TMT \_ 大小       | 專案的大小                          | [**大小**](/previous-versions//dd145106(v=vs.85)) 結構         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| TMT \_ 字串     | Unicode 字串                           | **WCHAR** 陣列                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring)、 [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>屬性識別碼

以下是依資料類型分組之主題屬性的定義值。

**TMT \_ BOOL**



| 識別碼                        | 備註                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | 如果應該一律顯示與元件和狀態相關聯的大小調整列，**則為 TRUE** 。                                                                                                                           |
| TMT \_ AUTOSIZE             | 如果與元件和狀態相關聯的非工作區標題區域與文字寬度不同，則 **為 TRUE** 。                                                                                                                 |
| TMT \_ BGFILL               | 如果要在背景填滿時，將與元件和狀態相關聯的大小調整影像設為 true，**則為 true** 。                                                                                                        |
| TMT \_ BORDERONLY           | 如果與元件和狀態相關聯的影像應該只繪製其邊界，**則為 TRUE** 。                                                                                                                     |
| TMT \_ 複合           | 如果與元件和狀態相關聯的控制項將會處理本身的影像合成，**則為 TRUE** 。                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| TMT \_ DRAWBORDERS          |                                                                                                                                                                                                                 |
| TMT \_ FLATMENUS            | 請參閱 [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)。                                                                                                                                                                 |
| TMT \_ GLYPHONLY            | 如果與元件和狀態相關聯的圖像應該在沒有背景的情況下繪製，**則為 TRUE** 。                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | 如果與元件和狀態相關聯的圖像具有透明區域，**則為 TRUE** 。 如需定義透明色彩之 TMT GLYPHCOLOR 值的定義，請參閱 [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) \_ 。 |
| TMT \_ INTEGRALSIZING       | 如果與元件和狀態相關聯的 truesize 影像或框線必須調整為2的因數，**則為 TRUE** 。                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **如果以** 由右至左閱讀模式來查看視窗，則應該翻轉與元件和狀態相關聯的影像。                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | 如果與元件和狀態相關聯的影像會在必要時相應放大，則 **為 TRUE** 。                                                                                                                |
| TMT \_ SOURCESHRINK         | 如果與元件和狀態相關聯的影像會在需要時調整為較小的大小，**則為 TRUE** 。                                                                                                               |
| TMT \_ TEXTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| TMT \_ TEXTGLOW             |                                                                                                                                                                                                                 |
| TMT \_ TEXTITALIC           |                                                                                                                                                                                                                 |
| TMT \_ 透明          |                                                                                                                                                                                                                 |
| TMT \_ UNIFORMSIZING        | 如果與元件和狀態相關聯的影像必須有相等的高度和寬度，**則為 TRUE** 。                                                                                                                      |
| TMT \_ USERPICTURE          | 如果與元件和狀態相關聯的影像是以目前使用者為基礎，則 **為 TRUE** 。                                                                                                                          |



 

**TMT \_ 色彩**



| 識別碼                           | 備註                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | 用來作為自訂控制項之輔色提示的色彩。                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| TMT \_ 背景              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | 用來作為 blend 色彩的色彩。                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| TMT \_ 邊框             | 與元件和狀態相關聯的框線色彩。                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | 用來當做自訂控制項之框線色彩提示的色彩。                                                                                                                                     |
| TMT \_ BTNFACE                 |                                                                                                                                                                                                |
| TMT \_ BTNHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BTNTEXT                 |                                                                                                                                                                                                |
| TMT \_ BUTTONALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | 與這個元件和狀態相關聯之邊緣的深色陰影色彩。                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | 與這個元件和狀態相關聯的邊緣填滿色彩。                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | 與這個元件和狀態相關聯之邊緣的醒目提示色彩。                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | 與此元件和狀態相關聯之邊緣的淺色色彩。                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | 與這個元件和狀態相關聯之邊緣的陰影色彩。                                                                                                                              |
| TMT \_ FILLCOLOR               | 與元件和狀態相關聯的背景填滿色彩。                                                                                                                           |
| TMT \_ FILLCOLORHINT           | 用來作為自訂控制項填滿色彩提示的色彩。                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ GLOWCOLOR               | 使用這個部分和狀態呼叫 [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) 所產生的發光色彩。                                                                                    |
| TMT \_ GLYPHTEXTCOLOR          | 與這個元件和狀態相關聯之字型型圖像將使用的色彩。                                                                                                              |
| TMT \_ GLYPHTRANSPARENTCOLOR   | 與這個元件和狀態相關聯的透明圖像色彩。 如果 \_ 這個元件的 TMT GLYPHTRANSPARENT 值和狀態為 **TRUE**，就不會繪製使用此色彩的部分圖像。 |
| TMT \_ GRADIENTACTIVECAPTION   |                                                                                                                                                                                                |
| TMT \_ GRADIENTCOLOR1          | 與這個元件和狀態相關聯之漸層的第一種色彩。                                                                                                                           |
| TMT \_ GRADIENTCOLOR2          | 漸層的第二個色彩。                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR3          | 漸層的第三個色彩。                                                                                                                                                               |
| TMT \_ GRADIENTCOLOR4          | 漸層的第四個色彩。                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR5          | 漸層的第五個色彩。                                                                                                                                                               |
| TMT \_ GRADIENTINACTIVECAPTION |                                                                                                                                                                                                |
| TMT \_ GRAYTEXT                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ 醒目提示               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| TMT \_ HOTTRACKING 開啟             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ INFOTEXT                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| TMT \_ 功能表                    |                                                                                                                                                                                                |
| TMT \_ 功能表列                 |                                                                                                                                                                                                |
| TMT \_ MENUHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| TMT \_ 捲軸               |                                                                                                                                                                                                |
| TMT \_ SHADOWCOLOR             | 在與這個部分和狀態相關聯的文字下繪製的陰影色彩。                                                                                                             |
| TMT \_ TEXTBORDERCOLOR         | 與這個元件和狀態相關聯的文字框線色彩。                                                                                                                              |
| TMT \_ TEXTCOLOR               | 與這個元件和狀態相關聯之文字的色彩。                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | 與這個元件和狀態相關聯之文字陰影的色彩。                                                                                                                              |
| TMT \_ TRANSPARENTCOLOR        | 與這個元件和狀態相關聯的透明色彩。 如果 \_ 這個元件的 TMT 透明值和狀態為 **TRUE**，則不會繪製使用此色彩的圖形部分。          |
| TMT \_ 視窗                  |                                                                                                                                                                                                |
| TMT \_ WINDOWFRAME             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| 識別碼              | 備註 |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**TMT \_ 列舉**



| 列舉型別         | 屬性值                                                                                                                                                                                                                                            | 備註                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE、BT \_ BORDERFILL                                                                                                                                                                                                                              | 此元件的基本繪圖類型。                                                                                                                |
| BORDERTYPE          | BT \_ RECT、BT \_ ROUNDRECT、BT \_ 橢圓形                                                                                                                                                                                                                       | 當這個部分是框線填滿時，所繪製的框線類型。                                                                                              |
| CONTENTALIGNMENT    | CA \_ 左方、CA \_ 中心、CA \_ 權利                                                                                                                                                                                                                            | 與此元件相關聯之標題中的文字對齊方式。                                                                                      |
| FILLTYPE            | FT \_ 固態、FT \_ VERTGRADIENT、FT \_ HORZGRADIENT、FT \_ RADIALGRADIENT、FT \_ TILEIMAGE                                                                                                                                                                           | 當這個部分是框線填滿時，所繪製的填滿圖形類型。                                                                                          |
| GLYPHTYPE           | GT \_ 無、GT \_ IMAGEGLYPH、GT \_ FONTGLYPH                                                                                                                                                                                                                    | 此元件繪製的圖像類型。                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ NONE、GFST \_ SIZE、GFST \_ DPI                                                                                                                                                                                                                          | 用來在不同大小的字型之間選取的方法類型。                                                                                    |
| HALIGN              | HA \_ 剩下，HA \_ 中心，HA \_ 許可權                                                                                                                                                                                                                            | 如果這個部分使用真正大小的影像，則為水準對齊。                                                                                        |
| ICONEFFECT          | ICE \_ 無、冰 \_ 發光、冰 \_ 影子、冰 \_ 脈衝、冰 \_ ALPHA                                                                                                                                                                                                  | 使用 [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)繪製此元件時，所要顯示的效果類型。                                             |
| IMAGELAYOUT         | IL \_ 垂直、IL \_ 水準                                                                                                                                                                                                                               | 繪製多個影像時所使用的對齊類型。                                                                                           |
| IMAGESELECTTYPE     | IST \_ NONE、IST \_ 大小、IST \_ DPI                                                                                                                                                                                                                             | 用來在此元件的大小影像之間選取的方法類型。 請參閱 GetThemeFilename 的 TMT \_ IMAGEFILE1 [](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)值。 |
| OFFSETTYPE          | OT \_ 下拉式功能表、OT \_ 右上、OT \_ TOPMIDDLE、OT \_ BOTTOMLEFT、OT \_ BOTTOMRIGHT、OT \_ BOTTOMMIDDLE、OT \_ MIDDLELEFT、OT \_ \_ \_ \_ \_ \_ \_ MIDDLERIGHT、OT LEFTOFCAPTION、OT RIGHTOFCAPTION、OT LEFTOFLASTBUTTON、OT RIGHTOFLASTBUTTON、OT ABOVELASTBUTTON、OT BELOWLASTBUTTON | 這個部分在視窗上的對齊方式。                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE、ST \_ STRETCH、ST \_ 圖、ST \_ TILEHORZ、ST \_ TILEVERT、ST \_ TILECENTER                                                                                                                                                                            | 如果這個部分使用影像檔案，則用來調整影像大小的方法。                                                                                    |
| TEXTSHADOWTYPE      | TST \_ NONE、TST \_ SINGLE、TST \_ 連續                                                                                                                                                                                                                    | 要在與此元件相關聯的文字背後繪製的陰影效果類型。                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ NONE、TSST \_ SIZE、TSST \_ DPI                                                                                                                                                                                                                          | 當這個部分使用真尺寸的影像時，所使用的縮放類型。                                                                                       |
| VALIGN              | VA \_ 頂端、VA \_ 中心、VA \_ 底部                                                                                                                                                                                                                            | 如果這個部分使用真正大小的影像，則垂直對齊。                                                                                          |



 

**TMT \_ 檔案名**



| 識別碼                  | 備註                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYPHIMAGEFILE | 與這個元件和狀態相關聯之圖像影像的檔案名。                                                                        |
| TMT \_ IMAGEFILE      | 與此元件和狀態相關聯之影像的檔案名，或與此元件和狀態相關聯之多個映射的基底檔案名。 |
| TMT \_ IMAGEFILE1     | 與此元件和狀態相關聯的第一個縮放影像的檔案名，以支援不同的解析度。                            |
| TMT \_ IMAGEFILE2     | 第二個縮放影像的檔案名。                                                                                                     |
| TMT \_ IMAGEFILE3     | 第三個縮放影像的檔案名。                                                                                                      |
| TMT \_ IMAGEFILE4     | 第四個縮放影像的檔案名。                                                                                                     |
| TMT \_ IMAGEFILE5     | 第五個縮放影像的檔案名。                                                                                                      |



 

**TMT \_ 字型**



| 識別碼                    | 備註                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| TMT \_ GLYPHFONT        | 當使用以字型為基礎的字元時，與此元件相關聯的字型將會繪製的字型。 |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| TMT \_ ICONTITLEFONT    |                                                                                                      |
| TMT \_ MENUFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| TMT \_ STATUSFONT       |                                                                                                      |



 

**TMT \_ INT**



| 識別碼                       | 備註                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)使用的 Alpha 值 (0-255) 。                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | 最小 Alpha 值 (0-255) 必須將圖元視為不透明。                                                                                                                                  |
| TMT \_ ANIMATIONDELAY      |                                                                                                                                                                                                                  |
| TMT \_ ANIMATIONDURATION   |                                                                                                                                                                                                                  |
| TMT \_ BORDERSIZE          | 當這個部分使用框線填滿時，所繪製的框線粗細。                                                                                                                                               |
| TMT \_ 字元集             |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONCOLOR   |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONOPACITY |                                                                                                                                                                                                                  |
| TMT \_ FRAMESPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT \_ GLOWINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | 如果元件使用以字型為基礎的圖像，則為要用於圖像的選定字型中的字元索引。                                                                                                 |
| TMT \_ GRADIENTRATIO1      | 第一個漸層色彩 (TMT \_ GRADIENTCOLOR1) 用來繪製元件的數量。 這個值可以是0到255，但是這個值加上每個 GRADIENTRATIO 值的值都必須加上255。 |
| TMT \_ GRADIENTRATIO2      | 第二個漸層色彩 (TMT \_ GRADIENTCOLOR2) 用來繪製元件的數量。                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | 第三個漸層色彩 (TMT \_ GRADIENTCOLOR3) 用來繪製元件的數量。                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | 第四個漸層色彩 (TMT \_ GRADIENTCOLOR4) 用來繪製元件的數量。                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | 第五個漸層色彩 (TMT \_ GRADIENTCOLOR5) 用來繪製元件的數量。                                                                                                                         |
| TMT \_ 高度              | 元件的高度。                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | 影像檔案中所顯示的狀態影像數目。                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | 第一個影像檔的設計目的是每英寸的最小點數 (DPI) 。                                                                                                                                      |
| TMT \_ MINDPI2             | 第二個影像檔案設計的最小 DPI。                                                                                                                                                     |
| TMT \_ MINDPI3             | 第三個影像檔案設計時的最小 DPI。                                                                                                                                                      |
| TMT \_ MINDPI4             | 第四個影像檔案設計的最小 DPI。                                                                                                                                                     |
| TMT \_ MINDPI5             | 第五個影像檔案設計用的最小 DPI。                                                                                                                                                      |
| TMT \_ 不透明度             |                                                                                                                                                                                                                  |
| TMT \_ PIXELSPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | 進度控制項「區塊」圖形的大小，定義作業的進度。                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | 所有進度控制項「區塊」的總大小。                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | 圓度的圓度 (0 到 100%) 。                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | 圓度的圓度 (0 到 100%) 。                                                                                                                                                          |
| TMT \_ 飽和度          |  (0-255) 套用至使用 [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)繪製之圖示的飽和度量。                                                                                                         |
| TMT \_ TEXTBORDERSIZE      | 在文字字元周圍繪製的框線粗細。                                                                                                                                                        |
| TMT \_ TEXTGLOWSIZE        |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR1            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR2            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR3            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR4            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR5            |                                                                                                                                                                                                                  |
| TMT \_ TOHUE1              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE2              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE3              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE4              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE5              |                                                                                                                                                                                                                  |
| TMT \_ TRUESIZESTRETCHMARK | 影像將延展到的真實大小影像原始大小百分比。                                                                                                                        |
| TMT \_ 寬度               | 元件的寬度。                                                                                                                                                                                           |



 

**TMT \_ INTLIST**



| 識別碼                       | 備註 |
|--------------------------|-------|
| TMT \_ TRANSITIONDURATIONS |       |



 

**TMT \_ 邊界**



| 識別碼                  | 備註                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | 定義標題文字可以放在元件中的邊界。 |
| TMT \_ CONTENTMARGINS | 定義內容可能放置在元件中的邊界。      |
| TMT \_ SIZINGMARGINS  | 用來調整非真尺寸影像大小的邊界。                      |



 

**TMT \_ 位置**



| 識別碼                    | 備註                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MINSIZE          | 在移至下一個最小的影像檔案之前，可以使用一般影像檔案的大小下限。   |
| TMT \_ MINSIZE1         | 第一個小型影像檔可用於的最小大小。                                            |
| TMT \_ MINSIZE2         | 第二個小型影像檔案可使用的大小下限。                                           |
| TMT \_ MINSIZE3         | 第三個小型影像檔案可使用的大小下限。                                            |
| TMT \_ MINSIZE4         | 第四個小型影像檔可用於的最小大小。                                           |
| TMT \_ MINSIZE5         | 第五個小型影像檔案可用的最小大小。                                            |
| TMT \_ NORMALSIZE       | 與此元件相關聯之一般影像的大小。                                                      |
| TMT \_ 位移           | 此元件對齊的位置位移。 對齊是由 TMT \_ OFFSETTYPE 值定義。 |
| TMT \_ TEXTSHADOWOFFSET | 繪製文字陰影之文字的位移。                                                    |



 

**TMT \_ RECT**



| 識別碼                       | 備註                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| TMT \_ CUSTOMSPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | 元件的預設大小。 |



 

**TMT \_ 大小**



| 識別碼                      | 備註                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | 標題列高度。       |
| TMT \_ CAPTIONBARWIDTH    | 標題列寬度。        |
| TMT \_ MENUBARHEIGHT      | 功能表列高度。          |
| TMT \_ MENUBARWIDTH       | 功能表列的寬度。           |
| TMT \_ PADDEDBORDERWIDTH  | 填補的框線寬度。      |
| TMT \_ SCROLLBARHEIGHT    | 捲軸高度。        |
| TMT \_ SCROLLBARWIDTH     | 捲軸寬度。         |
| TMT \_ SIZINGBORDERWIDTH  | 調整大小框線的寬度。 |
| TMT \_ SMCAPTIONBARHEIGHT | 標題列高度。       |
| TMT \_ SMCAPTIONBARWIDTH  | 標題列寬度。        |



 

**TMT \_ 字串**



| 識別碼                   | 備註                                               |
|----------------------|-----------------------------------------------------|
| TMT \_ 別名           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| TMT \_ 作者          |                                                     |
| TMT \_ CLASSICVALUE    |                                                     |
| TMT \_ COLORSCHEMES    |                                                     |
| TMT \_ 公司         |                                                     |
| TMT \_ 著作權       |                                                     |
| TMT \_ CSSNAME         | 請參閱 [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)。 |
| TMT \_ 描述     |                                                     |
| TMT \_ DISPLAYNAME     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| TMT \_ 大小           |                                                     |
| TMT \_ 文字            | 元件所顯示的文字。                     |
| TMT \_ 工具提示         |                                                     |
| TMT \_ URL             |                                                     |
| TMT \_ 版本         |                                                     |
| TMT \_ XMLNAME         | 請參閱 [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)。 |
| TMT \_ 名稱            |                                                     |



 

 

 
