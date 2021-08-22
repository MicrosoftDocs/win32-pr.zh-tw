---
title: 所有 WCS 函數的字母順序清單
description: 以下是 Windows \ 160; 98 和更新版本以及 Windows \ 160; 2000 和更新版本所提供之 WCS 1.0 API 函式的完整字母順序清單。
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows色彩系統 (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e2c9250cc9fb1e9e418079ed3b9524b3add2535dd780eed65ae998bda80ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706658"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>所有 WCS 函數的字母順序清單

以下是 Windows 98 和更新版本以及 Windows 2000 和更新版本所提供之 WCS 1.0 API 函式的完整字母順序清單。



| 函數或結構                                                                 | 描述                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (或 **ApplyCallbackFunction**) 是一種回呼函式，您會在執行 [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) 函式所顯示的對話方塊時，執行此函數來更新 WCS 設定資料。 |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | 將指定的色彩設定檔與指定的裝置產生關聯。                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | 檢查指定點陣圖中的圖元是否位於指定轉換 [的輸出範圍](g.md) 內。 |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | 判斷陣列中的色彩是否位於指定轉換 [的輸出範圍](g.md) 內。 |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | 檢查指定的色彩是否在裝置的範圍中。                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | 關閉開啟的設定檔控制碼。 |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | 判斷指定的色彩是否位於指定轉換 [的輸出範圍](./g.md) 內。 |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | 判斷指定的 RGB 三合一是否位於指定轉換 [的輸出範圍](./g.md) 中。 |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | 針對輸出範圍檢查點陣圖色彩。                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | 將命名色彩空間中的色彩名稱轉換成色彩設定檔中的索引編號 |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | 以國際色彩協會在其 ICC 配置檔案格式規格中指定的格式建立 [裝置連結設定檔](./d.md) 。 |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | 接受設定檔的陣列或單一 [裝置連結設定檔](./d.md) ，並建立色彩轉換。 這項轉換是從第一個設定檔所指定的色彩空間到第二個設定檔的對應，依此類推到最後一個設定檔的對應。 |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | 從 [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) 結構建立顯示色彩設定檔。 |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | 從 [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) 結構建立顯示色彩設定檔。 |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | 已取代。 沒有取代的 API，因為不再使用此 API。 不需要替代的 CMM 模組開發人員來執行它。 |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | 建立從輸入 [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) 對應至選擇性目標空間的色彩轉換，然後使用一組旗標來定義應如何建立轉換，以將其對應至輸出裝置。 |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | 建立從輸入 [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) 對應至選擇性目標空間的色彩轉換，然後使用一組旗標來定義應如何建立轉換，以將其對應至輸出裝置。 |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | 已取代。 沒有取代的 API，因為不再使用此 API。 不需要替代的 CMM 模組開發人員來執行它。 |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | 刪除指定的色彩轉換，並釋出任何與其相關聯的記憶體。 |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | 抓取 (CMM) 的色彩管理模組的各種相關資訊。 |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | 抓取指定之命名色彩設定檔的相關資訊。 |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | 取得 PostScript 色彩轉譯字典。                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | 從設定檔抓取 PostScript 層級2色彩轉譯[意圖](rendering-intents.md)。 |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | 取得 PostScript 的色彩空間陣列。                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | 報告指定的設定檔是否為可用於色彩管理的有效 ICC 設定檔。 |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | 使用色彩轉換，將色彩的陣列從來源 [色彩空間](color-spaces.md) 轉譯為目的色彩空間。 |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | 將應用程式提供的 RGBQuad 轉譯成裝置 [色彩空間](color-spaces.md)。 |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | 使用色彩轉換，將點陣圖從某個 [色彩空間](color-spaces.md) 轉譯成另一個。 |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | 將點陣圖從一個已定義的格式轉譯為不同的定義格式，並定期呼叫回呼函式（如果有指定），以報告進度並允許呼叫應用程式終止翻譯。 |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | 更正裝置內容之調色板中的專案。                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | 針對預覽用途執行色彩對應。                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | 將命名色彩空間中的色彩名稱轉換成 (ICC) 色彩設定檔的國際色彩協會中的索引編號。 |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | 建立色彩空間。                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | 將色彩空間中的索引轉換為命名色彩空間中的名稱陣列。 |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | 接受設定檔的陣列或單一 [裝置連結設定檔](d.md) ，並建立應用程式可用來執行色彩對應的色彩轉換。 |
| [**CreateProfileFromLogColorSpaceW**] ( (/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)  | 將邏輯 [色彩空間](c.md) 轉換成 [裝置設定檔](d.md)。 |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | 刪除色彩空間。                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | 刪除指定的色彩轉換。 |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | 解除指定的色彩設定檔與指定電腦上的指定裝置。 |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | 列舉滿足指定列舉準則的所有設定檔。 |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | 列舉適用于指定之裝置內容的輸出色彩設定檔。                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)的應用程式定義回呼函數。                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | 抓取有關建立指定的色彩轉換 (CMM) 之色彩管理模組的各種資訊。 |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | 抓取指定電腦上 Windows COLOR 目錄的路徑。 |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | 從指定的色彩設定檔中指定的已標記設定檔元素，將資料複製到緩衝區。 |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | 在指定的國際色彩協會)  (的標記資料表中，抓取 *dwIndex* 所指定的標籤名稱，其中 *dwIndex* 是該資料表中以單一為基礎的索引。 |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | 針對開啟色彩設定檔的控制碼，抓取色彩設定檔內容。                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | 從 ICC 色彩設定檔或 WCS XML 設定檔，抓取或衍生 ICC 標頭結構。 驅動程式和應用程式應該假設傳回 **TRUE** 只表示傳回的是正確結構化的標頭。 每個標記仍然需要使用舊版 ICM2 Api 或 XML 架構 Api 獨立進行驗證。 |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | 取得裝置內容中目前的輸入色彩空間。 |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | 抓取指定色彩設定檔中的已標記元素數目。 |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | 從直接色彩顯示面板取得 gamma 曲線。                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | 取得裝置內容目前的輸出色彩設定檔。                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | 取得裝置內容的 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) 結構。                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | 抓取第一個參數中所指定的「國際色彩協會」 (ICC) 命名色彩設定檔的相關資訊。 |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | 從指定的 ICC 色彩設定檔抓取 PostScript 層級2色彩轉譯字典。 |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | 從 ICC 色彩設定檔抓取 PostScript 層級2色彩轉譯[意圖](r.md)。 |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | 從 ICC 色彩設定檔抓取 PostScript 層級 2[色彩空間](c.md)陣列。 |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | 抓取已針對指定標準 [色彩空間](c.md)註冊的色彩設定檔。 |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | 應用程式提供的回呼，以報告進度。                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | 安裝指定的設定檔，以便在指定的電腦上使用。 設定檔也會複製到 COLOR 目錄。 |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | 報告指定的國際色彩協會 (ICC) 標記是否存在於指定的色彩設定檔中。 |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | 可讓您判斷指定的設定檔是否為有效的國際色彩協會 (ICC) 設定檔，或可用於色彩管理的有效 Windows 色彩系統 (WCS) 設定檔控制碼。 |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | 建立指定之色彩設定檔的控制碼。 然後，控制碼可用於其他設定檔管理功能。 |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | 將指定的識別值與指定的色彩管理模組動態連結程式庫產生關聯 (的 CMM DLL) 。 當此識別碼出現在色彩設定檔時，Windows 可以找到對應的 CMM，以便建立轉換。 |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | 可讓您選取慣用的色彩管理模組 (要使用的 CMM) 。 |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | 設定 ICC 色彩設定檔中已標記之設定檔元素的元素資料。 |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | 在指定的 ICC 色彩設定檔中，建立參考與現有標記相同資料的新標記。 |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | 設定 ICC 色彩設定檔中標記專案的大小。 |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | 設定指定之 ICC 色彩設定檔中的標頭資料。 |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | 設定裝置內容的輸入色彩空間。                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | 設定直接色彩顯示面板上的 gamma 曲線。                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | 在裝置內容中開啟或關閉色彩管理。                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | 設定指定之裝置內容的輸出色彩設定檔。                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | 針對指定的標準 [色彩空間](c.md)，註冊指定的設定檔。 您可以使用 [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)來查詢設定檔。 |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | 以對話方塊的方式，提供使用者控制項的色彩管理。                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | 使用色彩轉換來轉換點陣圖色彩。                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | 將色彩的陣列從來源 [色彩空間](c.md) 轉譯為目的色彩空間，如色彩轉換所定義。 |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | 從指定的電腦移除指定的色彩設定檔。 相關聯的檔案會選擇性地從系統中刪除。 |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | 從指定的色彩管理模組動態連結程式庫分離指定的識別碼值， (CMM DLL) 。 |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | 將指定的 WCS 色彩設定檔與指定的裝置產生關聯。                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | 判斷陣列中的色彩是否位於指定之 WCS 色彩轉換的輸出範圍內。                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | 將 WCS 設定檔轉換成 ICC 設定檔。                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | 解除指定的 WCS 色彩設定檔與指定電腦上的指定裝置。                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | 列舉符合指定設定檔管理範圍中的列舉準則的所有色彩設定檔。                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | 傳回 [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) 函式列舉色彩設定檔所需的緩衝區大小（以位元組為單位）。 |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | 決定是否啟用顯示校正狀態的系統管理。                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | 抓取裝置的預設色彩設定檔，或如果未指定裝置，則抓取與裝置無關的預設設定檔。                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | 傳回裝置預設色彩設定檔名稱的大小（以位元組為單位），包括 **Null** 結束字元。                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | 傳回使用者或全系統轉譯意圖。                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | 判斷使用者是否已選擇針對指定的裝置使用每個使用者設定檔關聯清單。                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | 建立指定之色彩設定檔的控制碼。                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | 啟用或停用顯示器校正狀態的系統管理。                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | 設定指定設定檔管理範圍中指定配置檔案類型的預設色彩設定檔名稱。                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | 設定使用者或全系統轉譯意圖。                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | 允許使用者指定是否要針對指定的裝置使用每個使用者設定檔關聯清單。                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | 將色彩的陣列從來源色彩空間轉譯為目的色彩空間，如色彩轉換所定義。                            |



 

 

 