---
title: 視覺化樣式參考
description: 本節說明搭配視覺化樣式使用的下列 API 元素。
ms.assetid: f1d01045-a296-4b39-bd42-1262ba4ad3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac237e8951e2aec3e6521c6918d13f216b0dbd7b11a9eba03c074910fbaea17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828519"
---
# <a name="visual-styles-reference"></a>視覺化樣式參考

本節說明搭配 [視覺化樣式](themes-overview.md)使用的下列 API 元素。

### <a name="functions"></a>函式



| 主題                                                                                  | 目錄                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginBufferedAnimation**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginbufferedanimation)                               | 開始緩衝的動畫作業。 動畫的組成是在指定的一段時間內，兩個緩衝區的內容之間的交叉淡化。 <br/>                                                                     |
| [**BeginBufferedPaint**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginbufferedpaint)                                       | 開始緩衝的繪製作業。<br/>                                                                                                                                                                                      |
| [**BeginPanningFeedback**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginpanningfeedback)                                   | 通知系統傳送有關移動流覽手勢所影響之目標視窗的意見反應。 <br/>                                                                                                                               |
| [**BufferedPaintClear**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintclear)                                       | 清除緩衝區中指定的矩形以 ARGB = {0,0,0,0} 。<br/>                                                                                                                                                         |
| [**BufferedPaintInit**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintinit)                                         | 初始化目前線程的緩衝繪製。<br/>                                                                                                                                                                    |
| [**BufferedPaintRenderAnimation**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintrenderanimation)                   | 繪製緩衝油漆動畫的下一個畫面格。<br/>                                                                                                                                                                    |
| [**BufferedPaintSetAlpha**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintsetalpha)                                 | 將 Alpha 設定為給定矩形中的指定值。 Alpha 會控制與緩衝區混合到目的地目標裝置內容 (DC) 時所套用的透明度量。 <br/>                         |
| [**BufferedPaintStopAllAnimations**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintstopallanimations)               | 停止指定視窗的所有緩衝動畫。<br/>                                                                                                                                                                     |
| [**BufferedPaintUnInit**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintuninit)                                     | 關閉目前線程的已緩衝繪製。 不再需要呼叫 [**BeginBufferedPaint**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginbufferedpaint)之後，呼叫 [**BufferedPaintInit**](/windows/desktop/api/Uxtheme/nf-uxtheme-bufferedpaintinit)的每個呼叫一次。<br/> |
| [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata)                                               | 關閉主題資料控制碼。<br/>                                                                                                                                                                                           |
| [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground)                                     | 繪製指定控制群組件的視覺化樣式所定義的框線和填滿。<br/>                                                                                                                                   |
| [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex)                                 | 繪製指定控制群組件的視覺化樣式所定義的背景影像。<br/>                                                                                                                                  |
| [**DrawThemeEdge**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeedge)                                                 | 繪製由矩形的視覺化樣式所定義的一或多個邊緣。<br/>                                                                                                                                                     |
| [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)                                                 | 使用視覺化樣式所定義的圖示效果，從影像清單中繪製影像。<br/>                                                                                                                                     |
| [**DrawThemeParentBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeparentbackground)                         | 繪製部分透明或 Alpha 混合子控制項所涵蓋之父控制項的部分。<br/>                                                                                                           |
| [**DrawThemeParentBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeparentbackgroundex)                     | 由部分透明或 Alpha 混合的子控制項使用，以便在其顯示的前方繪製其父系的部分。 傳送 WM \_ ERASEBKGND 訊息，後面接著 wm \_ PRINTCLIENT。<br/>                             |
| [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext)                                                 | 使用視覺化樣式所定義的色彩和字型來繪製文字。<br/>                                                                                                                                                        |
| [**方法的**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex)                                             | 使用視覺化樣式所定義的色彩和字型來繪製文字。 藉由允許其他文字格式選項來擴充 [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) 。<br/>                                                             |
| [**EnableThemeDialogTexture**](/windows/desktop/api/Uxtheme/nf-uxtheme-enablethemedialogtexture)                           | 啟用或停用對話方塊視窗背景的視覺化樣式。<br/>                                                                                                                                                   |
| [**EnableTheming**](/windows/desktop/api/Uxtheme/nf-uxtheme-enabletheming)                                                 | 在目前的和更新的會話中，啟用或停用目前使用者的視覺化樣式。<br/>                                                                                                                               |
| [**EndBufferedAnimation**](/windows/desktop/api/Uxtheme/nf-uxtheme-endbufferedanimation)                                   | 呈現緩衝動畫作業的第一個畫面格，並啟動動畫計時器。<br/>                                                                                                                               |
| [**EndBufferedPaint**](/windows/desktop/api/Uxtheme/nf-uxtheme-endbufferedpaint)                                           | 完成已緩衝處理的繪製作業，並釋出相關聯的緩衝油漆控制碼。<br/>                                                                                                                                    |
| [**EndPanningFeedback**](/windows/desktop/api/Uxtheme/nf-uxtheme-endpanningfeedback)                                       | 終止正在處理或由 [**BeginPanningFeedback**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginpanningfeedback) 和 [**UpdatePanningFeedback**](/windows/desktop/api/Uxtheme/nf-uxtheme-updatepanningfeedback)設定的任何現有動畫。 <br/>                                    |
| [**GetBufferedPaintBits**](/windows/desktop/api/Uxtheme/nf-uxtheme-getbufferedpaintbits)                                   | 如果緩衝區是與裝置無關的點陣圖 (DIB) ，則擷取緩衝區點陣圖的指標。<br/>                                                                                                                            |
| [**GetBufferedPaintDC**](/windows/desktop/api/Uxtheme/nf-uxtheme-getbufferedpaintdc)                                       | 取得油漆 DC。 這是 [**BeginBufferedPaint**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginbufferedpaint)所取出的相同值。<br/>                                                                                                                |
| [**GetBufferedPaintTargetDC**](/windows/desktop/api/Uxtheme/nf-uxtheme-getbufferedpainttargetdc)                           | 抓取目標 DC。 <br/>                                                                                                                                                                                               |
| [**GetBufferedPaintTargetRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getbufferedpainttargetrect)                       | 抓取 BeginBufferedPaint 所指定的目標矩形。<br/>                                                                                                                                                         |
| [**GetCurrentThemeName**](/windows/desktop/api/Uxtheme/nf-uxtheme-getcurrentthemename)                                     | 抓取目前視覺效果樣式的名稱，並選擇性地取出色彩配置名稱和大小名稱。<br/>                                                                                                           |
| [**GetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeappproperties)                                 | 抓取可控制如何在目前應用程式中套用視覺化樣式的屬性旗標。<br/>                                                                                                                     |
| [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect)                 | 針對視覺效果樣式所定義的背景，抓取內容區域的大小。<br/>                                                                                                                                  |
| [**GetThemeBackgroundExtent**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundextent)                           | 根據指定的內容區域，計算背景的大小和位置（視覺化樣式所定義）。<br/>                                                                                                                |
| [**GetThemeBackgroundRegion**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundregion)                           | 針對以指定矩形限定的一般或部分透明背景計算區域。<br/>                                                                                                         |
| [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                               | 抓取與特定主題、元件、狀態和屬性相關聯的點陣圖。<br/>                                                                                                                                     |
| [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool)                                                   | 從主題資料的 SysMetrics 區段中，抓取 **BOOL** 屬性的值。<br/>                                                                                                                                   |
| [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor)                                                 | 抓取 color 屬性的值。<br/>                                                                                                                                                                                |
| [**GetThemeDocumentationProperty**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemedocumentationproperty)                 | 從指定主題檔案的檔區段中，抓取主題屬性的值。<br/>                                                                                                                    |
| [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue)                                         | 捕獲列舉型別屬性的值。<br/>                                                                                                                                                                     |
| [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                           | 捕獲 filename 屬性的值。<br/>                                                                                                                                                                             |
| [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont)                                                   | 抓取字型屬性的值。 <br/>                                                                                                                                                                                |
| [**GetThemeInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint)                                                     | 捕獲 **int** 屬性的值。<br/>                                                                                                                                                                             |
| [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                             | 從視覺化樣式抓取 **int** 資料的清單。<br/>                                                                                                                                                                   |
| [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                             | 抓取 [**邊界**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) 屬性的值。<br/>                                                                                                                                                           |
| [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric)                                               | 抓取度量屬性的值。<br/>                                                                                                                                                                               |
| [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                           | 計算視覺化樣式所定義之元件的原始大小。<br/>                                                                                                                                                     |
| [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                           | 捕獲 position 屬性的值。<br/>                                                                                                                                                                             |
| [**GetThemePropertyOrigin**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepropertyorigin)                               | 抓取屬性之主題屬性定義的位置。 <br/>                                                                                                                                                |
| [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                   | 抓取 [**RECT**](/previous-versions//dd162897(v=vs.85)) 屬性的值。<br/>                                                                                                                                                                 |
| [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                               | 從指定的元件、狀態和屬性開始，抓取對應至指定之主題的資料流程。<br/>                                                                                                        |
| [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring)                                               | 抓取字串屬性的值。<br/>                                                                                                                                                                               |
| [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                             | 捕獲系統度量的布林值。<br/>                                                                                                                                                                         |
| [**GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                           | 捕獲系統色彩的值。<br/>                                                                                                                                                                                  |
| [**GetThemeSysColorBrush**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolorbrush)                                 | 捕獲系統色彩筆刷。<br/>                                                                                                                                                                                         |
| [**GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                             | 捕獲系統字型的 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 。<br/>                                                                                                                                                              |
| [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint)                                               | 捕獲系統 **int** 的值。 <br/>                                                                                                                                                                               |
| [**GetThemeSysSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyssize)                                             | 從主題資料抓取系統大小度量的值。<br/>                                                                                                                                                            |
| [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                                         | 捕獲系統字串的值。 <br/>                                                                                                                                                                                |
| [**GetThemeTextExtent**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemetextextent)                                       | 當以視覺化樣式字型呈現時，計算指定文字的大小和位置。<br/>                                                                                                                          |
| [**GetThemeTextMetrics**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemetextmetrics)                                     | 抓取特定元件的視覺化樣式所指定字型的相關資訊。<br/>                                                                                                                                 |
| [**GetThemeTransitionDuration**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemetransitionduration)                       | 取得指定之轉換的持續時間。<br/>                                                                                                                                                                         |
| [**GetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-getwindowtheme)                                               | 抓取已套用視覺化樣式之視窗的主題控制碼。<br/>                                                                                                                                                    |
| [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground)                               | 抓取視覺化樣式所指定背景中某個點的點擊測試程式碼。<br/>                                                                                                                                    |
| [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed)                                                     | 報告目前應用程式的使用者介面是否使用視覺化樣式來顯示。<br/>                                                                                                                                  |
| [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)                                     | 判斷主題是否可使用桌面視窗管理員 (DWM) 組合效果。<br/>                                                                                                                         |
| [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive)                                                 | 測試目前應用程式的視覺化樣式是否為作用中。<br/>                                                                                                                                                          |
| [**IsThemeBackgroundPartiallyTransparent**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemebackgroundpartiallytransparent) | 抓取視覺化樣式指定的背景是否有透明片段或 Alpha 混合的部分。<br/>                                                                                                          |
| [**IsThemeDialogTextureEnabled**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemedialogtextureenabled)                     | 報告指定的交談視窗是否支援背景紋理。<br/>                                                                                                                                                |
| [**IsThemePartDefined**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemepartdefined)                                       | 抓取視覺化樣式是否已針對指定的元件和狀態定義參數。<br/>                                                                                                                               |
| [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata)                                                 | 開啟視窗和其相關聯類別的主題資料。<br/>                                                                                                                                                             |
| [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex)                                             | 開啟與指定主題類別的視窗相關聯的主題資料。<br/>                                                                                                                                              |
| [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties)                                 | 設定旗標，以決定如何在呼叫的應用程式中執行視覺樣式。<br/>                                                                                                                             |
| [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)                                               | 使視窗使用的視覺效果樣式資訊集合，與類別一般使用的不同。<br/>                                                                                                                        |
| [**SetWindowThemeAttribute**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemeattribute)                             | 設定屬性，以控制如何將視覺效果樣式套用至指定的視窗。<br/>                                                                                                                                         |
| [**SetWindowThemeNonClientAttributes**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)         | 設定非用戶端屬性，以控制如何將視覺效果樣式套用至指定的視窗。<br/>                                                                                                                              |
| [**UpdatePanningFeedback**](/windows/desktop/api/Uxtheme/nf-uxtheme-updatepanningfeedback)                                 | 針對移動流覽手勢所產生的視窗，更新其狀態的用戶端。 只有在 [**BeginPanningFeedback**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginpanningfeedback) 呼叫之後，才能呼叫此函式。<br/>                                           |



 

### <a name="visual-styles-structures"></a>視覺化樣式結構



| 主題                                             | 目錄                                                                                                                                                      |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BP \_ ANIMATIONPARAMS**](/windows/desktop/api/Uxtheme/ns-uxtheme-bp_animationparams) | 定義 [**BeginBufferedPaint**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginbufferedpaint)所使用之 [**BP \_ PAINTPARAMS**](/windows/desktop/api/Uxtheme/ns-uxtheme-bp_paintparams)結構的動畫參數。<br/> |
| [**BP \_ PAINTPARAMS**](/windows/desktop/api/Uxtheme/ns-uxtheme-bp_paintparams)         | 定義 [**BeginBufferedPaint**](/windows/desktop/api/Uxtheme/nf-uxtheme-beginbufferedpaint)的繪製作業參數。<br/>                                                           |
| [**DTBGOPTS**](/windows/desktop/api/Uxtheme/ns-uxtheme-dtbgopts)                      | 定義 [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex) 函數的選項。<br/>                                                       |
| [**DTTOPTS**](/windows/desktop/api/Uxtheme/ns-uxtheme-dttopts)                        | 定義 [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) 函數的選項。<br/>                                                                   |
| [**INTLIST**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)                        | 包含來自視覺化樣式的 **整數** 資料項目陣列或清單。<br/>                                                                               |
| [**邊緣**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins)                        | 由 [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins) 函式傳回，以定義已套用視覺化樣式的視窗邊界。<br/>              |
| [**WTA \_ 選項**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)               | 定義用來設定視窗視覺化樣式屬性的選項。<br/>                                                                               |



 

### <a name="enumerated-types"></a>列舉類型



| 主題                                                        | 目錄                                                                                                               |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PROPERTYORIGIN**](/windows/desktop/api/Uxtheme/ne-uxtheme-propertyorigin)                     | 由 [**GetThemePropertyOrigin**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepropertyorigin) 傳回，以指定找到屬性的位置。<br/> |
| [**THEMESIZE**](/windows/desktop/api/Uxtheme/ne-uxtheme-themesize)                              | 識別要取出的視覺化樣式元件大小。 <br/>                                                  |
| [**TM \_ .PROPS**](tm-props.md)                                | 目前不支援。<br/>                                                                                    |
| [**WINDOWTHEMEATTRIBUTETYPE**](/windows/desktop/api/Uxtheme/ne-uxtheme-windowthemeattributetype) | 指定要在視窗上設定的視覺化樣式屬性型別。<br/>                                            |



 

### <a name="visual-styles-topics"></a>視覺化樣式主題



| 主題                                                                            | 目錄                                                                                                                                                                                  |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aero 樣式類別、元件和狀態](aero-style-classes-parts-and-states.md) | 描述 Aero 主題所支援的類別、元件和狀態，以定義預設 Windows Vista 使用的視覺效果樣式<br/>                                       |
| [主題檔案格式](themesfileformat-overview.md)                               | 討論主題 ( 的格式。主題) 檔。 <br/>                                                                                                                                 |
| [格式值](theme-format-values.md)                                         | 列出與 [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext)和 [**GetThemeTextExtent**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemetextextent)函數的 *dwTextFlags* 參數搭配使用的值。 <br/> |
| [點擊測試選項](theme-hit-test-options.md)                                   | 列出與 [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground)函數的 *>dwoptions* 參數搭配使用的選項值。 <br/>                                |
| [點擊測試傳回值](theme-hit-test-retval.md)                              | 列出在 [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground)函數的 *pwHitTestCode* 參數中傳回的點擊測試程式碼值。 <br/>                   |
| [Parts and States](parts-and-states.md)                                         | 描述啟用視覺化樣式時，用來變更控制面板的部分和狀態。 <br/>                                                              |
| [屬性識別項](property-typedefs.md)                                    | 包含已定義值的相關資訊，這些值可用來取出視覺化樣式的屬性。 <br/>                                                                              |



 

 

